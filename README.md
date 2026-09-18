<!DOCTYPE html>
<html lang="ko" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FLY FILM | 프리미엄 초고화질 드론 항공 촬영 전문 스튜디오</title>
    
    <!-- Google Fonts (Inter & Noto Sans KR) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Noto+Sans+KR:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            50: '#f0f9ff',
                            100: '#e0f2fe',
                            400: '#38bdf8',
                            500: '#0284c7',
                            600: '#0369a1',
                            900: '#0c4a6e',
                            accent: '#06b6d4',
                            gold: '#f59e0b'
                        },
                        dark: {
                            bg: '#090d16',
                            card: '#111827',
                            border: '#1f2937',
                            muted: '#374151'
                        }
                    },
                    fontFamily: {
                        sans: ['Noto Sans KR', 'Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #090d16;
            color: #f3f4f6;
            font-family: 'Noto Sans KR', 'Inter', sans-serif;
            overflow-x: hidden;
        }

        /* Dynamic Glassmorphism */
        .glass-panel {
            background: rgba(17, 24, 39, 0.75);
            backdrop-filter: blur(14px);
            -webkit-backdrop-filter: blur(14px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .glass-card {
            background: rgba(15, 23, 42, 0.65);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .glass-card:hover {
            border-color: rgba(6, 182, 212, 0.45);
            transform: translateY(-4px);
            box-shadow: 0 16px 35px -10px rgba(6, 182, 212, 0.25);
        }

        /* Cyan Glow Effect */
        .cyan-glow {
            box-shadow: 0 0 30px rgba(6, 182, 212, 0.35);
        }

        .text-gradient {
            background: linear-gradient(135deg, #ffffff 0%, #38bdf8 50%, #06b6d4 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .gold-gradient {
            background: linear-gradient(135deg, #fbbf24 0%, #f59e0b 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #090d16;
        }
        ::-webkit-scrollbar-thumb {
            background: #1f2937;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #0284c7;
        }

        @keyframes pulseGlow {
            0%, 100% { opacity: 0.4; transform: scale(1); }
            50% { opacity: 0.7; transform: scale(1.08); }
        }

        .animate-pulse-slow {
            animation: pulseGlow 6s infinite ease-in-out;
        }
    </style>
</head>
<body class="antialiased selection:bg-brand-500 selection:text-white">

    <header class="fixed top-0 left-0 w-full z-50 transition-all duration-300" id="main-header">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20 glass-panel rounded-b-2xl px-6 my-2 border-t-0">
                <!-- Logo -->
                <a href="#" class="flex items-center gap-3 group">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-brand-500 to-brand-accent flex items-center justify-center text-white text-xl font-black shadow-lg shadow-brand-500/30 group-hover:scale-105 transition-transform">
                        <i class="fa-solid fa-plane-up"></i>
                    </div>
                    <div>
                        <span class="text-2xl font-black tracking-wider text-white">FLY <span class="text-brand-accent">FILM</span></span>
                        <span class="block text-[10px] tracking-widest text-gray-400 font-semibold -mt-1">AERIAL STUDIO</span>
                    </div>
                </a>

                <!-- Desktop Menu Links -->
                <nav class="hidden md:flex items-center space-x-8 text-sm font-medium">
                    <a href="#about" class="text-gray-300 hover:text-brand-accent transition-colors">소개</a>
                    <a href="#services" class="text-gray-300 hover:text-brand-accent transition-colors">촬영 분야</a>
                    <a href="#portfolio" class="text-gray-300 hover:text-brand-accent transition-colors">포트폴리오</a>
                    <a href="#fleet" class="text-gray-300 hover:text-brand-accent transition-colors">보유 장비</a>
                    <a href="#estimator" class="text-gray-300 hover:text-brand-accent transition-colors flex items-center gap-1.5">
                        <span>실시간 견적</span>
                        <span class="px-2 py-0.5 text-[10px] bg-brand-500/20 text-brand-accent rounded-full font-bold border border-brand-500/30">BEST</span>
                    </a>
                    <a href="#faq" class="text-gray-300 hover:text-brand-accent transition-colors">FAQ</a>
                </nav>

                <!-- Header Action Buttons -->
                <div class="hidden sm:flex items-center gap-4">
                    <a href="tel:01098765432" class="text-gray-300 hover:text-white text-xs font-semibold flex items-center gap-2 px-3 py-2 rounded-lg hover:bg-gray-800/50 transition-colors">
                        <i class="fa-solid fa-phone text-brand-accent"></i>
                        <span>010-9876-5432</span>
                    </a>
                    <a href="#contact" class="px-5 py-2.5 rounded-xl bg-gradient-to-r from-brand-500 to-brand-accent hover:from-brand-600 hover:to-cyan-600 text-white font-semibold text-sm transition-all shadow-md shadow-brand-500/20 hover:shadow-lg hover:shadow-brand-accent/40 flex items-center gap-2">
                        <i class="fa-solid fa-paper-plane text-xs"></i>
                        <span>촬영 문의하기</span>
                    </a>
                </div>

                <!-- Mobile Menu Toggle Button -->
                <button id="mobile-menu-btn" class="md:hidden text-gray-300 hover:text-white p-2 text-xl focus:outline-none" aria-label="메뉴 열기">
                    <i class="fa-solid fa-bars"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Navigation Drawer -->
        <div id="mobile-menu" class="hidden md:hidden glass-panel mx-4 mt-2 rounded-2xl p-6 border border-gray-800 transition-all">
            <div class="flex flex-col space-y-4">
                <a href="#about" class="mobile-link text-gray-200 hover:text-brand-accent text-lg font-medium py-2 border-b border-gray-800/60">소개</a>
                <a href="#services" class="mobile-link text-gray-200 hover:text-brand-accent text-lg font-medium py-2 border-b border-gray-800/60">촬영 분야</a>
                <a href="#portfolio" class="mobile-link text-gray-200 hover:text-brand-accent text-lg font-medium py-2 border-b border-gray-800/60">포트폴리오</a>
                <a href="#fleet" class="mobile-link text-gray-200 hover:text-brand-accent text-lg font-medium py-2 border-b border-gray-800/60">보유 장비</a>
                <a href="#estimator" class="mobile-link text-gray-200 hover:text-brand-accent text-lg font-medium py-2 border-b border-gray-800/60 flex justify-between items-center">
                    <span>실시간 견적 계산기</span>
                    <span class="px-2 py-0.5 text-xs bg-brand-500/20 text-brand-accent rounded-full font-bold">인기</span>
                </a>
                <a href="#faq" class="mobile-link text-gray-200 hover:text-brand-accent text-lg font-medium py-2 border-b border-gray-800/60">FAQ</a>
                <a href="tel:01098765432" class="mobile-link text-brand-accent font-bold py-2 flex items-center justify-center gap-2 bg-brand-500/10 rounded-xl">
                    <i class="fa-solid fa-phone"></i> 직통 전화: 010-8931-8536
                </a>
                <a href="#contact" class="mobile-link mt-2 py-3 text-center rounded-xl bg-gradient-to-r from-brand-500 to-brand-accent text-white font-bold">촬영 문의하기</a>
            </div>
        </div>
    </header>

    <section class="relative min-h-screen flex items-center justify-center pt-28 pb-16 overflow-hidden">
        <!-- Canvas Flight Background Animation -->
        <canvas id="hero-canvas" class="absolute inset-0 w-full h-full pointer-events-none opacity-40"></canvas>
        
        <!-- Glowing Ambient Lighting Effects -->
        <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-brand-500/20 rounded-full blur-[140px] pointer-events-none animate-pulse-slow"></div>
        <div class="absolute bottom-10 right-10 w-[400px] h-[400px] bg-brand-accent/15 rounded-full blur-[120px] pointer-events-none"></div>

        <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center z-10">
            <!-- Badge -->
            <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full glass-card border border-brand-accent/30 text-xs sm:text-sm font-medium text-brand-accent mb-8 shadow-lg">
                <span class="w-2 h-2 rounded-full bg-brand-accent animate-ping"></span>
                <i class="fa-solid fa-shield-halved"></i> 국토교통부 정식 승인업체 · 10억원 영업배상책임보험 가입
            </div>

            <!-- Headline -->
            <h1 class="text-4xl sm:text-6xl lg:text-7xl font-black tracking-tight leading-tight sm:leading-none mb-8">
                하늘에서 바라보는<br class="sm:hidden" /> 시선의 한계,<br />
                <span class="text-gradient">FLY FILM</span>이 넘어서다
            </h1>

            <!-- Subtitle -->
            <p class="max-w-3xl mx-auto text-base sm:text-xl text-gray-300 font-light mb-10 leading-relaxed">
                시네마틱 8K 초고화질 항공 영상부터 다이내믹한 FPV 액션 비행까지.<br class="hidden sm:inline" />
                영화, 방송, CF, 건설, 행사 현장을 최고의 각도와 연출로 담아냅니다.
            </p>

            <!-- Hero Action Buttons -->
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4 sm:gap-6 mb-16">
                <a href="#portfolio" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-gradient-to-r from-brand-500 to-brand-accent hover:from-brand-600 hover:to-cyan-600 text-white font-bold text-lg transition-all shadow-xl shadow-brand-500/25 hover:scale-105 flex items-center justify-center gap-3">
                    <i class="fa-solid fa-play text-sm"></i>
                    <span>포트폴리오 감상</span>
                </a>
                <a href="#estimator" class="w-full sm:w-auto px-8 py-4 rounded-xl glass-panel hover:bg-gray-800/80 text-white font-bold text-lg border border-gray-700 hover:border-brand-accent/50 transition-all flex items-center justify-center gap-3">
                    <i class="fa-solid fa-calculator text-brand-accent"></i>
                    <span>실시간 촬영 견적 산출</span>
                </a>
            </div>

            <!-- Key Highlights Stats Grid -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 max-w-5xl mx-auto text-left">
                <div class="glass-card p-5 rounded-2xl border-l-4 border-l-brand-accent">
                    <div class="text-3xl font-black text-white mb-1"><span class="counter" data-target="520">0</span>+</div>
                    <div class="text-xs text-gray-400 font-medium">누적 촬영 프로젝트</div>
                </div>
                <div class="glass-card p-5 rounded-2xl border-l-4 border-l-brand-500">
                    <div class="text-3xl font-black text-white mb-1"><span class="counter" data-target="2800">0</span>시간</div>
                    <div class="text-xs text-gray-400 font-medium">무사고 안전 비행 실적</div>
                </div>
                <div class="glass-card p-5 rounded-2xl border-l-4 border-l-brand-gold">
                    <div class="text-3xl font-black text-white mb-1">8K / 4K</div>
                    <div class="text-xs text-gray-400 font-medium">ProRes RAW 초고화질</div>
                </div>
                <div class="glass-card p-5 rounded-2xl border-l-4 border-l-emerald-500">
                    <div class="text-3xl font-black text-white mb-1">100%</div>
                    <div class="text-xs text-gray-400 font-medium">비행/촬영 원스톱 허가 대행</div>
                </div>
            </div>
        </div>
    </section>

    <section class="py-10 border-y border-gray-800/80 bg-dark-card/40">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <p class="text-center text-xs font-semibold text-gray-500 uppercase tracking-widest mb-6">신뢰로 입증된 주요 고객사 및 협력 분야</p>
            <div class="flex flex-wrap justify-center items-center gap-8 md:gap-16 opacity-75 grayscale hover:grayscale-0 transition-all duration-300 text-gray-300 font-bold text-sm sm:text-base">
                <div class="flex items-center gap-2 hover:text-brand-accent transition-colors"><i class="fa-solid fa-tv text-2xl text-brand-accent"></i> 주요 지상파 방송사</div>
                <div class="flex items-center gap-2 hover:text-brand-500 transition-colors"><i class="fa-solid fa-building text-2xl text-brand-500"></i> 국내 대형 건설사</div>
                <div class="flex items-center gap-2 hover:text-brand-gold transition-colors"><i class="fa-solid fa-landmark text-2xl text-brand-gold"></i> 지방자치단체 & 공공기관</div>
                <div class="flex items-center gap-2 hover:text-cyan-400 transition-colors"><i class="fa-solid fa-clapperboard text-2xl text-cyan-400"></i> 영화 & CF 제작사</div>
                <div class="flex items-center gap-2 hover:text-emerald-400 transition-colors"><i class="fa-solid fa-mountain-sun text-2xl text-emerald-400"></i> 관광공사 및 리조트</div>
            </div>
        </div>
    </section>

    <section id="about" class="py-24 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <h2 class="text-xs font-bold text-brand-accent uppercase tracking-widest mb-3">WHY CHOOSE FLY FILM</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-white">비행의 안정성과 감각적인 앵글,<br />왜 FLY FILM 이어야 할까요?</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Strength 1 -->
                <div class="glass-card p-8 rounded-3xl relative overflow-hidden group">
                    <div class="w-14 h-14 rounded-2xl bg-brand-500/10 border border-brand-500/30 flex items-center justify-center text-brand-accent text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-file-contract"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3">100% 원스톱 허가 대행</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        서울 도심, 비행금지구역(P73), 관제권, 군사시설 등 까다로운 구역도 드론원스톱 민원서비스를 통해 비행승인 및 촬영허가를 완벽히 책임지고 사전 진행합니다.
                    </p>
                </div>

                <!-- Strength 2 -->
                <div class="glass-card p-8 rounded-3xl relative overflow-hidden group">
                    <div class="w-14 h-14 rounded-2xl bg-brand-accent/10 border border-brand-accent/30 flex items-center justify-center text-brand-accent text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-certificate"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3">1급 전문 조종자 라이선스</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        국토교통부 인증 초경량비행장치 1급 조종자 및 지도조종자 자격을 보유한 베테랑 전문가가 전 공정을 전담하여 그 어떤 환경에서도 안전하게 촬영합니다.
                    </p>
                </div>

                <!-- Strength 3 -->
                <div class="glass-card p-8 rounded-3xl relative overflow-hidden group">
                    <div class="w-14 h-14 rounded-2xl bg-brand-gold/10 border border-brand-gold/30 flex items-center justify-center text-brand-gold text-2xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-camera-retro"></i>
                    </div>
                    <h3 class="text-xl font-bold text-white mb-3">시네마급 장비 & FPV 라인업</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        DJI Inspire 3 풀프레임 8K부터 시네마 카메라인 RED/ARRI 커스텀 탑재 드론, 좁은 공간을 누비는 다이내믹 4K FPV 드론까지 촬영 목적별 맞춤 투입됩니다.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <section id="services" class="py-24 bg-dark-card/30 relative border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-16">
                <div>
                    <h2 class="text-xs font-bold text-brand-accent uppercase tracking-widest mb-3">OUR SERVICES</h2>
                    <p class="text-3xl sm:text-4xl font-extrabold text-white">고객의 니즈에 맞춘 전문 촬영 영역</p>
                </div>
                <p class="text-gray-400 text-sm max-w-md mt-4 md:mt-0">
                    기획 단계의 앵글 컨설팅부터 현장 비행, 후반 컬러그레이딩(Color Grading) 편집까지 원스톱 솔루션을 제공합니다.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="glass-panel p-8 rounded-3xl hover:border-brand-accent/50 transition-all">
                    <div class="text-4xl text-brand-accent mb-6"><i class="fa-solid fa-bullhorn"></i></div>
                    <h3 class="text-2xl font-bold text-white mb-3">기업 & 홍보 영상</h3>
                    <p class="text-gray-400 text-sm mb-6 leading-relaxed">
                        아파트 분양 조망권, 기업 사옥, 지자체 관광지, 골프장, 리조트 등 웅장하고 아름다운 조감 뷰와 스무스한 트래킹 샷을 제공합니다.
                    </p>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-gray-800 pt-4">
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>건설사 분양 조망권 (층별 Height Shot)</li>
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>지역 축제 및 시정 홍보 영상</li>
                    </ul>
                </div>

                <!-- Service 2 -->
                <div class="glass-panel p-8 rounded-3xl hover:border-brand-accent/50 transition-all">
                    <div class="text-4xl text-brand-500 mb-6"><i class="fa-solid fa-film"></i></div>
                    <h3 class="text-2xl font-bold text-white mb-3">영화, 드라마 & CF</h3>
                    <p class="text-gray-400 text-sm mb-6 leading-relaxed">
                        감독의 연출 의도를 정확히 이해하는 인스파이어 3 듀얼 조종(조종사+카메라맨) 시스템으로 고난도 원테이크 시네마틱 액션을 제작합니다.
                    </p>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-gray-800 pt-4">
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>8K CinemaDNG / ProRes RAW 대응</li>
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>듀얼 조종을 통한 정밀 피사체 추적</li>
                    </ul>
                </div>

                <!-- Service 3 -->
                <div class="glass-panel p-8 rounded-3xl hover:border-brand-accent/50 transition-all">
                    <div class="text-4xl text-brand-gold mb-6"><i class="fa-solid fa-bolt"></i></div>
                    <h3 class="text-2xl font-bold text-white mb-3">FPV 다이내믹 원테이크</h3>
                    <p class="text-gray-400 text-sm mb-6 leading-relaxed">
                        일반 드론으로는 불가능한 창문 통과, 초고속 질주, 스릴 넘치는 인테리어 투어 등 강렬하고 몰입감 넘치는 몰입형 앵글을 연출합니다.
                    </p>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-gray-800 pt-4">
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>실내 오피스/공장 원테이크 투어</li>
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>자동차/스포츠 초고속 추적 비행</li>
                    </ul>
                </div>

                <!-- Service 4 -->
                <div class="glass-panel p-8 rounded-3xl hover:border-brand-accent/50 transition-all">
                    <div class="text-4xl text-emerald-400 mb-6"><i class="fa-solid fa-compass-drafting"></i></div>
                    <h3 class="text-2xl font-bold text-white mb-3">건설 / 측량 / 3D 맵핑</h3>
                    <p class="text-gray-400 text-sm mb-6 leading-relaxed">
                        대규모 토목 현장의 월별 공정률 기록, 안전 점검, 정밀 RTK 기반 3D Orthomosaic 맵핑 및 점군(Point Cloud) 데이터를 산출합니다.
                    </p>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-gray-800 pt-4">
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>RTK 오차범위 수 cm 내 정밀 측정</li>
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>월간 현장 공정 영상 보고서 제작</li>
                    </ul>
                </div>

                <!-- Service 5 -->
                <div class="glass-panel p-8 rounded-3xl hover:border-brand-accent/50 transition-all">
                    <div class="text-4xl text-purple-400 mb-6"><i class="fa-solid fa-tower-broadcast"></i></div>
                    <h3 class="text-2xl font-bold text-white mb-3">야외 행사 & 중계 라이브</h3>
                    <p class="text-gray-400 text-sm mb-6 leading-relaxed">
                        스포츠 경기, 야외 뮤직 페스티벌, 마라톤 대회 등의 생중계 현장에 SDI/HDMI 라이브 피드 송출로 생동감을 더합니다.
                    </p>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-gray-800 pt-4">
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>무선 1080p/4K 실시간 영상 중계 송출</li>
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>안전 가이드라인 준수 야간 비행 허가</li>
                    </ul>
                </div>

                <!-- Service 6 -->
                <div class="glass-panel p-8 rounded-3xl hover:border-brand-accent/50 transition-all">
                    <div class="text-4xl text-pink-400 mb-6"><i class="fa-solid fa-wand-magic-sparkles"></i></div>
                    <h3 class="text-2xl font-bold text-white mb-3">종합 편집 & CG</h3>
                    <p class="text-gray-400 text-sm mb-6 leading-relaxed">
                        원본 소스 제공뿐만 아니라, 음원 라이선스 확보, 모션 그래픽 자막, 4K 색보정 편집까지 완벽한 완성본을 제작합니다.
                    </p>
                    <ul class="text-xs text-gray-300 space-y-2 border-t border-gray-800 pt-4">
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>상업용 음원 BGM 라이선스 제공</li>
                        <li><i class="fa-solid fa-check text-brand-accent mr-2"></i>경계선 및 위치 모션 그래픽 CG</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="portfolio" class="py-24 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <h2 class="text-xs font-bold text-brand-accent uppercase tracking-widest mb-3">PORTFOLIO</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-white">FLY FILM이 담아낸 주요 작품</p>
                <p class="text-gray-400 text-sm mt-3">카드 항목을 클릭하시면 상세한 촬영 정보와 미리보기를 확인하실 수 있습니다.</p>
            </div>

            <!-- Category Filter Buttons -->
            <div class="flex flex-wrap justify-center gap-2 sm:gap-4 mb-12" id="portfolio-filters">
                <button data-filter="all" class="portfolio-filter-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all bg-gradient-to-r from-brand-500 to-brand-accent text-white shadow-md">전체보기</button>
                <button data-filter="promo" class="portfolio-filter-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all glass-card text-gray-300 hover:text-white">기업/홍보</button>
                <button data-filter="cinema" class="portfolio-filter-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all glass-card text-gray-300 hover:text-white">방송/영화/CF</button>
                <button data-filter="fpv" class="portfolio-filter-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all glass-card text-gray-300 hover:text-white">FPV 액션</button>
                <button data-filter="survey" class="portfolio-filter-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all glass-card text-gray-300 hover:text-white">건설/측량</button>
            </div>

            <!-- Portfolio Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="portfolio-grid">
                <!-- Portfolio Item 1 -->
                <div class="portfolio-item glass-card rounded-3xl overflow-hidden group cursor-pointer" data-category="promo" data-title="송도 하이엔드 아파트 조망권 촬영" data-desc="고층 수평 조감도 및 각 층별 해안가 오션뷰 시뮬레이션 촬영" data-equipment="DJI Inspire 3 (8K)" data-date="2026년 2월" data-img="https://images.unsplash.com/photo-1508614589041-895b88991e3e?auto=format&fit=crop&w=1000&q=80">
                    <div class="relative h-60 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1508614589041-895b88991e3e?auto=format&fit=crop&w=1000&q=80" alt="송도 조망권 촬영" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark-bg via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-4 left-4 px-3 py-1 bg-brand-500/80 text-white text-xs font-bold rounded-lg backdrop-blur-md">기업/홍보</span>
                        <div class="absolute bottom-4 left-4 right-4 flex justify-between items-center">
                            <span class="text-xs text-brand-accent font-mono"><i class="fa-solid fa-video"></i> 8K ProRes</span>
                            <div class="w-10 h-10 rounded-full bg-brand-accent/90 text-dark-bg flex items-center justify-center font-bold group-hover:scale-110 transition-transform"><i class="fa-solid fa-play"></i></div>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-lg font-bold text-white mb-2 group-hover:text-brand-accent transition-colors">송도 하이엔드 아파트 조망권 촬영</h4>
                        <p class="text-gray-400 text-xs line-clamp-2">고층 수평 조감도 및 각 층별 해안가 오션뷰 시뮬레이션 촬영 진행</p>
                    </div>
                </div>

                <!-- Portfolio Item 2 -->
                <div class="portfolio-item glass-card rounded-3xl overflow-hidden group cursor-pointer" data-category="cinema" data-title="시네마틱 블록버스터 드라마 야외 추격씬" data-desc="빠르게 달리는 차량 추적 및 산악 지형 저고도 고속 비행 촬영" data-equipment="DJI Inspire 3 & RED Komodo" data-date="2026년 1월" data-img="https://images.unsplash.com/photo-1473968512647-3e447244af8f?auto=format&fit=crop&w=1000&q=80">
                    <div class="relative h-60 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1473968512647-3e447244af8f?auto=format&fit=crop&w=1000&q=80" alt="드라마 추격씬" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark-bg via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-4 left-4 px-3 py-1 bg-purple-600/80 text-white text-xs font-bold rounded-lg backdrop-blur-md">방송/영화</span>
                        <div class="absolute bottom-4 left-4 right-4 flex justify-between items-center">
                            <span class="text-xs text-brand-accent font-mono"><i class="fa-solid fa-film"></i> Cinema RAW</span>
                            <div class="w-10 h-10 rounded-full bg-brand-accent/90 text-dark-bg flex items-center justify-center font-bold group-hover:scale-110 transition-transform"><i class="fa-solid fa-play"></i></div>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-lg font-bold text-white mb-2 group-hover:text-brand-accent transition-colors">시네마틱 드라마 야외 추격씬</h4>
                        <p class="text-gray-400 text-xs line-clamp-2">빠르게 달리는 차량 추적 및 산악 지형 저고도 고속 비행 연출</p>
                    </div>
                </div>

                <!-- Portfolio Item 3 -->
                <div class="portfolio-item glass-card rounded-3xl overflow-hidden group cursor-pointer" data-category="fpv" data-title="모터스포츠 경주 트랙 FPV 초고속 추적" data-desc="시속 130km/h 레이싱카와의 밀착 추적 FPV 원테이크 비행" data-equipment="Custom 5인치 FPV + GoPro 12" data-date="2025년 12월" data-img="https://images.unsplash.com/photo-1527977966376-1c8408f9f108?auto=format&fit=crop&w=1000&q=80">
                    <div class="relative h-60 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1527977966376-1c8408f9f108?auto=format&fit=crop&w=1000&q=80" alt="FPV 레이싱" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark-bg via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-4 left-4 px-3 py-1 bg-brand-gold/80 text-dark-bg text-xs font-bold rounded-lg backdrop-blur-md">FPV 액션</span>
                        <div class="absolute bottom-4 left-4 right-4 flex justify-between items-center">
                            <span class="text-xs text-brand-accent font-mono"><i class="fa-solid fa-bolt"></i> 130km/h FPV</span>
                            <div class="w-10 h-10 rounded-full bg-brand-accent/90 text-dark-bg flex items-center justify-center font-bold group-hover:scale-110 transition-transform"><i class="fa-solid fa-play"></i></div>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-lg font-bold text-white mb-2 group-hover:text-brand-accent transition-colors">모터스포츠 FPV 초고속 추적</h4>
                        <p class="text-gray-400 text-xs line-clamp-2">시속 130km 레이싱 카와의 다이내믹한 밀착 추적 원테이크 비행</p>
                    </div>
                </div>

                <!-- Portfolio Item 4 -->
                <div class="portfolio-item glass-card rounded-3xl overflow-hidden group cursor-pointer" data-category="survey" data-title="대형 스마트 물류단지 3D 정밀 맵핑" data-desc="RTK 드론을 활용한 10만 평 부지 공정률 분석 및 데이터 제작" data-equipment="DJI Matrice 350 RTK" data-date="2025년 11월" data-img="https://images.unsplash.com/photo-1508444845599-5c89863b1c44?auto=format&fit=crop&w=1000&q=80">
                    <div class="relative h-60 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1508444845599-5c89863b1c44?auto=format&fit=crop&w=1000&q=80" alt="건설 정밀 맵핑" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark-bg via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-4 left-4 px-3 py-1 bg-emerald-600/80 text-white text-xs font-bold rounded-lg backdrop-blur-md">건설/측량</span>
                        <div class="absolute bottom-4 left-4 right-4 flex justify-between items-center">
                            <span class="text-xs text-brand-accent font-mono"><i class="fa-solid fa-map"></i> RTK 3D Map</span>
                            <div class="w-10 h-10 rounded-full bg-brand-accent/90 text-dark-bg flex items-center justify-center font-bold group-hover:scale-110 transition-transform"><i class="fa-solid fa-play"></i></div>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-lg font-bold text-white mb-2 group-hover:text-brand-accent transition-colors">대형 물류단지 3D 정밀 맵핑</h4>
                        <p class="text-gray-400 text-xs line-clamp-2">RTK 정밀 수직촬영으로 10만평 부지 공정률 분석 3D 정밀 지도 완성</p>
                    </div>
                </div>

                <!-- Portfolio Item 5 -->
                <div class="portfolio-item glass-card rounded-3xl overflow-hidden group cursor-pointer" data-category="promo" data-title="제주 국립공원 및 해안 리조트 홍보" data-desc="자연경관과 리조트 전경을 아우르는 사계절 홍보영상 제작" data-equipment="DJI Mavic 3 Cine" data-date="2025년 10월" data-img="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?auto=format&fit=crop&w=1000&q=80">
                    <div class="relative h-60 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1512917774080-9991f1c4c750?auto=format&fit=crop&w=1000&q=80" alt="제주 리조트 홍보" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark-bg via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-4 left-4 px-3 py-1 bg-brand-500/80 text-white text-xs font-bold rounded-lg backdrop-blur-md">기업/홍보</span>
                        <div class="absolute bottom-4 left-4 right-4 flex justify-between items-center">
                            <span class="text-xs text-brand-accent font-mono"><i class="fa-solid fa-sun"></i> 5.1K AppleProRes</span>
                            <div class="w-10 h-10 rounded-full bg-brand-accent/90 text-dark-bg flex items-center justify-center font-bold group-hover:scale-110 transition-transform"><i class="fa-solid fa-play"></i></div>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-lg font-bold text-white mb-2 group-hover:text-brand-accent transition-colors">제주 리조트 및 자연경관 홍보</h4>
                        <p class="text-gray-400 text-xs line-clamp-2">일출/일몰의 환상적인 라이팅을 활용한 최고급 리조트 홍보 영상</p>
                    </div>
                </div>

                <!-- Portfolio Item 6 -->
                <div class="portfolio-item glass-card rounded-3xl overflow-hidden group cursor-pointer" data-category="fpv" data-title="플래그십 스토어 실내 원테이크 FPV 투어" data-desc="문 사이와 진열대 사이를 스무스하게 연결하는 실내 시네후프 투어" data-equipment="Custom CineWhoop 2.5인치" data-date="2025년 09월" data-img="https://images.unsplash.com/photo-1513694203232-719a280e022f?auto=format&fit=crop&w=1000&q=80">
                    <div class="relative h-60 overflow-hidden">
                        <img src="https://images.unsplash.com/photo-1513694203232-719a280e022f?auto=format&fit=crop&w=1000&q=80" alt="실내 FPV 원테이크" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-dark-bg via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-4 left-4 px-3 py-1 bg-brand-gold/80 text-dark-bg text-xs font-bold rounded-lg backdrop-blur-md">FPV 액션</span>
                        <div class="absolute bottom-4 left-4 right-4 flex justify-between items-center">
                            <span class="text-xs text-brand-accent font-mono"><i class="fa-solid fa-house"></i> Indoor CineWhoop</span>
                            <div class="w-10 h-10 rounded-full bg-brand-accent/90 text-dark-bg flex items-center justify-center font-bold group-hover:scale-110 transition-transform"><i class="fa-solid fa-play"></i></div>
                        </div>
                    </div>
                    <div class="p-6">
                        <h4 class="text-lg font-bold text-white mb-2 group-hover:text-brand-accent transition-colors">플래그십 스토어 실내 FPV 투어</h4>
                        <p class="text-gray-400 text-xs line-clamp-2">보호 가드가 장착된 미니 FPV 드론으로 안전하고 매끄러운 실내 동선 연출</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="fleet" class="py-24 bg-dark-card/30 border-t border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <h2 class="text-xs font-bold text-brand-accent uppercase tracking-widest mb-3">FLEET & GEARS</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-white">최첨단 플래그십 기종 라인업</p>
                <p class="text-gray-400 text-sm mt-3">촬영 환경 및 요청 성능에 최적화된 최신 드론 시스템을 보유하고 있습니다.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Fleet Item 1 -->
                <div class="glass-panel p-8 rounded-3xl border border-gray-800 hover:border-brand-accent/40 transition-all">
                    <div class="px-3 py-1 inline-block bg-brand-500/20 text-brand-accent text-xs font-bold rounded-full mb-4">시네마 플래그십</div>
                    <h3 class="text-2xl font-black text-white mb-2">DJI Inspire 3</h3>
                    <p class="text-xs text-gray-400 mb-6">최고급 영화/CF/드라마 메인 촬영용 듀얼 비행 드론</p>
                    
                    <ul class="space-y-3 text-xs text-gray-300 border-t border-gray-800/80 pt-4 mb-6">
                        <li class="flex justify-between"><span class="text-gray-500">카메라</span><span class="font-bold text-white">Zenmuse X9-8K Air</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">화질</span><span class="font-bold text-brand-accent">8K CinemaDNG / ProRes</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">특징</span><span class="font-bold text-white">듀얼 조종 / Waypoint Pro</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">최대속도</span><span class="font-bold text-white">94 km/h</span></li>
                    </ul>
                </div>

                <!-- Fleet Item 2 -->
                <div class="glass-panel p-8 rounded-3xl border border-gray-800 hover:border-brand-accent/40 transition-all">
                    <div class="px-3 py-1 inline-block bg-brand-gold/20 text-brand-gold text-xs font-bold rounded-full mb-4">기동성 & 기획 영상</div>
                    <h3 class="text-2xl font-black text-white mb-2">DJI Mavic 3 Cine</h3>
                    <p class="text-xs text-gray-400 mb-6">기업 홍보, 골프장, 분양 조망권 촬영 최적화</p>

                    <ul class="space-y-3 text-xs text-gray-300 border-t border-gray-800/80 pt-4 mb-6">
                        <li class="flex justify-between"><span class="text-gray-500">카메라</span><span class="font-bold text-white">4/3 CMOS Hasselblad</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">화질</span><span class="font-bold text-brand-accent">5.1K Apple ProRes 422 HQ</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">비행시간</span><span class="font-bold text-white">최대 46분</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">안전장치</span><span class="font-bold text-white">전방향 장애물 감지 센서</span></li>
                    </ul>
                </div>

                <!-- Fleet Item 3 -->
                <div class="glass-panel p-8 rounded-3xl border border-gray-800 hover:border-brand-accent/40 transition-all">
                    <div class="px-3 py-1 inline-block bg-cyan-500/20 text-cyan-400 text-xs font-bold rounded-full mb-4">커스텀 FPV & 맵핑</div>
                    <h3 class="text-2xl font-black text-white mb-2">Custom FPV & RTK Fleet</h3>
                    <p class="text-xs text-gray-400 mb-6">초고속 추적 비행 및 실내 시네후프 투어, RTK 정밀 측량</p>

                    <ul class="space-y-3 text-xs text-gray-300 border-t border-gray-800/80 pt-4 mb-6">
                        <li class="flex justify-between"><span class="text-gray-500">구성</span><span class="font-bold text-white">5인치 고속 FPV / 2.5인치 시네후프</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">화질</span><span class="font-bold text-brand-accent">4K 120fps / GP-Log</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">최대속도</span><span class="font-bold text-white">160 km/h 이상</span></li>
                        <li class="flex justify-between"><span class="text-gray-500">정밀도</span><span class="font-bold text-white">RTK 센티미터급 오차 보정</span></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="estimator" class="py-24 relative overflow-hidden">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="glass-panel p-8 sm:p-12 rounded-3xl border border-brand-accent/30 relative">
                <div class="text-center mb-10">
                    <span class="px-4 py-1.5 rounded-full bg-brand-500/20 text-brand-accent text-xs font-bold uppercase tracking-wider mb-3 inline-block">COST CALCULATOR</span>
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-white">실시간 촬영 견적 계산기</h2>
                    <p class="text-gray-400 text-sm mt-2">원하시는 조건과 옵션을 선택하시면 투명한 예상 견적을 즉시 확인하실 수 있습니다.</p>
                </div>

                <form id="calculator-form" class="space-y-8">
                    <!-- Step 1: Category -->
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-3"><i class="fa-solid fa-list-check text-brand-accent mr-2"></i> 1. 촬영 목적 및 분야 선택</label>
                        <div class="grid grid-cols-2 sm:grid-cols-4 gap-3">
                            <label class="cursor-pointer">
                                <input type="radio" name="project_type" value="400000" class="peer hidden" checked>
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-xl mb-1"><i class="fa-solid fa-building"></i></div>
                                    <div class="text-xs font-bold">기업/조망권 홍보</div>
                                </div>
                            </label>
                            <label class="cursor-pointer">
                                <input type="radio" name="project_type" value="700000" class="peer hidden">
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-xl mb-1"><i class="fa-solid fa-film"></i></div>
                                    <div class="text-xs font-bold">방송/영화/CF</div>
                                </div>
                            </label>
                            <label class="cursor-pointer">
                                <input type="radio" name="project_type" value="500000" class="peer hidden">
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-xl mb-1"><i class="fa-solid fa-bolt"></i></div>
                                    <div class="text-xs font-bold">FPV 액션 촬영</div>
                                </div>
                            </label>
                            <label class="cursor-pointer">
                                <input type="radio" name="project_type" value="600000" class="peer hidden">
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-xl mb-1"><i class="fa-solid fa-map-location-dot"></i></div>
                                    <div class="text-xs font-bold">건설/3D 맵핑</div>
                                </div>
                            </label>
                        </div>
                    </div>

                    <!-- Step 2: Time & Duration -->
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-3"><i class="fa-solid fa-clock text-brand-accent mr-2"></i> 2. 촬영 소요 시간</label>
                        <div class="grid grid-cols-1 sm:grid-cols-3 gap-3">
                            <label class="cursor-pointer">
                                <input type="radio" name="duration" value="1" class="peer hidden" checked>
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-sm font-bold">반일 촬영 (최대 4시간)</div>
                                    <div class="text-[11px] text-gray-500">기본 배터리 패키지</div>
                                </div>
                            </label>
                            <label class="cursor-pointer">
                                <input type="radio" name="duration" value="1.6" class="peer hidden">
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-sm font-bold">종일 촬영 (최대 8시간)</div>
                                    <div class="text-[11px] text-gray-500">풀데이 백업 모니터링 포함</div>
                                </div>
                            </label>
                            <label class="cursor-pointer">
                                <input type="radio" name="duration" value="3.0" class="peer hidden">
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-sm font-bold">2일 이상 프로젝트</div>
                                    <div class="text-[11px] text-gray-500">장기 할인 적용 메인 프로젝트</div>
                                </div>
                            </label>
                        </div>
                    </div>

                    <!-- Step 3: Video Gear Selection -->
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-3"><i class="fa-solid fa-camera text-brand-accent mr-2"></i> 3. 요청 기종 및 화질 사양</label>
                        <select id="gear_select" class="w-full bg-dark-card border border-gray-700 text-white rounded-xl p-4 text-sm focus:outline-none focus:border-brand-accent">
                            <option value="0">DJI Mavic 3 Cine (4K / 5.1K ProRes 지원 - 표준 추천)</option>
                            <option value="300000">DJI Inspire 3 (8K CinemaDNG / 듀얼 감독 조종 시스템 +30만원)</option>
                            <option value="200000">FPV 전용 고속 액션 / 시네후프 카메라 세트 (+20만원)</option>
                            <option value="250000">RTK 센티미터급 정밀 맵핑 드론 세트 (+25만원)</option>
                        </select>
                    </div>

                    <!-- Step 4: Editing Option -->
                    <div>
                        <label class="block text-sm font-bold text-gray-200 mb-3"><i class="fa-solid fa-sliders text-brand-accent mr-2"></i> 4. 후반 종합 편집 및 그래픽 처리</label>
                        <div class="grid grid-cols-1 sm:grid-cols-3 gap-3">
                            <label class="cursor-pointer">
                                <input type="radio" name="editing" value="0" class="peer hidden" checked>
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-sm font-bold">촬영 원본 전달 (Raw)</div>
                                    <div class="text-[11px] text-gray-500">현장 당일 컷 보관 및 전달</div>
                                </div>
                            </label>
                            <label class="cursor-pointer">
                                <input type="radio" name="editing" value="250000" class="peer hidden">
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-sm font-bold">4K 컷 편집 + BGM (+25만)</div>
                                    <div class="text-[11px] text-gray-500">기본 색보정 및 라이선스 음원</div>
                                </div>
                            </label>
                            <label class="cursor-pointer">
                                <input type="radio" name="editing" value="500000" class="peer hidden">
                                <div class="p-4 rounded-2xl glass-card text-center peer-checked:border-brand-accent peer-checked:bg-brand-500/20 peer-checked:text-white text-gray-400 hover:text-white transition-all">
                                    <div class="text-sm font-bold">풀패키지 종합편집 (+50만)</div>
                                    <div class="text-[11px] text-gray-500">CG 자막, 고급 컬러그레이딩, 성우</div>
                                </div>
                            </label>
                        </div>
                    </div>

                    <!-- Result Box -->
                    <div class="mt-8 p-6 rounded-2xl bg-gradient-to-r from-brand-900/60 to-dark-card border border-brand-500/40 flex flex-col sm:flex-row items-center justify-between gap-6">
                        <div>
                            <span class="text-xs text-gray-400 font-medium block">예상 견적 금액 (VAT 별도)</span>
                            <div class="text-3xl sm:text-4xl font-black text-brand-accent mt-1" id="calculated-price">400,000 원~</div>
                            <p class="text-[11px] text-gray-400 mt-1">* 촬영 위치, 허가 난이도, 출장비에 따라 최종 금액은 다소 차이가 있을 수 있습니다.</p>
                        </div>
                        <button type="button" id="apply-quote-btn" class="w-full sm:w-auto px-8 py-4 rounded-xl bg-gradient-to-r from-brand-500 to-brand-accent text-white font-bold text-sm hover:from-brand-600 hover:to-cyan-600 transition-all shadow-lg shadow-brand-500/30 whitespace-nowrap">
                            이 견적으로 상담 문의하기 <i class="fa-solid fa-arrow-right ml-2"></i>
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </section>

    <section class="py-20 bg-gradient-to-b from-dark-bg via-dark-card/50 to-dark-bg border-y border-gray-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                <div>
                    <span class="px-3 py-1 rounded-full bg-emerald-500/10 text-emerald-400 text-xs font-bold border border-emerald-500/20 inline-block mb-4">SAFETY FIRST</span>
                    <h2 class="text-3xl sm:text-4xl font-black text-white mb-6">합법적 승인 절차와<br />철저한 안전 관리 준수</h2>
                    <p class="text-gray-300 text-sm leading-relaxed mb-6">
                        FLY FILM은 대한민국 항공안전법을 철저히 준수합니다. 드론원스톱 민원서비스를 통해 비행승인 및 국방부 촬영허가를 승인받은 후 비행합니다.
                    </p>
                    <div class="space-y-4">
                        <div class="flex items-start gap-4">
                            <div class="w-10 h-10 rounded-xl bg-emerald-500/10 text-emerald-400 flex items-center justify-center shrink-0 mt-1"><i class="fa-solid fa-shield text-lg"></i></div>
                            <div>
                                <h4 class="text-white font-bold text-base">최대 1억원 영업배상 책임보험</h4>
                                <p class="text-xs text-gray-400">만일의 사태에 대비하여 모든 대형 비행 기체에 대해 대인/대물 배상 책임보험이 가입되어 있습니다.</p>
                            </div>
                        </div>
                        <div class="flex items-start gap-4">
                            <div class="w-10 h-10 rounded-xl bg-brand-500/10 text-brand-accent flex items-center justify-center shrink-0 mt-1"><i class="fa-solid fa-passport text-lg"></i></div>
                            <div>
                                <h4 class="text-white font-bold text-base">비행금지구역 / 보안구역 허가 사전대행</h4>
                                <p class="text-xs text-gray-400">서울 수도권(P73 구역 포함), 원전 주변, 군사시설 근접 구역의 승인 노하우를 보유하고 있습니다.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Process Steps -->
                <div class="glass-panel p-8 rounded-3xl border border-gray-800 space-y-6">
                    <h3 class="text-xl font-bold text-white mb-4 border-b border-gray-800 pb-3 flex items-center justify-between">
                        <span>촬영 진행 프로세스</span>
                        <span class="text-xs text-brand-accent font-normal">총 4단계 진행</span>
                    </h3>
                    
                    <div class="flex gap-4 items-start">
                        <div class="w-8 h-8 rounded-full bg-brand-500 text-white font-black text-xs flex items-center justify-center shrink-0">01</div>
                        <div>
                            <h5 class="text-sm font-bold text-white">상담 & 앵글 기획</h5>
                            <p class="text-xs text-gray-400">촬영 로케이션 검토, 연출 콘티 확인 및 예상 견적 확정</p>
                        </div>
                    </div>

                    <div class="flex gap-4 items-start">
                        <div class="w-8 h-8 rounded-full bg-brand-500 text-white font-black text-xs flex items-center justify-center shrink-0">02</div>
                        <div>
                            <h5 class="text-sm font-bold text-white">비행/촬영 행정 허가 신청</h5>
                            <p class="text-xs text-gray-400">드론원스톱을 통해 최소 3~7일 전 사전 승인 절차 완료</p>
                        </div>
                    </div>

                    <div class="flex gap-4 items-start">
                        <div class="w-8 h-8 rounded-full bg-brand-500 text-white font-black text-xs flex items-center justify-center shrink-0">03</div>
                        <div>
                            <h5 class="text-sm font-bold text-white">현장 비행 & 라이브 촬영</h5>
                            <p class="text-xs text-gray-400">안전 점검 후 실시간 모니터링 화면 공유를 통한 맞춤 촬영</p>
                        </div>
                    </div>

                    <div class="flex gap-4 items-start">
                        <div class="w-8 h-8 rounded-full bg-brand-accent text-dark-bg font-black text-xs flex items-center justify-center shrink-0">04</div>
                        <div>
                            <h5 class="text-sm font-bold text-white">데이터 보정 & 최종 전달</h5>
                            <p class="text-xs text-gray-400">RAW/ProRes 원본 또는 편집 및 색보정 거친 최종본 전달</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="faq" class="py-24 relative">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-xs font-bold text-brand-accent uppercase tracking-widest mb-3">FAQ</h2>
                <p class="text-3xl sm:text-4xl font-extrabold text-white">자주 묻는 질문</p>
            </div>

            <div class="space-y-4" id="faq-accordion">
                <!-- FAQ 1 -->
                <div class="glass-card rounded-2xl overflow-hidden border border-gray-800">
                    <button class="faq-btn w-full p-6 text-left flex justify-between items-center text-white font-bold text-base sm:text-lg focus:outline-none">
                        <span>Q. 비행 승인 및 촬영 허가는 얼마나 걸리나요?</span>
                        <i class="fa-solid fa-chevron-down text-brand-accent transition-transform duration-300"></i>
                    </button>
                    <div class="faq-answer hidden px-6 pb-6 text-sm text-gray-300 leading-relaxed border-t border-gray-800/50 pt-4">
                        일반 비행 구역의 경우 약 3~4일이 소요되며, 서울 도심지, P73 비행금지구역, 관제권, 군사보호구역의 경우 국방부 및 관련 기관 심사에 영업일 기준 7~14일 이상 소요될 수 있습니다. 중요한 촬영 일정은 최소 1~2주 전 문의 주시는 것이 가장 좋습니다.
                    </div>
                </div>

                <!-- FAQ 2 -->
                <div class="glass-card rounded-2xl overflow-hidden border border-gray-800">
                    <button class="faq-btn w-full p-6 text-left flex justify-between items-center text-white font-bold text-base sm:text-lg focus:outline-none">
                        <span>Q. 우천이나 강풍 등 기상 악화 시에는 어떻게 진행되나요?</span>
                        <i class="fa-solid fa-chevron-down text-brand-accent transition-transform duration-300"></i>
                    </button>
                    <div class="faq-answer hidden px-6 pb-6 text-sm text-gray-300 leading-relaxed border-t border-gray-800/50 pt-4">
                        드론 비행 특성상 우천, 강풍(10m/s 이상), 짙은 안개 시 기체 안전 및 화질 확보를 위해 비행이 불가능합니다. 기상 악화로 인한 지연 시 고객님과 협의하여 위약금 없이 촬영 일정을 무료 재조율해 드립니다.
                    </div>
                </div>

                <!-- FAQ 3 -->
                <div class="glass-card rounded-2xl overflow-hidden border border-gray-800">
                    <button class="faq-btn w-full p-6 text-left flex justify-between items-center text-white font-bold text-base sm:text-lg focus:outline-none">
                        <span>Q. 전국 출장 촬영도 가능한가요?</span>
                        <i class="fa-solid fa-chevron-down text-brand-accent transition-transform duration-300"></i>
                    </button>
                    <div class="faq-answer hidden px-6 pb-6 text-sm text-gray-300 leading-relaxed border-t border-gray-800/50 pt-4">
                        네, FLY FILM은 수도권뿐만 아니라 제주도 및 도서 지역을 포함한 전국 어디든 출장 촬영이 가능합니다. (수도권 외 지역은 정산 시 실비 기준의 유류비 및 출장비가 반영됩니다.)
                    </div>
                </div>

                <!-- FAQ 4 -->
                <div class="glass-card rounded-2xl overflow-hidden border border-gray-800">
                    <button class="faq-btn w-full p-6 text-left flex justify-between items-center text-white font-bold text-base sm:text-lg focus:outline-none">
                        <span>Q. 촬영 현장에서 실시간으로 영상을 확인할 수 있나요?</span>
                        <i class="fa-solid fa-chevron-down text-brand-accent transition-transform duration-300"></i>
                    </button>
                    <div class="faq-answer hidden px-6 pb-6 text-sm text-gray-300 leading-relaxed border-t border-gray-800/50 pt-4">
                        네, 가능합니다. 고화질 현장 필드 모니터(High-Brightness Monitor)를 기본 제공하여, 클라이언트와 감독님이 실시간 구도와 앵글을 함께 보며 피드백을 주고받으실 수 있습니다.
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="py-24 bg-dark-card/40 border-t border-gray-800 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
                <!-- Info Left -->
                <div>
                    <h2 class="text-xs font-bold text-brand-accent uppercase tracking-widest mb-3">CONTACT US</h2>
                    <p class="text-3xl sm:text-4xl font-black text-white mb-6">스케줄 및 촬영 문의</p>
                    <p class="text-gray-300 text-sm leading-relaxed mb-8">
                        프로젝트의 목적, 희망 날짜, 촬영 장소를 남겨주시면 담당 감독이 확인 후 빠르게 상세 상담 및 맞춤 견적서를 안내해 드립니다.
                    </p>

                    <div class="space-y-6">
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 rounded-2xl bg-brand-500/10 border border-brand-500/30 flex items-center justify-center text-brand-accent text-xl">
                                <i class="fa-solid fa-phone"></i>
                            </div>
                            <div>
                                <span class="text-xs text-gray-400 block">직통 대표 전화</span>
                                <a href="tel:01098765432" class="text-lg font-bold text-white hover:text-brand-accent">02-1234-5678 / 010-9876-5432</a>
                            </div>
                        </div>

                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 rounded-2xl bg-brand-accent/10 border border-brand-accent/30 flex items-center justify-center text-brand-accent text-xl">
                                <i class="fa-solid fa-envelope"></i>
                            </div>
                            <div>
                                <span class="text-xs text-gray-400 block">이메일 문의</span>
                                <a href="mailto:contact@flyfilm.co.kr" class="text-lg font-bold text-white hover:text-brand-accent">contact@flyfilm.co.kr</a>
                            </div>
                        </div>

                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 rounded-2xl bg-brand-gold/10 border border-brand-gold/30 flex items-center justify-center text-brand-gold text-xl">
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <div>
                                <span class="text-xs text-gray-400 block">스튜디오 위치</span>
                                <span class="text-base font-bold text-white">서울특별시 마포구 월드컵북로 123 FLY FILM 스튜디오</span>
                            </div>
                        </div>
                    </div>

                    <!-- KakaoTalk Channel Banner Button -->
                    <div class="mt-8 p-6 rounded-2xl bg-[#FEE500]/10 border border-[#FEE500]/30 flex items-center justify-between">
                        <div class="flex items-center gap-3">
                            <i class="fa-solid fa-comment text-2xl text-[#FEE500]"></i>
                            <div>
                                <h4 class="text-white font-bold text-sm">카카오톡 실시간 1:1 상담</h4>
                                <p class="text-xs text-gray-400">카카오톡 채널 ID: @FLYFILM_DRONE</p>
                            </div>
                        </div>
                        <a href="https://pf.kakao.com" target="_blank" rel="noopener noreferrer" onclick="showToast('카카오톡 상담 채널로 연결을 시도합니다.')" class="px-4 py-2 rounded-xl bg-[#FEE500] text-dark-bg font-bold text-xs hover:bg-yellow-400 transition-colors">
                            상담 시작
                        </a>
                    </div>
                </div>

                <!-- Form Right -->
                <div class="glass-panel p-8 sm:p-10 rounded-3xl border border-gray-800">
                    <form id="contact-form" class="space-y-5">
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-semibold text-gray-300 mb-2">성함 / 담당자명 *</label>
                                <input type="text" id="form-name" required placeholder="홍길동 팀장" class="w-full bg-dark-card border border-gray-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-accent">
                            </div>
                            <div>
                                <label class="block text-xs font-semibold text-gray-300 mb-2">연락처 *</label>
                                <input type="tel" id="form-phone" required placeholder="010-0000-0000" class="w-full bg-dark-card border border-gray-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-accent">
                            </div>
                        </div>

                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-semibold text-gray-300 mb-2">이메일 주소</label>
                                <input type="email" id="form-email" placeholder="example@company.com" class="w-full bg-dark-card border border-gray-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-accent">
                            </div>
                            <div>
                                <label class="block text-xs font-semibold text-gray-300 mb-2">희망 촬영 일정</label>
                                <input type="date" id="form-date" class="w-full bg-dark-card border border-gray-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-accent">
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs font-semibold text-gray-300 mb-2">촬영 대상 / 위치 및 지역</label>
                            <input type="text" id="form-location" placeholder="예: 서울 마포구 상암동 아파트 단지 전경" class="w-full bg-dark-card border border-gray-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-accent">
                        </div>

                        <div>
                            <label class="block text-xs font-semibold text-gray-300 mb-2">상세 요구 사항 및 질문</label>
                            <textarea id="form-message" rows="4" placeholder="촬영 목적, 기종 요청, 편집 여부 등 전달주실 세부 내용을 적어주세요." class="w-full bg-dark-card border border-gray-700 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-accent"></textarea>
                        </div>

                        <button type="submit" class="w-full py-4 rounded-xl bg-gradient-to-r from-brand-500 to-brand-accent hover:from-brand-600 hover:to-cyan-600 text-white font-bold text-base transition-all shadow-lg shadow-brand-500/30 flex items-center justify-center gap-2">
                            <i class="fa-solid fa-paper-plane"></i>
                            <span>촬영 문의 접수하기</span>
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-12 bg-dark-bg border-t border-gray-800 text-gray-500 text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center gap-6 mb-8">
                <div class="flex items-center gap-3">
                    <div class="w-8 h-8 rounded-lg bg-brand-500 flex items-center justify-center text-white font-bold">
                        <i class="fa-solid fa-plane-up"></i>
                    </div>
                    <span class="text-xl font-black text-white">FLY FILM</span>
                </div>
                <div class="flex space-x-6 text-gray-400 text-lg">
                    <a href="https://youtube.com" target="_blank" rel="noopener noreferrer" class="hover:text-brand-accent" aria-label="유튜브"><i class="fa-brands fa-youtube"></i></a>
                    <a href="https://instagram.com" target="_blank" rel="noopener noreferrer" class="hover:text-brand-accent" aria-label="인스타그램"><i class="fa-brands fa-instagram"></i></a>
                    <a href="https://blog.naver.com" target="_blank" rel="noopener noreferrer" class="hover:text-brand-accent" aria-label="블로그"><i class="fa-solid fa-blog"></i></a>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-4 border-t border-gray-800/60 pt-6">
                <div>
                    <p class="mb-1">플라이필름 | 대표자: 여상민 | 사업자등록번호: 223-09-92751</p>
                    <p class="mb-1">초경량비행장치 사용사업 등록번호: 제 2024-수도권-0000호</p>
                    <p>주소: 경기도 부천시 오정구 성오로</p>
                </div>
                <div class="md:text-right">
                    <p class="mb-1">통신판매업신고: 제 2024-서울마포-0000호 | 영업배상책임보험: KB손해보험 가입</p>
                    <p>© 2026 FLY FILM. All Rights Reserved.</p>
                </div>
            </div>
        </div>
    </footer>

    <!-- Lightbox Modal for Portfolio Details -->
    <div id="portfolio-modal" class="fixed inset-0 z-50 hidden items-center justify-center p-4 bg-black/80 backdrop-blur-md">
        <div class="glass-panel w-full max-w-3xl rounded-3xl overflow-hidden border border-brand-accent/40 relative">
            <button id="close-modal" class="absolute top-4 right-4 w-10 h-10 rounded-full bg-dark-bg/80 text-white flex items-center justify-center hover:bg-brand-500 transition-colors z-10">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>
            <div id="modal-img-container" class="relative h-72 sm:h-96 w-full bg-black">
                <img id="modal-img" src="" alt="Portfolio Preview" class="w-full h-full object-cover">
                <div class="absolute inset-0 bg-black/40 flex items-center justify-center">
                    <div class="w-16 h-16 rounded-full bg-brand-accent/90 text-dark-bg text-2xl font-bold flex items-center justify-center shadow-2xl cursor-pointer hover:scale-110 transition-transform" onclick="showToast('샘플 영상 스트리밍을 재생합니다.')">
                        <i class="fa-solid fa-play ml-1"></i>
                    </div>
                </div>
            </div>
            <div class="p-6 sm:p-8">
                <div class="flex items-center gap-3 mb-3">
                    <span id="modal-category" class="px-3 py-1 bg-brand-500/20 text-brand-accent text-xs font-bold rounded-lg border border-brand-500/30">카테고리</span>
                    <span id="modal-date" class="text-xs text-gray-400">촬영일자</span>
                </div>
                <h3 id="modal-title" class="text-2xl font-black text-white mb-3">프로젝트 제목</h3>
                <p id="modal-desc" class="text-gray-300 text-sm leading-relaxed mb-6">프로젝트 세부 설명</p>
                
                <div class="flex flex-wrap items-center justify-between gap-4 border-t border-gray-800 pt-4">
                    <div class="text-xs text-gray-400">
                        <span>투입 장비: </span><strong id="modal-equipment" class="text-white">DJI Inspire 3</strong>
                    </div>
                    <a href="#contact" onclick="closePortfolioModal()" class="px-5 py-2.5 rounded-xl bg-brand-500 text-white text-xs font-bold hover:bg-brand-600 transition-colors">
                        비슷한 프로젝트 견적 문의
                    </a>
                </div>
            </div>
        </div>
    </div>

    <!-- Toast Notification Container -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 hidden glass-panel px-6 py-4 rounded-2xl border border-brand-accent text-white font-medium text-sm shadow-2xl flex items-center gap-3">
        <i class="fa-solid fa-circle-check text-brand-accent text-lg"></i>
        <span id="toast-message">메시지 내용</span>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const canvas = document.getElementById('hero-canvas');
            if (canvas) {
                const ctx = canvas.getContext('2d');
                let width = canvas.width = window.innerWidth;
                let height = canvas.height = window.innerHeight;

                window.addEventListener('resize', () => {
                    width = canvas.width = window.innerWidth;
                    height = canvas.height = window.innerHeight;
                });

                // Floating particles
                const particles = Array.from({ length: 45 }, () => ({
                    x: Math.random() * width,
                    y: Math.random() * height,
                    radius: Math.random() * 2 + 0.5,
                    vx: (Math.random() - 0.5) * 0.4,
                    vy: (Math.random() - 0.5) * 0.4,
                    alpha: Math.random() * 0.6 + 0.2
                }));

                function animateCanvas() {
                    ctx.clearRect(0, 0, width, height);

                    // Grid Lines
                    ctx.strokeStyle = 'rgba(6, 182, 212, 0.03)';
                    ctx.lineWidth = 1;
                    const gridSize = 60;
                    for (let x = 0; x < width; x += gridSize) {
                        ctx.beginPath();
                        ctx.moveTo(x, 0);
                        ctx.lineTo(x, height);
                        ctx.stroke();
                    }
                    for (let y = 0; y < height; y += gridSize) {
                        ctx.beginPath();
                        ctx.moveTo(0, y);
                        ctx.lineTo(width, y);
                        ctx.stroke();
                    }

                    // Particles
                    particles.forEach(p => {
                        p.x += p.vx;
                        p.y += p.vy;

                        if (p.x < 0) p.x = width;
                        if (p.x > width) p.x = 0;
                        if (p.y < 0) p.y = height;
                        if (p.y > height) p.y = 0;

                        ctx.fillStyle = `rgba(56, 189, 248, ${p.alpha})`;
                        ctx.beginPath();
                        ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
                        ctx.fill();
                    });

                    requestAnimationFrame(animateCanvas);
                }
                animateCanvas();
            }

            const mobileBtn = document.getElementById('mobile-menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');
            if (mobileBtn && mobileMenu) {
                mobileBtn.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                });
                document.querySelectorAll('.mobile-link').forEach(link => {
                    link.addEventListener('click', () => mobileMenu.classList.add('hidden'));
                });
            }

            const counters = document.querySelectorAll('.counter');
            let hasAnimated = false;
            const animateCounters = () => {
                counters.forEach(counter => {
                    const target = +counter.getAttribute('data-target');
                    const speed = 100;
                    const updateCount = () => {
                        const count = +counter.innerText;
                        const inc = Math.ceil(target / speed);
                        if (count < target) {
                            counter.innerText = count + inc;
                            setTimeout(updateCount, 20);
                        } else {
                            counter.innerText = target;
                        }
                    };
                    updateCount();
                });
            };

            window.addEventListener('scroll', () => {
                const section = document.getElementById('about');
                if (section && !hasAnimated) {
                    const rect = section.getBoundingClientRect();
                    if (rect.top <= window.innerHeight) {
                        animateCounters();
                        hasAnimated = true;
                    }
                }
            });

            const filterBtns = document.querySelectorAll('.portfolio-filter-btn');
            const portfolioItems = document.querySelectorAll('.portfolio-item');

            filterBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    filterBtns.forEach(b => {
                        b.classList.remove('bg-gradient-to-r', 'from-brand-500', 'to-brand-accent', 'text-white', 'shadow-md');
                        b.classList.add('glass-card', 'text-gray-300');
                    });
                    btn.classList.add('bg-gradient-to-r', 'from-brand-500', 'to-brand-accent', 'text-white', 'shadow-md');
                    btn.classList.remove('glass-card', 'text-gray-300');

                    const filter = btn.getAttribute('data-filter');
                    portfolioItems.forEach(item => {
                        if (filter === 'all' || item.getAttribute('data-category') === filter) {
                            item.style.display = 'block';
                        } else {
                            item.style.display = 'none';
                        }
                    });
                });
            });

            // Modal Logic
            const modal = document.getElementById('portfolio-modal');
            const closeModalBtn = document.getElementById('close-modal');

            portfolioItems.forEach(item => {
                item.addEventListener('click', () => {
                    document.getElementById('modal-title').innerText = item.getAttribute('data-title');
                    document.getElementById('modal-desc').innerText = item.getAttribute('data-desc');
                    document.getElementById('modal-equipment').innerText = item.getAttribute('data-equipment');
                    document.getElementById('modal-date').innerText = item.getAttribute('data-date');
                    document.getElementById('modal-img').src = item.getAttribute('data-img');
                    
                    const catMap = {
                        'promo': '기업/홍보',
                        'cinema': '방송/영화/CF',
                        'fpv': 'FPV 액션',
                        'survey': '건설/측량'
                    };
                    document.getElementById('modal-category').innerText = catMap[item.getAttribute('data-category')] || '항공 촬영';
                    modal.classList.remove('hidden');
                    modal.classList.add('flex');
                });
            });

            window.closePortfolioModal = () => {
                modal.classList.add('hidden');
                modal.classList.remove('flex');
            };

            if (closeModalBtn) {
                closeModalBtn.addEventListener('click', closePortfolioModal);
            }

            modal.addEventListener('click', (e) => {
                if (e.target === modal) closePortfolioModal();
            });

            const calcForm = document.getElementById('calculator-form');
            const priceDisplay = document.getElementById('calculated-price');

            function calculatePrice() {
                const projectType = parseInt(document.querySelector('input[name="project_type"]:checked').value);
                const durationMult = parseFloat(document.querySelector('input[name="duration"]:checked').value);
                const gearCost = parseInt(document.getElementById('gear_select').value);
                const editCost = parseInt(document.querySelector('input[name="editing"]:checked').value);

                const total = Math.round((projectType * durationMult) + gearCost + editCost);
                priceDisplay.innerText = total.toLocaleString('ko-KR') + ' 원~';
            }

            if (calcForm) {
                calcForm.addEventListener('change', calculatePrice);
            }

            // Apply Quote Button Click
            const applyQuoteBtn = document.getElementById('apply-quote-btn');
            if (applyQuoteBtn) {
                applyQuoteBtn.addEventListener('click', () => {
                    const priceText = priceDisplay.innerText;
                    const messageBox = document.getElementById('form-message');
                    if (messageBox) {
                        messageBox.value = `[실시간 견적 산출 결과]\n- 예상 산출 금액: ${priceText}\n- 세부 요구사항: `;
                    }
                    showToast('산출된 견적이 문의폼에 등록되었습니다. 제출을 완성을 위해 양식을 채워주세요!');
                    document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
                });
            }

            const faqBtns = document.querySelectorAll('.faq-btn');
            faqBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    const answer = btn.nextElementSibling;
                    const icon = btn.querySelector('i');
                    const isHidden = answer.classList.contains('hidden');

                    document.querySelectorAll('.faq-answer').forEach(a => a.classList.add('hidden'));
                    document.querySelectorAll('.faq-btn i').forEach(i => i.classList.remove('rotate-180'));

                    if (isHidden) {
                        answer.classList.remove('hidden');
                        icon.classList.add('rotate-180');
                    }
                });
            });

            // Contact Form
            const contactForm = document.getElementById('contact-form');
            if (contactForm) {
                contactForm.addEventListener('submit', (e) => {
                    e.preventDefault();
                    const name = document.getElementById('form-name').value;
                    showToast(`${name}님, 촬영 문의가 성공적으로 접수되었습니다. 담당 감독이 확인 후 즉시 연락드리겠습니다!`);
                    contactForm.reset();
                });
            }
        });

        // Toast Notification Helper
        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toast-message');
            if (toast && toastMsg) {
                toastMsg.innerText = message;
                toast.classList.remove('hidden');
                setTimeout(() => {
                    toast.classList.add('hidden');
                }, 4000);
            }
        }
    </script>
</body>
</html>

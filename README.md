<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hub Interactivo de Ciberseguridad 2024-2025</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;800&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                        mono: ['JetBrains Mono', 'monospace'],
                    },
                    fontSize: {
                        // Escala aumentada +0.5rem sobre base estándar
                        'xs':   ['1rem',    { lineHeight: '1.5rem' }],
                        'sm':   ['1.125rem',{ lineHeight: '1.75rem' }],
                        'base': ['1.25rem', { lineHeight: '1.875rem' }],
                        'lg':   ['1.5rem',  { lineHeight: '2rem' }],
                        'xl':   ['1.75rem', { lineHeight: '2.25rem' }],
                        '2xl':  ['2.25rem', { lineHeight: '2.75rem' }],
                        '3xl':  ['2.75rem', { lineHeight: '3.25rem' }],
                        '4xl':  ['3.5rem',  { lineHeight: '4rem' }],
                        '5xl':  ['4.5rem',  { lineHeight: '5rem' }],
                        '6xl':  ['5.5rem',  { lineHeight: '6rem' }],
                        '7xl':  ['6.5rem',  { lineHeight: '7rem' }],
                        '8xl':  ['8rem',    { lineHeight: '8.5rem' }],
                        '9xl':  ['10rem',   { lineHeight: '10.5rem' }],
                    },
                    colors: {
                        cyber: {
                            dark: '#0a0f1d',
                            card: '#111827',
                            border: '#1f2937',
                            accent: '#06b6d4',
                            blue: '#3b82f6',
                            red: '#ef4444',
                            purple: '#8b5cf6',
                            emerald: '#10b981',
                            amber: '#f59e0b'
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #060913;
            color: #e2e8f0;
            font-family: 'Plus Jakarta Sans', sans-serif;
            font-size: 1.125rem;
        }
        /* Títulos duplicados */
        h1 { font-size: 3.5rem; line-height: 4rem; }
        h2 { font-size: 2.5rem; line-height: 3rem; }
        h3 { font-size: 1.75rem; line-height: 2.25rem; }
        h4 { font-size: 1.5rem; line-height: 2rem; }

        .glow-effect {
            box-shadow: 0 0 25px -5px rgba(6, 182, 212, 0.15);
        }
        .glow-effect-red {
            box-shadow: 0 0 25px -5px rgba(239, 68, 68, 0.15);
        }
        .glow-effect-purple {
            box-shadow: 0 0 25px -5px rgba(139, 92, 246, 0.15);
        }
        .custom-scrollbar::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #0f172a;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #334155;
            border-radius: 4px;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover {
            background: #475569;
        }
        /* Iconos decorativos de fondo */
        .bg-icon {
            position: absolute;
            opacity: 0.04;
            pointer-events: none;
        }
        /* Animaciones sutiles */
        @keyframes pulse-slow {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.6; }
        }
        .animate-pulse-slow {
            animation: pulse-slow 3s ease-in-out infinite;
        }
        /* Tarjeta hover */
        .card-hover {
            transition: all 0.3s ease;
        }
        .card-hover:hover {
            transform: translateY(-4px);
        }
        /* Glosario card */
        .glossary-card {
            transition: all 0.25s ease;
        }
        .glossary-card:hover {
            border-color: rgba(6, 182, 212, 0.5);
            background-color: rgba(15, 23, 42, 0.9);
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-cyan-500 selection:text-black">

    <!-- TOP HEADER / NAVBAR -->
    <header class="border-b border-gray-800 bg-slate-950/80 backdrop-blur-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col md:flex-row items-center justify-between gap-4">
            <div class="flex items-center space-x-3">
                <div class="p-3 bg-gradient-to-tr from-cyan-600 to-blue-600 rounded-xl shadow-lg shadow-cyan-500/20">
                    <i class="fa-solid fa-shield-halved text-4xl text-white"></i>
                </div>
                <div>
                    <h1 class="font-extrabold tracking-tight bg-gradient-to-r from-cyan-400 via-sky-300 to-indigo-400 bg-clip-text text-transparent">
                        CIBERSEGURIDAD 2024-2025
                    </h1>
                    <p class="text-base text-slate-400 font-mono">FRAMEWORKS & ECOSYSTEM HUB</p>
                </div>
            </div>

            <!-- SEARCH / QUICK STATS -->
            <div class="flex items-center gap-3 w-full md:w-auto">
                <div class="relative w-full md:w-80">
                    <i class="fa-solid fa-magnifying-glass absolute left-3 top-1/2 -translate-y-1/2 text-slate-500 text-sm"></i>
                    <input type="text" id="globalSearch" placeholder="Buscar cert, rol, marco..." 
                        class="w-full bg-slate-900 border border-slate-700/60 rounded-lg pl-10 pr-3 py-2 text-sm text-slate-200 focus:outline-none focus:border-cyan-500 transition-all font-mono">
                </div>
                <span class="hidden lg:inline-flex items-center px-3 py-1.5 rounded-full text-sm font-medium bg-cyan-950/80 text-cyan-400 border border-cyan-800/50">
                    <span class="w-2.5 h-2.5 rounded-full bg-cyan-400 animate-ping mr-2"></span> NIST SP 800-181r1
                </span>
            </div>
        </div>

        <!-- MAIN NAVIGATION TABS -->
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex space-x-1 overflow-x-auto custom-scrollbar border-t border-slate-800/50 pt-2 pb-2 text-base font-semibold">
            <button onclick="switchTab('overview')" id="tab-overview" class="tab-btn active px-5 py-2.5 rounded-lg flex items-center gap-2 transition-all text-cyan-400 bg-slate-800/80 border border-cyan-500/30 whitespace-nowrap">
                <i class="fa-solid fa-chart-pie"></i> Vista General
            </button>
            <button onclick="switchTab('domains')" id="tab-domains" class="tab-btn px-5 py-2.5 rounded-lg flex items-center gap-2 transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/50 whitespace-nowrap">
                <i class="fa-solid fa-sitemap"></i> Dominios
            </button>
            <button onclick="switchTab('certs')" id="tab-certs" class="tab-btn px-5 py-2.5 rounded-lg flex items-center gap-2 transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/50 whitespace-nowrap">
                <i class="fa-solid fa-certificate"></i> Certificaciones
            </button>
            <button onclick="switchTab('emerging')" id="tab-emerging" class="tab-btn px-5 py-2.5 rounded-lg flex items-center gap-2 transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/50 whitespace-nowrap">
                <i class="fa-solid fa-microchip"></i> Nichos
            </button>
            <button onclick="switchTab('glossary')" id="tab-glossary" class="tab-btn px-5 py-2.5 rounded-lg flex items-center gap-2 transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/50 whitespace-nowrap">
                <i class="fa-solid fa-book-open"></i> Glosario
            </button>
            <button onclick="switchTab('trends')" id="tab-trends" class="tab-btn px-5 py-2.5 rounded-lg flex items-center gap-2 transition-all text-slate-400 hover:text-slate-200 hover:bg-slate-800/50 whitespace-nowrap">
                <i class="fa-solid fa-bolt"></i> Tendencias
            </button>
        </nav>
    </header>

    <!-- MAIN CONTAINER -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10 flex-1 w-full">

        <!-- ==================== TAB 1: OVERVIEW ==================== -->
        <section id="content-overview" class="tab-content space-y-10">
            <!-- INTRO BANNER -->
            <div class="relative bg-gradient-to-r from-slate-900 via-cyan-950/20 to-slate-900 border border-cyan-500/20 rounded-2xl p-8 lg:p-12 overflow-hidden glow-effect">
                <div class="max-w-4xl relative z-10 space-y-4">
                    <span class="px-4 py-1.5 bg-cyan-500/10 text-cyan-400 rounded-full text-base font-mono font-semibold border border-cyan-500/20">
                        <i class="fa-solid fa-graduation-cap mr-2"></i>MARCO ACADÉMICO & PROFESIONAL
                    </span>
                    <h2 class="font-bold text-white tracking-tight">
                        Estructura e Integración Funcional de la Ciberseguridad
                    </h2>
                    <p class="text-slate-300 leading-relaxed">
                        La ciberseguridad contemporánea se articula en torno a dominios especializados que responden a necesidades operativas, estratégicas y regulatorias. Integra marcos internacionales como 
                        <span class="text-cyan-300 font-mono">NIST NICE (SP 800-181r1)</span>, <span class="text-cyan-300 font-mono">MITRE ATT&CK</span>, <span class="text-cyan-300 font-mono">NIST CSF 2.0</span>, <span class="text-cyan-300 font-mono">ISO/IEC 27001</span> y <span class="text-cyan-300 font-mono">CIS Controls v8</span>.
                    </p>
                </div>
                <i class="fa-solid fa-shield-virus absolute -right-10 -bottom-10 text-9xl text-cyan-500/5 pointer-events-none"></i>
            </div>

            <!-- DOMAIN SUMMARY CARDS GRID -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Blue Team -->
                <div onclick="goToDomain('blue')" class="card-hover cursor-pointer group p-6 bg-slate-900/80 border border-slate-800 hover:border-blue-500/50 rounded-xl transition-all duration-300 glow-effect relative overflow-hidden">
                    <i class="fa-solid fa-shield-halved bg-icon text-8xl right-2 bottom-2 text-blue-500"></i>
                    <div class="flex items-center justify-between mb-4 relative z-10">
                        <span class="p-3 bg-blue-500/10 text-blue-400 rounded-lg group-hover:bg-blue-500 group-hover:text-white transition-all">
                            <i class="fa-solid fa-user-shield text-2xl"></i>
                        </span>
                        <span class="text-sm font-mono text-slate-500">DOMINIO 01</span>
                    </div>
                    <h3 class="font-bold text-white group-hover:text-blue-400 transition-colors relative z-10">Defensa & Operaciones (Blue)</h3>
                    <p class="text-slate-400 mt-3 relative z-10">Monitoreo, detección, triage y respuesta activa ante incidentes en infraestructuras corporativas.</p>
                    <div class="mt-5 pt-4 border-t border-slate-800/80 flex items-center justify-between text-sm font-mono text-slate-400 relative z-10">
                        <span><i class="fa-solid fa-layer-group mr-1"></i>3 Niveles</span>
                        <span class="text-blue-400 group-hover:translate-x-1 transition-transform">Explorar <i class="fa-solid fa-arrow-right"></i></span>
                    </div>
                </div>

                <!-- Red Team -->
                <div onclick="goToDomain('red')" class="card-hover cursor-pointer group p-6 bg-slate-900/80 border border-slate-800 hover:border-red-500/50 rounded-xl transition-all duration-300 glow-effect-red relative overflow-hidden">
                    <i class="fa-solid fa-skull-crossbones bg-icon text-8xl right-2 bottom-2 text-red-500"></i>
                    <div class="flex items-center justify-between mb-4 relative z-10">
                        <span class="p-3 bg-red-500/10 text-red-400 rounded-lg group-hover:bg-red-500 group-hover:text-white transition-all">
                            <i class="fa-solid fa-skull text-2xl"></i>
                        </span>
                        <span class="text-sm font-mono text-slate-500">DOMINIO 02</span>
                    </div>
                    <h3 class="font-bold text-white group-hover:text-red-400 transition-colors relative z-10">Seguridad Ofensiva (Red)</h3>
                    <p class="text-slate-400 mt-3 relative z-10">Simulación de ataques, pentesting manual, análisis de vulnerabilidades y emulación de adversarios APT.</p>
                    <div class="mt-5 pt-4 border-t border-slate-800/80 flex items-center justify-between text-sm font-mono text-slate-400 relative z-10">
                        <span><i class="fa-solid fa-layer-group mr-1"></i>3 Niveles</span>
                        <span class="text-red-400 group-hover:translate-x-1 transition-transform">Explorar <i class="fa-solid fa-arrow-right"></i></span>
                    </div>
                </div>

                <!-- DFIR -->
                <div onclick="goToDomain('dfir')" class="card-hover cursor-pointer group p-6 bg-slate-900/80 border border-slate-800 hover:border-amber-500/50 rounded-xl transition-all duration-300 relative overflow-hidden">
                    <i class="fa-solid fa-fingerprint bg-icon text-8xl right-2 bottom-2 text-amber-500"></i>
                    <div class="flex items-center justify-between mb-4 relative z-10">
                        <span class="p-3 bg-amber-500/10 text-amber-400 rounded-lg group-hover:bg-amber-500 group-hover:text-white transition-all">
                            <i class="fa-solid fa-magnifying-glass-location text-2xl"></i>
                        </span>
                        <span class="text-sm font-mono text-slate-500">DOMINIO 03</span>
                    </div>
                    <h3 class="font-bold text-white group-hover:text-amber-400 transition-colors relative z-10">Forense Digital (DFIR)</h3>
                    <p class="text-slate-400 mt-3 relative z-10">Recolección de evidencia, análisis de artefactos, ingeniería inversa de malware y cadena de custodia.</p>
                    <div class="mt-5 pt-4 border-t border-slate-800/80 flex items-center justify-between text-sm font-mono text-slate-400 relative z-10">
                        <span><i class="fa-solid fa-layer-group mr-1"></i>3 Niveles</span>
                        <span class="text-amber-400 group-hover:translate-x-1 transition-transform">Explorar <i class="fa-solid fa-arrow-right"></i></span>
                    </div>
                </div>

                <!-- Purple / Build -->
                <div onclick="goToDomain('purple')" class="card-hover cursor-pointer group p-6 bg-slate-900/80 border border-slate-800 hover:border-purple-500/50 rounded-xl transition-all duration-300 glow-effect-purple relative overflow-hidden">
                    <i class="fa-solid fa-cubes bg-icon text-8xl right-2 bottom-2 text-purple-500"></i>
                    <div class="flex items-center justify-between mb-4 relative z-10">
                        <span class="p-3 bg-purple-500/10 text-purple-400 rounded-lg group-hover:bg-purple-500 group-hover:text-white transition-all">
                            <i class="fa-solid fa-cubes text-2xl"></i>
                        </span>
                        <span class="text-sm font-mono text-slate-500">DOMINIO 04</span>
                    </div>
                    <h3 class="font-bold text-white group-hover:text-purple-400 transition-colors relative z-10">Arquitectura & Build (Purple)</h3>
                    <p class="text-slate-400 mt-3 relative z-10">Diseño y blindaje de infraestructura, arquitectura Zero Trust (NIST SP 800-207), SABSA y TOGAF.</p>
                    <div class="mt-5 pt-4 border-t border-slate-800/80 flex items-center justify-between text-sm font-mono text-slate-400 relative z-10">
                        <span><i class="fa-solid fa-layer-group mr-1"></i>3 Niveles</span>
                        <span class="text-purple-400 group-hover:translate-x-1 transition-transform">Explorar <i class="fa-solid fa-arrow-right"></i></span>
                    </div>
                </div>

                <!-- Cloud & DevSecOps -->
                <div onclick="goToDomain('cloud')" class="card-hover cursor-pointer group p-6 bg-slate-900/80 border border-slate-800 hover:border-sky-500/50 rounded-xl transition-all duration-300 relative overflow-hidden">
                    <i class="fa-solid fa-cloud bg-icon text-8xl right-2 bottom-2 text-sky-500"></i>
                    <div class="flex items-center justify-between mb-4 relative z-10">
                        <span class="p-3 bg-sky-500/10 text-sky-400 rounded-lg group-hover:bg-sky-500 group-hover:text-white transition-all">
                            <i class="fa-solid fa-cloud text-2xl"></i>
                        </span>
                        <span class="text-sm font-mono text-slate-500">DOMINIO 05</span>
                    </div>
                    <h3 class="font-bold text-white group-hover:text-sky-400 transition-colors relative z-10">Nube & DevSecOps</h3>
                    <p class="text-slate-400 mt-3 relative z-10">Seguridad multinube (AWS, Azure, GCP), integración CI/CD (SAST/DAST), contenedores y K8s.</p>
                    <div class="mt-5 pt-4 border-t border-slate-800/80 flex items-center justify-between text-sm font-mono text-slate-400 relative z-10">
                        <span><i class="fa-solid fa-layer-group mr-1"></i>3 Niveles</span>
                        <span class="text-sky-400 group-hover:translate-x-1 transition-transform">Explorar <i class="fa-solid fa-arrow-right"></i></span>
                    </div>
                </div>

                <!-- GRC -->
                <div onclick="goToDomain('grc')" class="card-hover cursor-pointer group p-6 bg-slate-900/80 border border-slate-800 hover:border-emerald-500/50 rounded-xl transition-all duration-300 relative overflow-hidden">
                    <i class="fa-solid fa-scale-balanced bg-icon text-8xl right-2 bottom-2 text-emerald-500"></i>
                    <div class="flex items-center justify-between mb-4 relative z-10">
                        <span class="p-3 bg-emerald-500/10 text-emerald-400 rounded-lg group-hover:bg-emerald-500 group-hover:text-white transition-all">
                            <i class="fa-solid fa-scale-balanced text-2xl"></i>
                        </span>
                        <span class="text-sm font-mono text-slate-500">DOMINIO 06</span>
                    </div>
                    <h3 class="font-bold text-white group-hover:text-emerald-400 transition-colors relative z-10">Gobernanza & Riesgo (GRC)</h3>
                    <p class="text-slate-400 mt-3 relative z-10">Cumplimiento regulatorio (ISO 27001, NIS2, DORA), gestión de riesgos de negocio y liderazgo CISO.</p>
                    <div class="mt-5 pt-4 border-t border-slate-800/80 flex items-center justify-between text-sm font-mono text-slate-400 relative z-10">
                        <span><i class="fa-solid fa-layer-group mr-1"></i>3 Niveles</span>
                        <span class="text-emerald-400 group-hover:translate-x-1 transition-transform">Explorar <i class="fa-solid fa-arrow-right"></i></span>
                    </div>
                </div>
            </div>

            <!-- KEY STATS MATRIX -->
            <div class="p-8 bg-slate-900/60 border border-slate-800 rounded-2xl grid grid-cols-2 md:grid-cols-4 gap-6 text-center">
                <div class="space-y-2">
                    <i class="fa-solid fa-certificate text-3xl text-cyan-400 mb-2"></i>
                    <div class="font-extrabold text-cyan-400 font-mono">40+</div>
                    <div class="text-slate-400 uppercase tracking-wider font-mono">Certificaciones</div>
                </div>
                <div class="space-y-2">
                    <i class="fa-solid fa-diagram-project text-3xl text-indigo-400 mb-2"></i>
                    <div class="font-extrabold text-indigo-400 font-mono">6</div>
                    <div class="text-slate-400 uppercase tracking-wider font-mono">Dominios</div>
                </div>
                <div class="space-y-2">
                    <i class="fa-solid fa-rocket text-3xl text-purple-400 mb-2"></i>
                    <div class="font-extrabold text-purple-400 font-mono">4</div>
                    <div class="text-slate-400 uppercase tracking-wider font-mono">Nichos Emergentes</div>
                </div>
                <div class="space-y-2">
                    <i class="fa-solid fa-calendar-check text-3xl text-emerald-400 mb-2"></i>
                    <div class="font-extrabold text-emerald-400 font-mono">2024-25</div>
                    <div class="text-slate-400 uppercase tracking-wider font-mono">Alineación</div>
                </div>
            </div>
        </section>

        <!-- ==================== TAB 2: DOMAIN DETAILS ==================== -->
        <section id="content-domains" class="tab-content space-y-8 hidden">
            <div class="flex flex-wrap items-center justify-between gap-4 p-5 bg-slate-900 border border-slate-800 rounded-xl">
                <span class="font-semibold text-slate-400 uppercase tracking-wider font-mono">
                    <i class="fa-solid fa-filter mr-2"></i> Filtrar Dominio:
                </span>
                <div id="domainFilterBar" class="flex flex-wrap gap-2">
                    <button onclick="filterDomain('all', event)" class="domain-filter-btn active px-4 py-2 rounded-lg border border-slate-700 bg-slate-800 text-white font-medium transition-all">Todos</button>
                    <button onclick="filterDomain('blue', event)" class="domain-filter-btn px-4 py-2 rounded-lg border border-slate-800 text-slate-400 hover:text-blue-400 transition-all">1. Blue Team</button>
                    <button onclick="filterDomain('red', event)" class="domain-filter-btn px-4 py-2 rounded-lg border border-slate-800 text-slate-400 hover:text-red-400 transition-all">2. Red Team</button>
                    <button onclick="filterDomain('dfir', event)" class="domain-filter-btn px-4 py-2 rounded-lg border border-slate-800 text-slate-400 hover:text-amber-400 transition-all">3. DFIR</button>
                    <button onclick="filterDomain('purple', event)" class="domain-filter-btn px-4 py-2 rounded-lg border border-slate-800 text-slate-400 hover:text-purple-400 transition-all">4. Arquitectura</button>
                    <button onclick="filterDomain('cloud', event)" class="domain-filter-btn px-4 py-2 rounded-lg border border-slate-800 text-slate-400 hover:text-sky-400 transition-all">5. Cloud</button>
                    <button onclick="filterDomain('grc', event)" class="domain-filter-btn px-4 py-2 rounded-lg border border-slate-800 text-slate-400 hover:text-emerald-400 transition-all">6. GRC</button>
                </div>
            </div>

            <div id="domainsContainer" class="space-y-10"></div>
        </section>

        <!-- ==================== TAB 3: CERTIFICATIONS TABLE ==================== -->
        <section id="content-certs" class="tab-content space-y-8 hidden">
            <div class="p-6 bg-slate-900 border border-slate-800 rounded-xl space-y-4">
                <div class="flex flex-col md:flex-row justify-between items-start md:items-center gap-4">
                    <div>
                        <h2 class="font-bold text-white flex items-center gap-3">
                            <i class="fa-solid fa-certificate text-cyan-400"></i> Tabla Comparativa de Certificaciones
                        </h2>
                        <p class="text-slate-400 mt-1">Catálogo estructurado por organismo, nivel, vigencia y requisitos previos.</p>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <select id="levelFilter" onchange="applyCertFilters()" class="bg-slate-950 border border-slate-700 rounded-lg px-4 py-2 text-slate-200 focus:outline-none focus:border-cyan-500 font-mono">
                            <option value="">Todos los Niveles</option>
                            <option value="Básico">Básico</option>
                            <option value="Intermedio">Intermedio</option>
                            <option value="Avanzado">Avanzado</option>
                            <option value="Directivo">Directivo</option>
                        </select>
                        <select id="areaFilter" onchange="applyCertFilters()" class="bg-slate-950 border border-slate-700 rounded-lg px-4 py-2 text-slate-200 focus:outline-none focus:border-cyan-500 font-mono">
                            <option value="">Todas las Áreas</option>
                            <option value="General">General</option>
                            <option value="Blue Team">Blue Team</option>
                            <option value="Red Team">Red Team</option>
                            <option value="DFIR">DFIR</option>
                            <option value="IR">IR</option>
                            <option value="Detección">Detección</option>
                            <option value="Análisis de Malware">Análisis de Malware</option>
                            <option value="Arquitectura">Arquitectura</option>
                            <option value="Cloud">Cloud</option>
                            <option value="Cloud / Kubernetes">Cloud / Kubernetes</option>
                            <option value="GRC">GRC</option>
                            <option value="Auditoría">Auditoría</option>
                            <option value="Riesgo">Riesgo</option>
                            <option value="Gobierno TI">Gobierno TI</option>
                            <option value="Privacidad">Privacidad</option>
                            <option value="Liderazgo">Liderazgo</option>
                            <option value="OT/ICS">OT/ICS</option>
                        </select>
                    </div>
                </div>
            </div>

            <div class="overflow-x-auto border border-slate-800 rounded-xl bg-slate-900/60 custom-scrollbar">
                <table class="w-full text-left">
                    <thead class="bg-slate-950 text-slate-300 font-mono uppercase tracking-wider border-b border-slate-800">
                        <tr>
                            <th class="py-4 px-5">Certificación</th>
                            <th class="py-4 px-5">Organismo</th>
                            <th class="py-4 px-5">Nivel</th>
                            <th class="py-4 px-5">Área</th>
                            <th class="py-4 px-5">Requisitos</th>
                            <th class="py-4 px-5">Vigencia</th>
                        </tr>
                    </thead>
                    <tbody id="certTableBody" class="divide-y divide-slate-800/60 text-slate-300 font-sans"></tbody>
                </table>
            </div>
        </section>

        <!-- ==================== TAB 4: EMERGING NICHES ==================== -->
        <section id="content-emerging" class="tab-content space-y-8 hidden">
            <div class="border-b border-slate-800 pb-5">
                <h2 class="font-bold text-white flex items-center gap-3">
                    <i class="fa-solid fa-microchip text-cyan-400"></i> Especializaciones Emergentes y de Nicho
                </h2>
                <p class="text-slate-400 mt-2">Campos tecnológicos de alta demanda y especialización avanzada para el período 2024-2025.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- OT / SCADA -->
                <div class="p-8 bg-slate-900/80 border border-slate-800 rounded-2xl space-y-5 relative overflow-hidden">
                    <i class="fa-solid fa-industry bg-icon text-9xl right-2 bottom-2 text-amber-500"></i>
                    <div class="flex items-center gap-4 relative z-10">
                        <div class="p-4 bg-amber-500/10 text-amber-400 rounded-xl border border-amber-500/20">
                            <i class="fa-solid fa-industry text-3xl"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-white">7.1 Seguridad OT / IoT / SCADA</h3>
                            <span class="font-mono text-amber-400">Infraestructuras Críticas</span>
                        </div>
                    </div>
                    <div class="space-y-3 text-slate-300 relative z-10">
                        <p><strong class="text-slate-100"><i class="fa-solid fa-circle-chevron-right text-amber-400 mr-2"></i>Funciones Clave:</strong> Desde analista de redes industriales hasta ingeniero de protección para plantas de energía, agua y manufactura.</p>
                        <p><strong class="text-slate-100"><i class="fa-solid fa-certificate text-amber-400 mr-2"></i>Certificaciones:</strong> GICSP, GRID, CSSA, ISA/IEC 62443 Certificate.</p>
                        <p><strong class="text-slate-100"><i class="fa-solid fa-book text-amber-400 mr-2"></i>Marcos:</strong> ISA/IEC 62443, NIST SP 800-82.</p>
                    </div>
                </div>

                <!-- AI / ML Security -->
                <div class="p-8 bg-slate-900/80 border border-slate-800 rounded-2xl space-y-5 relative overflow-hidden">
                    <i class="fa-solid fa-brain bg-icon text-9xl right-2 bottom-2 text-purple-500"></i>
                    <div class="flex items-center gap-4 relative z-10">
                        <div class="p-4 bg-purple-500/10 text-purple-400 rounded-xl border border-purple-500/20">
                            <i class="fa-solid fa-brain text-3xl"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-white">7.2 Seguridad en IA y ML</h3>
                            <span class="font-mono text-purple-400">LLM Red Teaming & Defense</span>
                        </div>
                    </div>
                    <div class="space-y-3 text-slate-300 relative z-10">
                        <p><strong class="text-slate-100"><i class="fa-solid fa-circle-chevron-right text-purple-400 mr-2"></i>Funciones Clave:</strong> Investigador defensivo/ofensivo sobre modelos LLM, prevención de Prompt Injection y envenenamiento de datos.</p>
                        <p><strong class="text-slate-100"><i class="fa-solid fa-book text-purple-400 mr-2"></i>Marcos:</strong> OWASP Top 10 for LLM, MITRE ATLAS, NIST AI RMF.</p>
                    </div>
                </div>

                <!-- Post Quantum -->
                <div class="p-8 bg-slate-900/80 border border-slate-800 rounded-2xl space-y-5 relative overflow-hidden">
                    <i class="fa-solid fa-atom bg-icon text-9xl right-2 bottom-2 text-cyan-500"></i>
                    <div class="flex items-center gap-4 relative z-10">
                        <div class="p-4 bg-cyan-500/10 text-cyan-400 rounded-xl border border-cyan-500/20">
                            <i class="fa-solid fa-atom text-3xl"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-white">7.3 Criptografía Post-Cuántica</h3>
                            <span class="font-mono text-cyan-400">Algoritmos Cuánticos Resilientes</span>
                        </div>
                    </div>
                    <div class="space-y-3 text-slate-300 relative z-10">
                        <p><strong class="text-slate-100"><i class="fa-solid fa-circle-chevron-right text-cyan-400 mr-2"></i>Funciones Clave:</strong> Migración de esquemas de cifrado tradicionales a algoritmos cuántico-resistentes y gestión experta PKI.</p>
                        <p><strong class="text-slate-100"><i class="fa-solid fa-shield text-cyan-400 mr-2"></i>Estándares:</strong> FIPS 203 (ML-KEM), FIPS 204 (ML-DSA), FIPS 205 (SLH-DSA), CNSA 2.0.</p>
                    </div>
                </div>

                <!-- Otras emergentes -->
                <div class="p-8 bg-slate-900/80 border border-slate-800 rounded-2xl space-y-5 relative overflow-hidden">
                    <i class="fa-solid fa-satellite-dish bg-icon text-9xl right-2 bottom-2 text-emerald-500"></i>
                    <div class="flex items-center gap-4 relative z-10">
                        <div class="p-4 bg-emerald-500/10 text-emerald-400 rounded-xl border border-emerald-500/20">
                            <i class="fa-solid fa-satellite-dish text-3xl"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-white">7.4 Otras Tecnologías</h3>
                            <span class="font-mono text-emerald-400">Blockchain, Vehicular, Espacial, 5G/6G</span>
                        </div>
                    </div>
                    <ul class="text-slate-300 space-y-2 list-none relative z-10">
                        <li><i class="fa-solid fa-cube text-emerald-400 mr-2"></i><strong>Blockchain / Web3:</strong> Auditoría de Smart Contracts (OWASP Smart Contract Top 10).</li>
                        <li><i class="fa-solid fa-car text-emerald-400 mr-2"></i><strong>Seguridad Vehicular:</strong> ISO/SAE 21434, UNECE R155/R156.</li>
                        <li><i class="fa-solid fa-satellite text-emerald-400 mr-2"></i><strong>Seguridad Espacial:</strong> NIST IR 8270, Space ISAC.</li>
                        <li><i class="fa-solid fa-tower-cell text-emerald-400 mr-2"></i><strong>Redes 5G / 6G:</strong> 3GPP, GSMA FS.11, NIST 5G Cybersecurity.</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- ==================== TAB 5: GLOSSARY ==================== -->
        <section id="content-glossary" class="tab-content space-y-8 hidden">
            <div class="border-b border-slate-800 pb-5 flex flex-col md:flex-row justify-between items-start md:items-center gap-4">
                <div>
                    <h2 class="font-bold text-white flex items-center gap-3">
                        <i class="fa-solid fa-book-open text-cyan-400"></i> Glosario de Términos Técnicos
                    </h2>
                    <p class="text-slate-400 mt-2">Definiciones esenciales para la comprensión del ecosistema de ciberseguridad.</p>
                </div>
                <div class="relative w-full md:w-80">
                    <i class="fa-solid fa-magnifying-glass absolute left-3 top-1/2 -translate-y-1/2 text-slate-500"></i>
                    <input type="text" id="glossarySearch" placeholder="Buscar término..." 
                        class="w-full bg-slate-900 border border-slate-700/60 rounded-lg pl-10 pr-3 py-2 text-slate-200 focus:outline-none focus:border-cyan-500 transition-all font-mono">
                </div>
            </div>

            <div id="glossaryContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4"></div>
        </section>

        <!-- ==================== TAB 6: TRENDS & REFS ==================== -->
        <section id="content-trends" class="tab-content space-y-10 hidden">
            <div class="space-y-6">
                <h2 class="font-bold text-white flex items-center gap-3">
                    <i class="fa-solid fa-arrow-trend-up text-cyan-400"></i> Tendencias Clave 2024-2025
                </h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5">
                    <div class="p-6 bg-slate-900 border border-slate-800 rounded-xl space-y-3 card-hover">
                        <i class="fa-solid fa-robot text-3xl text-cyan-400"></i>
                        <div class="text-cyan-400 font-bold font-mono">01. IA Generativa en SOC</div>
                        <p class="text-slate-400">Automatización de triage de alertas, generación automática de reglas de detección y resúmenes ejecutivos de incidentes.</p>
                    </div>
                    <div class="p-6 bg-slate-900 border border-slate-800 rounded-xl space-y-3 card-hover">
                        <i class="fa-solid fa-lock text-3xl text-cyan-400"></i>
                        <div class="text-cyan-400 font-bold font-mono">02. Zero Trust Adoption</div>
                        <p class="text-slate-400">Consolidación de modelos de verificación continua alineados de manera estricta con NIST SP 800-207.</p>
                    </div>
                    <div class="p-6 bg-slate-900 border border-slate-800 rounded-xl space-y-3 card-hover">
                        <i class="fa-solid fa-atom text-3xl text-cyan-400"></i>
                        <div class="text-cyan-400 font-bold font-mono">03. Migración Cuántica</div>
                        <p class="text-slate-400">Implementación activa de los estándares finales NIST PQC (FIPS 203, 204 y 205).</p>
                    </div>
                    <div class="p-6 bg-slate-900 border border-slate-800 rounded-xl space-y-3 card-hover">
                        <i class="fa-solid fa-gavel text-3xl text-cyan-400"></i>
                        <div class="text-cyan-400 font-bold font-mono">04. Marcos Regulatorios UE</div>
                        <p class="text-slate-400">Entrada en vigor y exigencia de cumplimiento para NIS2, DORA y Cyber Resilience Act (CRA).</p>
                    </div>
                    <div class="p-6 bg-slate-900 border border-slate-800 rounded-xl space-y-3 card-hover">
                        <i class="fa-solid fa-comment-dots text-3xl text-cyan-400"></i>
                        <div class="text-cyan-400 font-bold font-mono">05. LLM & AI Red Teaming</div>
                        <p class="text-slate-400">Evaluación continua de vulnerabilidades en modelos de lenguaje con OWASP LLM y MITRE ATLAS.</p>
                    </div>
                    <div class="p-6 bg-slate-900 border border-slate-800 rounded-xl space-y-3 card-hover">
                        <i class="fa-solid fa-network-wired text-3xl text-cyan-400"></i>
                        <div class="text-cyan-400 font-bold font-mono">06. Convergencia IT / OT</div>
                        <p class="text-slate-400">Unificación de la visibilidad de ciberdefensa entre entornos corporativos e infraestructuras operacionales críticas.</p>
                    </div>
                </div>
            </div>

            <div class="p-8 bg-slate-900/60 border border-slate-800 rounded-2xl space-y-5">
                <h3 class="font-bold text-white flex items-center gap-3">
                    <i class="fa-solid fa-book text-slate-400 text-2xl"></i> Bibliografía Sugerida (APA 7)
                </h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-3 text-slate-400 font-mono">
                    <div class="p-3 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>CSA. (2024). <em>Cloud Controls Matrix (CCM)</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>ENISA. (2024). <em>Cybersecurity Skills Framework</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>ISACA. (2024). <em>State of Cybersecurity Report</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>ISC². (2024). <em>Cybersecurity Workforce Study</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>ISO/IEC. (2012). <em>ISO/IEC 27037:2012</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>ISO/IEC. (2022). <em>ISO/IEC 27001:2022</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>MITRE. (2024). <em>ATLAS Framework</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>MITRE. (2024). <em>ATT&CK Framework</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>NIST. (2020). <em>Zero Trust Architecture (SP 800-207)</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>NIST. (2024). <em>Cybersecurity Framework 2.0</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>NIST. (2024). <em>NICE Framework (SP 800-181r1)</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>OWASP. (2024). <em>Top 10 for LLM Applications</em>.</div>
                    <div class="p-2.5 bg-slate-950 rounded-lg border border-slate-800"><i class="fa-solid fa-file-lines text-cyan-400 mr-2"></i>SANS Institute. (2024). <em>Cyber Workforce Report</em>.</div>
                </div>
            </div>
        </section>

    </main>

    <!-- FOOTER -->
    <footer class="border-t border-slate-800/80 bg-slate-950 text-slate-500 py-8 text-center font-mono">
        <div class="max-w-7xl mx-auto px-4">
            <i class="fa-solid fa-shield-halved text-cyan-500 mr-2"></i>
            Dashboard Hub Interactivo de Ciberseguridad • Alineado con NIST NICE, MITRE ATT&CK & CSF 2.0
        </div>
    </footer>

    <!-- INTERACTIVE SCRIPT -->
    <script>
        // ============================================================
        // DOMAINS DATA
        // ============================================================
        const domainsData = [
            {
                id: 'blue',
                title: '1. Operaciones de Seguridad y Defensa (Blue Team)',
                color: 'blue',
                badge: 'Defensa Activa & SOC',
                definition: 'Área especializada en monitorear, detectar, analizar y mitigar amenazas activas en infraestructuras corporativas. Se apoya en marcos como MITRE ATT&CK, NIST CSF 2.0 y CIS Controls v8.',
                levels: [
                    {
                        name: 'Nivel Básico (Tier 1)',
                        role: 'Analista de SOC (Security Operations Center)',
                        functions: [
                            'Monitorea alertas en tiempo real mediante herramientas SIEM/EDR.',
                            'Filtra falsos positivos y realiza triage inicial de incidentes.',
                            'Documenta y escala incidentes según procedimientos establecidos.'
                        ],
                        certs: ['CompTIA Security+', 'CompTIA CySA+', 'Cisco CyberOps Associate'],
                        nice: 'Threat Analysis (PR-CIR-01), Cyber Defense Analysis (PR-CDA-01)'
                    },
                    {
                        name: 'Nivel Intermedio (Tier 2 / Tier 3)',
                        role: 'Analista de Respuesta a Incidentes (IR) / Threat Hunter',
                        functions: [
                            'Investiga contenciones de brechas complejas.',
                            'Busca proactivamente amenazas dentro de la red (Threat Hunting) usando MITRE ATT&CK.',
                            'Desarrolla reglas de detección personalizadas (Sigma, YARA, KQL).'
                        ],
                        certs: ['CompTIA CySA+', 'GIAC Certified Incident Handler (GCIH)', 'GIAC Certified Forensic Analyst (GCFA)'],
                        nice: 'Incident Response (PR-CIR-02), Threat Hunting (PR-TH-01)'
                    },
                    {
                        name: 'Nivel Avanzado',
                        role: 'Ingeniero de Detección (Detection Engineer) / Arquitecto de SOC',
                        functions: [
                            'Automatiza flujos de trabajo de respuesta (SOAR).',
                            'Diseña la arquitectura de visibilidad de toda la empresa.',
                            'Crea modelos predictivos de detección y reglas avanzadas alineadas a MITRE ATT&CK.',
                            'Integra IA generativa en operaciones de SOC (tendencia 2024-2025).'
                        ],
                        certs: ['GIAC Certified Detection Analyst (GCDA)', 'GIAC Certified Incident Handler (GCIH)', 'GIAC Strategic Planning, Policy, and Leadership (GSTRT)'],
                        nice: 'Cyber Defense Infrastructure Support (PR-INF-01), Cyber Defense Analysis (PR-CDA-02)'
                    }
                ]
            },
            {
                id: 'red',
                title: '2. Seguridad Ofensiva y Evaluación (Red Team)',
                color: 'red',
                badge: 'Ataque Simulado & Pentest',
                definition: 'Área especializada en simular ataques de cibercriminales para descubrir vulnerabilidades antes de que sean explotadas. Se apoya en marcos como MITRE ATT&CK, TIBER-EU, CBEST y OWASP Testing Guide.',
                levels: [
                    {
                        name: 'Nivel Básico',
                        role: 'Analista de Vulnerabilidades',
                        functions: [
                            'Ejecuta escaneos automáticos de vulnerabilidades.',
                            'Valida hallazgos básicos y redacta reportes de remediación iniciales.',
                            'Gestiona el ciclo de vida de vulnerabilidades (CVSS, CVE).'
                        ],
                        certs: ['eJPT (INE Security)', 'CompTIA PenTest+'],
                        nice: 'Vulnerability Assessment (PR-VA-01)'
                    },
                    {
                        name: 'Nivel Intermedio',
                        role: 'Penetration Tester (Ethical Hacker)',
                        functions: [
                            'Realiza pruebas de penetración manuales sobre aplicaciones, redes e infraestructuras de forma controlada.',
                            'Aplica metodologías como PTES, OWASP WSTG y OSSTMM.'
                        ],
                        certs: ['OSCP (Offensive Security)', 'CEH (Certified Ethical Hacker)'],
                        nice: 'Penetration Testing (PR-PT-01)'
                    },
                    {
                        name: 'Nivel Avanzado',
                        role: 'Operador de Red Team / Adversary Emulator',
                        functions: [
                            'Simula amenazas persistentes avanzadas (APT) a largo plazo.',
                            'Realiza ataques multifase que evaden activamente las defensas.',
                            'Ejecuta ingeniería social avanzada y bypass de EDRs. Alinea operaciones con TIBER-EU y CBEST.'
                        ],
                        certs: ['OSEP', 'CRTO', 'CRTP', 'CRTL'],
                        nice: 'Red Team Operations (PR-RT-01)'
                    }
                ]
            },
            {
                id: 'dfir',
                title: '3. Forense Digital e Investigación (DFIR)',
                color: 'amber',
                badge: 'Análisis Forense & Malware',
                definition: 'Área especializada en la recolección, análisis e interpretación de evidencias digitales tras un ataque o investigación judicial. Se rige por ISO/IEC 27037, RFC 3227 y principios de cadena de custodia.',
                levels: [
                    {
                        name: 'Nivel Básico',
                        role: 'Técnico en Adquisición Forense',
                        functions: [
                            'Asegura la cadena de custodia.',
                            'Realiza clonación bit a bit de discos, memoria RAM y dispositivos móviles sin alterar la evidencia.',
                            'Documenta procedimientos conforme a ISO/IEC 27037.'
                        ],
                        certs: ['CHFI (EC-Council)', 'GCFE (GIAC)'],
                        nice: 'Digital Forensics (PR-DF-01)'
                    },
                    {
                        name: 'Nivel Intermedio',
                        role: 'Analista Forense Digital (Host/Network Forensics)',
                        functions: [
                            'Reconstruye la cronología de una intrusión mediante análisis de artefactos de SO, registros de red y volcados de memoria.',
                            'Aplica el orden de volatilidad de RFC 3227.'
                        ],
                        certs: ['GCFE (GIAC)', 'GCFA (GIAC)'],
                        nice: 'Digital Forensics (PR-DF-02), Incident Response (PR-CIR-03)'
                    },
                    {
                        name: 'Nivel Avanzado',
                        role: 'Analista / Ingeniero de Inversión de Malware (Reverse Engineer)',
                        functions: [
                            'Descompila y analiza binarios de malware en entornos aislados (Sandboxing/Disassembly).',
                            'Comprende código fuente, comportamiento y mecanismos de cifrado.',
                            'Desarrolla firmas YARA y reglas de detección.'
                        ],
                        certs: ['GREM (GIAC)'],
                        extraTraining: 'Formación complementaria: FLARE (Mandiant) y Malware Unicorn.',
                        nice: 'Malware Analysis (PR-MA-01)'
                    }
                ]
            },
            {
                id: 'purple',
                title: '4. Arquitectura e Ingeniería de Seguridad (Purple Team / Build)',
                color: 'purple',
                badge: 'Zero Trust & Hardening',
                definition: 'Área especializada en construir, configurar y mantener entornos tecnológicamente blindados. Se apoya en Zero Trust Architecture (NIST SP 800-207), SABSA y TOGAF.',
                levels: [
                    {
                        name: 'Nivel Básico',
                        role: 'Administrador de Seguridad de Redes / Sistemas',
                        functions: [
                            'Configura firewalls, VPNs, gestión de parches, ACLs y antivirus corporativos.',
                            'Aplica CIS Benchmarks y hardening de sistemas.'
                        ],
                        certs: ['Cisco CyberOps Associate', 'Cisco CCNP Security', 'CompTIA Network+'],
                        nice: 'Network Defense (PR-INF-02), System Administration (OM-ST-01)'
                    },
                    {
                        name: 'Nivel Intermedio',
                        role: 'Ingeniero de Ciberseguridad',
                        functions: [
                            'Implementa tecnologías como IAM, segmentación Zero Trust, WAFs y encriptación de datos a gran escala.',
                            'Aplica NIST SP 800-207 (Zero Trust Architecture).'
                        ],
                        certs: ['GIAC Security Essentials (GSEC)', 'CISSP'],
                        nice: 'Security Architecture (SP-ARC-01)'
                    },
                    {
                        name: 'Nivel Avanzado',
                        role: 'Arquitecto de Ciberseguridad',
                        functions: [
                            'Diseña la estrategia y el modelo de seguridad global de toda la empresa (on-premise, nube e híbridos).',
                            'Asegura resistencia al fallo y alineación con el negocio mediante SABSA y TOGAF.'
                        ],
                        certs: ['SABSA', 'CISSP', 'ISSAP', 'TOGAF'],
                        nice: 'Security Architecture (SP-ARC-02), Enterprise Architecture (SP-EA-01)'
                    }
                ]
            },
            {
                id: 'cloud',
                title: '5. Seguridad en la Nube (Cloud Security) & DevSecOps',
                color: 'sky',
                badge: 'Cloud & CI/CD Pipelines',
                definition: 'Área especializada en entornos distribuidos como AWS, Azure y Google Cloud, y en pipelines de desarrollo de software. Se apoya en CSA CCM, CIS Benchmarks, OWASP Cloud Top 10 y NIST SP 800-204.',
                levels: [
                    {
                        name: 'Nivel Básico',
                        role: 'Especialista en Cumplimiento e Identidad Cloud',
                        functions: [
                            'Revisa permisos de roles de IAM en la nube.',
                            'Auditoría básica de S3 buckets y políticas de seguridad.',
                            'Aplica CIS Benchmarks para cloud.'
                        ],
                        certs: ['AWS Certified Cloud Practitioner', 'Azure Fundamentals (AZ-900)', 'Google Cloud Digital Leader', 'CCSK (CSA)'],
                        nice: 'Cloud Security (PR-CS-01)'
                    },
                    {
                        name: 'Nivel Intermedio',
                        role: 'Ingeniero de Seguridad en la Nube / DevSecOps Specialist',
                        functions: [
                            'Integra herramientas SAST/DAST en flujos CI/CD.',
                            'Asegura infraestructura como código (Terraform).',
                            'Gestiona seguridad de contenedores (Docker/Kubernetes) con CKS.'
                        ],
                        certs: ['AWS Certified Security – Specialty', 'Azure Security Engineer (AZ-500)', 'CCSP (ISC²)', 'CKS (CNCF)'],
                        nice: 'DevSecOps (SP-DSO-01), Cloud Security (PR-CS-02)'
                    },
                    {
                        name: 'Nivel Avanzado',
                        role: 'Arquitecto de Seguridad Cloud Multi-Nube',
                        functions: [
                            'Diseña infraestructuras resilientes en múltiples proveedores de nube bajo principios Zero Trust.',
                            'Gestiona claves (KMS) y protección de microservicios a escala.'
                        ],
                        certs: ['CCSP (ISC²)', 'GIAC Cloud Security Automation (GCSA)', 'AWS Certified Solutions Architect – Professional'],
                        nice: 'Cloud Security Architecture (SP-ARC-03)'
                    }
                ]
            },
            {
                id: 'grc',
                title: '6. Gobernanza, Riesgo y Cumplimiento (GRC)',
                color: 'emerald',
                badge: 'Estrategia, Normativa & CISO',
                definition: 'Área enfocada en el cumplimiento legal, la gestión del riesgo de negocio y la creación de políticas corporativas. Se apoya en ISO/IEC 27001, NIST CSF 2.0, PCI-DSS, GDPR, HIPAA, NIS2 y DORA.',
                levels: [
                    {
                        name: 'Nivel Básico',
                        role: 'Analista de Cumplimiento / Auditor Junior',
                        functions: [
                            'Revisa listas de verificación para normativas (ISO 27001, PCI-DSS, GDPR, HIPAA).',
                            'Apoya en la recolección de evidencias.'
                        ],
                        certs: ['ISACA CISA', 'ISO 27001 Lead Auditor'],
                        nice: 'Audit (SP-AUD-01), Compliance (SP-CMP-01)'
                    },
                    {
                        name: 'Nivel Intermedio',
                        role: 'Especialista en Riesgos Tecnológicos / GRC Lead',
                        functions: [
                            'Evalúa el impacto de amenazas en el negocio.',
                            'Gestiona el riesgo de proveedores de terceros (Third-Party Risk Management).',
                            'Diseña políticas internas alineadas a NIST CSF 2.0 e ISO 27001.'
                        ],
                        certs: ['CRISC (ISACA)', 'CGEIT (ISACA)', 'CIPP/E (IAPP)'],
                        nice: 'Risk Management (SP-RM-01), Privacy (SP-PRV-01)'
                    },
                    {
                        name: 'Nivel Avanzado',
                        role: 'Director de Seguridad / CISO (Chief Information Security Officer)',
                        functions: [
                            'Lidera la estrategia global de ciberseguridad.',
                            'Gestiona presupuestos y responde ante la junta directiva.',
                            'Maneja crisis institucionales y cumple con NIS2 y DORA.'
                        ],
                        certs: ['CISM (ISACA)', 'CCISO (EC-Council)', 'CISSP (ISC²)'],
                        nice: 'Executive Leadership (SP-EL-01), Strategic Planning (SP-SP-01)'
                    }
                ]
            }
        ];

        // ============================================================
        // CERTIFICATIONS TABLE DATA
        // ============================================================
        const certsData = [
            { cert: 'Security+', org: 'CompTIA', level: 'Básico', area: 'General', req: 'No', exp: '3 años (CEU)' },
            { cert: 'CySA+', org: 'CompTIA', level: 'Intermedio', area: 'Blue Team', req: 'Recomendado Security+', exp: '3 años' },
            { cert: 'PenTest+', org: 'CompTIA', level: 'Intermedio', area: 'Red Team', req: 'Recomendado Security+', exp: '3 años' },
            { cert: 'Network+', org: 'CompTIA', level: 'Básico', area: 'General', req: 'No', exp: '3 años (CEU)' },
            { cert: 'Cisco CyberOps Associate', org: 'Cisco', level: 'Básico', area: 'Blue Team', req: 'No', exp: '3 años' },
            { cert: 'CCNP Security', org: 'Cisco', level: 'Intermedio', area: 'Arquitectura', req: 'CCNA', exp: '3 años' },
            { cert: 'GCIH', org: 'GIAC / SANS', level: 'Intermedio', area: 'IR', req: 'No', exp: '4 años' },
            { cert: 'GCFE', org: 'GIAC / SANS', level: 'Intermedio', area: 'DFIR', req: 'No', exp: '4 años' },
            { cert: 'GCFA', org: 'GIAC / SANS', level: 'Avanzado', area: 'DFIR', req: 'No', exp: '4 años' },
            { cert: 'GREM', org: 'GIAC / SANS', level: 'Avanzado', area: 'Análisis de Malware', req: 'No', exp: '4 años' },
            { cert: 'GCDA', org: 'GIAC / SANS', level: 'Avanzado', area: 'Detección', req: 'No', exp: '4 años' },
            { cert: 'GSTRT', org: 'GIAC / SANS', level: 'Directivo', area: 'Liderazgo', req: 'No', exp: '4 años' },
            { cert: 'GSEC', org: 'GIAC / SANS', level: 'Intermedio', area: 'Arquitectura', req: 'No', exp: '4 años' },
            { cert: 'GICSP', org: 'GIAC / SANS', level: 'Avanzado', area: 'OT/ICS', req: 'No', exp: '4 años' },
            { cert: 'GRID', org: 'GIAC / SANS', level: 'Avanzado', area: 'OT/ICS', req: 'No', exp: '4 años' },
            { cert: 'GCSA', org: 'GIAC / SANS', level: 'Avanzado', area: 'Cloud', req: 'No', exp: '4 años' },
            { cert: 'OSCP', org: 'OffSec', level: 'Intermedio', area: 'Red Team', req: 'No', exp: 'Vitalicia' },
            { cert: 'OSEP', org: 'OffSec', level: 'Avanzado', area: 'Red Team', req: 'OSCP recomendado', exp: 'Vitalicia' },
            { cert: 'CRTO', org: 'Zero-Point Security', level: 'Avanzado', area: 'Red Team', req: 'No', exp: '3 años' },
            { cert: 'CRTP', org: 'Altered Security', level: 'Intermedio', area: 'Red Team', req: 'No', exp: '3 años' },
            { cert: 'CRTL', org: 'Altered Security', level: 'Avanzado', area: 'Red Team', req: 'CRTP recomendado', exp: '3 años' },
            { cert: 'eJPT', org: 'INE Security', level: 'Básico', area: 'Red Team', req: 'No', exp: '3 años' },
            { cert: 'CEH', org: 'EC-Council', level: 'Intermedio', area: 'Red Team', req: 'No', exp: '3 años' },
            { cert: 'CHFI', org: 'EC-Council', level: 'Básico', area: 'DFIR', req: 'No', exp: '3 años' },
            { cert: 'CCISO', org: 'EC-Council', level: 'Directivo', area: 'GRC', req: 'Experiencia', exp: '3 años' },
            { cert: 'CISSP', org: 'ISC²', level: 'Avanzado', area: 'General', req: '5 años exp.', exp: '3 años' },
            { cert: 'CCSP', org: 'ISC²', level: 'Avanzado', area: 'Cloud', req: '5 años exp.', exp: '3 años' },
            { cert: 'ISSAP', org: 'ISC²', level: 'Avanzado', area: 'Arquitectura', req: 'CISSP', exp: '3 años' },
            { cert: 'CISA', org: 'ISACA', level: 'Intermedio', area: 'Auditoría', req: 'No', exp: '3 años' },
            { cert: 'CISM', org: 'ISACA', level: 'Directivo', area: 'GRC', req: '5 años exp.', exp: '3 años' },
            { cert: 'CRISC', org: 'ISACA', level: 'Intermedio', area: 'Riesgo', req: 'No', exp: '3 años' },
            { cert: 'CGEIT', org: 'ISACA', level: 'Directivo', area: 'Gobierno TI', req: 'No', exp: '3 años' },
            { cert: 'CIPP/E', org: 'IAPP', level: 'Intermedio', area: 'Privacidad', req: 'No', exp: '2 años' },
            { cert: 'ISO 27001 Lead Auditor', org: 'PECB / BSI', level: 'Intermedio', area: 'Auditoría', req: 'No', exp: '3 años' },
            { cert: 'ISO 27001 Lead Implementer', org: 'PECB / BSI', level: 'Intermedio', area: 'GRC', req: 'No', exp: '3 años' },
            { cert: 'SABSA', org: 'SABSA Institute', level: 'Avanzado', area: 'Arquitectura', req: 'No', exp: '3 años' },
            { cert: 'TOGAF', org: 'The Open Group', level: 'Avanzado', area: 'Arquitectura', req: 'No', exp: '3 años' },
            { cert: 'CCSK', org: 'CSA', level: 'Básico', area: 'Cloud', req: 'No', exp: '2 años' },
            { cert: 'AWS Certified Cloud Practitioner', org: 'AWS', level: 'Básico', area: 'Cloud', req: 'No', exp: '3 años' },
            { cert: 'AWS Certified Security – Specialty', org: 'AWS', level: 'Intermedio', area: 'Cloud', req: 'Recomendado AWS Associate', exp: '3 años' },
            { cert: 'AWS Certified Solutions Architect – Professional', org: 'AWS', level: 'Avanzado', area: 'Cloud', req: 'AWS Associate', exp: '3 años' },
            { cert: 'Azure Fundamentals (AZ-900)', org: 'Microsoft', level: 'Básico', area: 'Cloud', req: 'No', exp: 'Sin vencimiento' },
            { cert: 'Azure Security Engineer (AZ-500)', org: 'Microsoft', level: 'Intermedio', area: 'Cloud', req: 'No', exp: '1 año' },
            { cert: 'Google Cloud Digital Leader', org: 'Google Cloud', level: 'Básico', area: 'Cloud', req: 'No', exp: '3 años' },
            { cert: 'CKS', org: 'CNCF', level: 'Avanzado', area: 'Cloud / Kubernetes', req: 'CKA recomendado', exp: '3 años' },
            { cert: 'ISA/IEC 62443', org: 'ISA', level: 'Avanzado', area: 'OT/ICS', req: 'No', exp: '3 años' }
        ];

        // ============================================================
        // GLOSSARY DATA
        // ============================================================
        const glossaryData = [
            { term: 'APT', category: 'Amenazas', def: 'Advanced Persistent Threat. Actor malicioso con recursos avanzados que mantiene acceso prolongado a una red objetivo.' },
            { term: 'Blue Team', category: 'Operaciones', def: 'Equipo defensivo encargado de proteger la infraestructura, detectar incidentes y responder a ataques.' },
            { term: 'Red Team', category: 'Operaciones', def: 'Equipo ofensivo que simula ataques reales para evaluar la eficacia de las defensas.' },
            { term: 'Purple Team', category: 'Operaciones', def: 'Colaboración entre Blue y Red Team para mejorar continuamente las detecciones y la postura defensiva.' },
            { term: 'SOC', category: 'Operaciones', def: 'Security Operations Center. Centro que monitoriza, detecta y responde a incidentes de seguridad 24/7.' },
            { term: 'SIEM', category: 'Herramientas', def: 'Security Information and Event Management. Plataforma que centraliza logs y correlaciona eventos para detectar amenazas.' },
            { term: 'EDR', category: 'Herramientas', def: 'Endpoint Detection and Response. Solución que monitoriza y responde a amenazas en endpoints (equipos finales).' },
            { term: 'XDR', category: 'Herramientas', def: 'Extended Detection and Response. Evolución del EDR que integra múltiples fuentes (red, cloud, email).' },
            { term: 'SOAR', category: 'Herramientas', def: 'Security Orchestration, Automation and Response. Plataforma para automatizar la respuesta a incidentes.' },
            { term: 'MITRE ATT&CK', category: 'Marcos', def: 'Base de conocimiento de tácticas, técnicas y procedimientos (TTP) usados por adversarios reales.' },
            { term: 'MITRE ATLAS', category: 'Marcos', def: 'Adaptación de ATT&CK para sistemas de Inteligencia Artificial y Machine Learning.' },
            { term: 'NIST CSF', category: 'Marcos', def: 'Cybersecurity Framework del NIST. Marco de referencia con funciones: Identificar, Proteger, Detectar, Responder, Recuperar, Gobernar.' },
            { term: 'NIST NICE', category: 'Marcos', def: 'Framework de NIST (SP 800-181r1) que define roles, competencias y tareas del personal de ciberseguridad.' },
            { term: 'ISO 27001', category: 'Marcos', def: 'Estándar internacional para Sistemas de Gestión de Seguridad de la Información (SGSI).' },
            { term: 'ISO 27037', category: 'Marcos', def: 'Estándar para identificación, recolección, adquisición y preservación de evidencia digital.' },
            { term: 'CIS Controls', category: 'Marcos', def: 'Conjunto priorizado de 18 controles de ciberseguridad desarrollados por Center for Internet Security.' },
            { term: 'Zero Trust', category: 'Arquitectura', def: 'Modelo de seguridad que asume que ninguna entidad es confiable por defecto; verificación continua (NIST SP 800-207).' },
            { term: 'IAM', category: 'Arquitectura', def: 'Identity and Access Management. Gestión de identidades y control de accesos a recursos.' },
            { term: 'MFA', category: 'Arquitectura', def: 'Multi-Factor Authentication. Autenticación basada en múltiples factores (algo que sabes, tienes o eres).' },
            { term: 'PKI', category: 'Criptografía', def: 'Public Key Infrastructure. Infraestructura de clave pública que gestiona certificados digitales.' },
            { term: 'PQC', category: 'Criptografía', def: 'Post-Quantum Cryptography. Algoritmos resistentes a ataques de computación cuántica (FIPS 203/204/205).' },
            { term: 'KMS', category: 'Cloud', def: 'Key Management Service. Servicio para crear, gestionar y rotar claves criptográficas.' },
            { term: 'CSPM', category: 'Cloud', def: 'Cloud Security Posture Management. Herramienta que audita configuraciones de seguridad en la nube.' },
            { term: 'CWPP', category: 'Cloud', def: 'Cloud Workload Protection Platform. Protección de cargas de trabajo en cloud (VMs, contenedores, serverless).' },
            { term: 'CI/CD', category: 'DevSecOps', def: 'Continuous Integration / Continuous Delivery. Prácticas de automatización del ciclo de vida del software.' },
            { term: 'SAST', category: 'DevSecOps', def: 'Static Application Security Testing. Análisis de código fuente sin ejecutarlo.' },
            { term: 'DAST', category: 'DevSecOps', def: 'Dynamic Application Security Testing. Análisis de aplicaciones en ejecución.' },
            { term: 'SCA', category: 'DevSecOps', def: 'Software Composition Analysis. Análisis de dependencias y librerías de terceros.' },
            { term: 'IaC', category: 'DevSecOps', def: 'Infrastructure as Code. Gestión de infraestructura mediante código (Terraform, Ansible).' },
            { term: 'OWASP', category: 'Marcos', def: 'Open Worldwide Application Security Project. Organización que publica el Top 10 de riesgos web y LLM.' },
            { term: 'CVE', category: 'Vulnerabilidades', def: 'Common Vulnerabilities and Exposures. Identificador único para vulnerabilidades conocidas.' },
            { term: 'CVSS', category: 'Vulnerabilidades', def: 'Common Vulnerability Scoring System. Sistema de puntuación de severidad de vulnerabilidades (0-10).' },
            { term: 'CWE', category: 'Vulnerabilidades', def: 'Common Weakness Enumeration. Catálogo de debilidades de software.' },
            { term: 'TTP', category: 'Amenazas', def: 'Tactics, Techniques and Procedures. Patrones de comportamiento de adversarios.' },
            { term: 'IoC', category: 'Amenazas', def: 'Indicator of Compromise. Evidencia observable de una intrusión (hashes, IPs, dominios).' },
            { term: 'Threat Hunting', category: 'Operaciones', def: 'Búsqueda proactiva de amenazas que han evadido las defensas automáticas.' },
            { term: 'DFIR', category: 'Forense', def: 'Digital Forensics and Incident Response. Disciplina que combina análisis forense y respuesta a incidentes.' },
            { term: 'YARA', category: 'Forense', def: 'Herramienta y lenguaje de reglas para identificar malware por patrones.' },
            { term: 'Sandbox', category: 'Forense', def: 'Entorno aislado para ejecutar y analizar código potencialmente malicioso.' },
            { term: 'OT', category: 'Industrial', def: 'Operational Technology. Tecnología que controla procesos físicos (SCADA, PLC, ICS).' },
            { term: 'ICS', category: 'Industrial', def: 'Industrial Control Systems. Sistemas de control industrial usados en infraestructuras críticas.' },
            { term: 'SCADA', category: 'Industrial', def: 'Supervisory Control and Data Acquisition. Sistema de control y supervisión de procesos industriales.' },
            { term: 'GRC', category: 'Gobernanza', def: 'Governance, Risk and Compliance. Disciplina que alinea seguridad con objetivos de negocio y normativa.' },
            { term: 'NIS2', category: 'Regulación', def: 'Directiva europea que amplía los requisitos de ciberseguridad a más sectores críticos.' },
            { term: 'DORA', category: 'Regulación', def: 'Digital Operational Resilience Act. Reglamento europeo de resiliencia operativa para el sector financiero.' },
            { term: 'CRA', category: 'Regulación', def: 'Cyber Resilience Act. Reglamento europeo que exige seguridad en productos con componentes digitales.' },
            { term: 'GDPR', category: 'Regulación', def: 'General Data Protection Regulation. Reglamento europeo de protección de datos personales.' },
            { term: 'CISO', category: 'Gobernanza', def: 'Chief Information Security Officer. Máximo responsable de la estrategia de ciberseguridad.' }
        ];

        // ============================================================
        // RENDER DOMAINS
        // ============================================================
        function renderDomains() {
            const container = document.getElementById('domainsContainer');
            container.innerHTML = domainsData.map(d => `
                <div id="domain-card-${d.id}" class="domain-card bg-slate-900 border border-slate-800 rounded-2xl p-8 space-y-6">
                    <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 border-b border-slate-800 pb-5">
                        <div>
                            <span class="text-sm font-mono font-bold text-${d.color}-400 bg-${d.color}-500/10 border border-${d.color}-500/20 px-3 py-1.5 rounded-md">
                                <i class="fa-solid fa-tag mr-1"></i>${d.badge}
                            </span>
                            <h2 class="font-bold text-white mt-3">${d.title}</h2>
                        </div>
                    </div>
                    <p class="text-slate-300 leading-relaxed">${d.definition}</p>
                    
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-5">
                        ${d.levels.map(lvl => `
                            <div class="bg-slate-950/70 border border-slate-800/80 rounded-xl p-5 flex flex-col justify-between space-y-4">
                                <div>
                                    <div class="font-mono text-cyan-400 font-semibold mb-2"><i class="fa-solid fa-signal mr-1"></i>${lvl.name}</div>
                                    <h3 class="font-bold text-white mb-3">${lvl.role}</h3>
                                    <div class="text-slate-400 space-y-1">
                                        <div class="font-semibold text-slate-300"><i class="fa-solid fa-list-check mr-1"></i>Funciones:</div>
                                        <ul class="list-disc pl-5 space-y-1">
                                            ${lvl.functions.map(f => `<li>${f}</li>`).join('')}
                                        </ul>
                                    </div>
                                </div>
                                <div class="pt-4 border-t border-slate-800/80 space-y-3">
                                    <div>
                                        <span class="text-xs font-mono uppercase text-slate-500 block mb-1"><i class="fa-solid fa-certificate mr-1"></i>Certificaciones:</span>
                                        <div class="flex flex-wrap gap-1.5">
                                            ${lvl.certs.map(c => `<span class="bg-slate-900 border border-slate-700 text-slate-300 text-xs px-2.5 py-1 rounded font-mono">${c}</span>`).join('')}
                                        </div>
                                        ${lvl.extraTraining ? `<div class="text-xs text-slate-500 italic mt-2"><i class="fa-solid fa-graduation-cap mr-1"></i>${lvl.extraTraining}</div>` : ''}
                                    </div>
                                    <div>
                                        <span class="text-xs font-mono uppercase text-slate-500 block mb-1"><i class="fa-solid fa-diagram-project mr-1"></i>Marco NICE:</span>
                                        <span class="text-xs font-mono text-slate-400">${lvl.nice}</span>
                                    </div>
                                </div>
                            </div>
                        `).join('')}
                    </div>
                </div>
            `).join('');
        }

        // ============================================================
        // RENDER CERTS TABLE
        // ============================================================
        function renderCertsTable(data) {
            const tbody = document.getElementById('certTableBody');
            if (data.length === 0) {
                tbody.innerHTML = `<tr><td colspan="6" class="text-center py-8 text-slate-500"><i class="fa-solid fa-magnifying-glass text-2xl block mb-2"></i>No se encontraron certificaciones.</td></tr>`;
                return;
            }
            tbody.innerHTML = data.map(c => `
                <tr class="hover:bg-slate-800/40 transition-colors">
                    <td class="py-4 px-5 font-bold text-white font-mono"><i class="fa-solid fa-certificate text-cyan-400 mr-2"></i>${c.cert}</td>
                    <td class="py-4 px-5 text-slate-300">${c.org}</td>
                    <td class="py-4 px-5">
                        <span class="px-2.5 py-1 rounded text-xs font-mono font-semibold ${
                            c.level === 'Básico' ? 'bg-emerald-500/10 text-emerald-400 border border-emerald-500/20' :
                            c.level === 'Intermedio' ? 'bg-blue-500/10 text-blue-400 border border-blue-500/20' :
                            c.level === 'Avanzado' ? 'bg-purple-500/10 text-purple-400 border border-purple-500/20' :
                            'bg-amber-500/10 text-amber-400 border border-amber-500/20'
                        }">${c.level}</span>
                    </td>
                    <td class="py-4 px-5 text-slate-300">${c.area}</td>
                    <td class="py-4 px-5 text-slate-400">${c.req}</td>
                    <td class="py-4 px-5 text-slate-400 font-mono">${c.exp}</td>
                </tr>
            `).join('');
        }

        // ============================================================
        // RENDER GLOSSARY
        // ============================================================
        function renderGlossary(data) {
            const container = document.getElementById('glossaryContainer');
            if (data.length === 0) {
                container.innerHTML = `<div class="col-span-full text-center py-8 text-slate-500"><i class="fa-solid fa-magnifying-glass text-2xl block mb-2"></i>No se encontraron términos.</div>`;
                return;
            }
            container.innerHTML = data.map(g => `
                <div class="glossary-card p-5 bg-slate-900/80 border border-slate-800 rounded-xl space-y-2">
                    <div class="flex items-center justify-between">
                        <h3 class="font-bold text-cyan-400 font-mono">${g.term}</h3>
                        <span class="text-xs bg-slate-800 text-slate-400 px-2 py-0.5 rounded-full font-mono">${g.category}</span>
                    </div>
                    <p class="text-slate-300 leading-relaxed">${g.def}</p>
                </div>
            `).join('');
        }

        // ============================================================
        // TAB SWITCHING
        // ============================================================
        function switchTab(tabId) {
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('active', 'text-cyan-400', 'bg-slate-800/80', 'border', 'border-cyan-500/30');
                btn.classList.add('text-slate-400');
            });
            document.querySelectorAll('.tab-content').forEach(content => {
                content.classList.add('hidden');
            });

            const activeBtn = document.getElementById(`tab-${tabId}`);
            const activeContent = document.getElementById(`content-${tabId}`);

            if (activeBtn && activeContent) {
                activeBtn.classList.add('active', 'text-cyan-400', 'bg-slate-800/80', 'border', 'border-cyan-500/30');
                activeBtn.classList.remove('text-slate-400');
                activeContent.classList.remove('hidden');
            }
        }

        // ============================================================
        // NAVIGATE TO DOMAIN
        // ============================================================
        function goToDomain(domainId) {
            switchTab('domains');
            setTimeout(() => {
                document.querySelectorAll('.domain-filter-btn').forEach(btn => {
                    btn.classList.remove('active', 'bg-slate-800', 'text-white');
                    btn.classList.add('text-slate-400');
                });
                const filterBtns = document.querySelectorAll('.domain-filter-btn');
                filterBtns.forEach(btn => {
                    if (btn.getAttribute('onclick') && btn.getAttribute('onclick').includes(`'${domainId}'`)) {
                        btn.classList.add('active', 'bg-slate-800', 'text-white');
                        btn.classList.remove('text-slate-400');
                    }
                });
                applyDomainVisibility(domainId);
            }, 50);
        }

        function filterDomain(domainId, event) {
            document.querySelectorAll('.domain-filter-btn').forEach(btn => {
                btn.classList.remove('active', 'bg-slate-800', 'text-white');
                btn.classList.add('text-slate-400');
            });

            if (event && event.target) {
                event.target.classList.add('active', 'bg-slate-800', 'text-white');
                event.target.classList.remove('text-slate-400');
            }

            applyDomainVisibility(domainId);
        }

        function applyDomainVisibility(domainId) {
            const cards = document.querySelectorAll('.domain-card');
            cards.forEach(card => {
                if (domainId === 'all' || card.id === `domain-card-${domainId}`) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // ============================================================
        // CERT FILTER
        // ============================================================
        function applyCertFilters() {
            const level = document.getElementById('levelFilter').value;
            const area = document.getElementById('areaFilter').value;

            const filtered = certsData.filter(c => {
                const matchLevel = !level || c.level === level;
                const matchArea = !area || c.area.toLowerCase().includes(area.toLowerCase());
                return matchLevel && matchArea;
            });

            renderCertsTable(filtered);
        }

        // ============================================================
        // GLOBAL SEARCH
        // ============================================================
        document.getElementById('globalSearch').addEventListener('input', function(e) {
            const query = e.target.value.toLowerCase().trim();

            if (query.length > 0) {
                const currentTab = document.querySelector('.tab-btn.active');
                if (currentTab && currentTab.id !== 'tab-certs') {
                    switchTab('certs');
                }
            }

            if (!query) {
                renderCertsTable(certsData);
                applyDomainVisibility('all');
                document.querySelectorAll('.domain-filter-btn').forEach(btn => {
                    btn.classList.remove('active', 'bg-slate-800', 'text-white');
                    btn.classList.add('text-slate-400');
                });
                const todosBtn = document.querySelector('.domain-filter-btn');
                if (todosBtn) {
                    todosBtn.classList.add('active', 'bg-slate-800', 'text-white');
                    todosBtn.classList.remove('text-slate-400');
                }
                return;
            }

            const filteredCerts = certsData.filter(c => 
                c.cert.toLowerCase().includes(query) ||
                c.org.toLowerCase().includes(query) ||
                c.area.toLowerCase().includes(query) ||
                c.level.toLowerCase().includes(query)
            );
            renderCertsTable(filteredCerts);

            domainsData.forEach(d => {
                const card = document.getElementById(`domain-card-${d.id}`);
                const matches = JSON.stringify(d).toLowerCase().includes(query);
                if (card) {
                    card.style.display = matches ? 'block' : 'none';
                }
            });
        });

        // ============================================================
        // GLOSSARY SEARCH
        // ============================================================
        document.getElementById('glossarySearch').addEventListener('input', function(e) {
            const query = e.target.value.toLowerCase().trim();
            if (!query) {
                renderGlossary(glossaryData);
                return;
            }
            const filtered = glossaryData.filter(g => 
                g.term.toLowerCase().includes(query) ||
                g.def.toLowerCase().includes(query) ||
                g.category.toLowerCase().includes(query)
            );
            renderGlossary(filtered);
        });

        // ============================================================
        // INIT
        // ============================================================
        window.addEventListener('DOMContentLoaded', () => {
            renderDomains();
            renderCertsTable(certsData);
            renderGlossary(glossaryData);
        });
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EducateHer - Empowering Women Through Education</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Chart.js CDN -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
        body { font-family: 'Inter', sans-serif; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 flex flex-col min-h-screen">

    <!-- Navigation Header -->
    <header class="bg-indigo-900 text-white shadow-md sticky top-0 z-50">
        <div class="max-w-6xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-3">
                <div class="bg-pink-500 text-white p-2 rounded-lg font-bold text-xl">
                    <i class="fa-solid fa-graduation-cap"></i>
                </div>
                <div>
                    <h1 class="font-bold text-lg leading-tight">EducateHer</h1>
                    <p class="text-xs text-indigo-200">Open-Source Community Advocacy Platform</p>
                </div>
            </div>
            <a href="#github-section" class="bg-indigo-800 hover:bg-indigo-700 text-xs sm:text-sm px-3 py-1.5 rounded-full border border-indigo-600 transition flex items-center gap-2">
                <i class="fa-brands fa-github text-base"></i> <span class="hidden sm:inline">View Source</span>
            </a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="bg-gradient-to-br from-indigo-900 via-indigo-800 to-purple-900 text-white py-12 px-4">
        <div class="max-w-4xl mx-auto text-center space-y-4">
            <span class="inline-block bg-pink-500/20 text-pink-300 text-xs px-3 py-1 rounded-full font-medium border border-pink-500/30">
                Community & Education Initiative
            </span>
            <h2 class="text-2xl sm:text-4xl font-extrabold text-balance">
                Breaking Barriers: Prioritizing Education & Growth for Women
            </h2>
            <p class="text-indigo-100 text-sm sm:text-base max-w-2xl mx-auto font-light">
                Education and marriage are not mutually exclusive. Empowering women with access to learning builds stronger families, healthier communities, and resilient local economies.
            </p>
            <div class="flex flex-wrap justify-center gap-3 pt-2">
                <a href="#simulator" class="bg-pink-600 hover:bg-pink-500 text-white text-sm px-5 py-2.5 rounded-lg font-medium shadow-lg transition flex items-center gap-2">
                    <i class="fa-solid fa-chart-line"></i> Impact Simulator
                </a>
                <a href="#toolkit" class="bg-white/10 hover:bg-white/20 text-white text-sm px-5 py-2.5 rounded-lg font-medium border border-white/20 backdrop-blur-sm transition flex items-center gap-2">
                    <i class="fa-solid fa-bullhorn"></i> Outreach Toolkit
                </a>
            </div>
        </div>
    </section>

    <!-- Main Content Container -->
    <main class="max-w-6xl mx-auto px-4 py-8 space-y-12 flex-grow">

        <!-- Section 1: Impact Simulator -->
        <section id="simulator" class="bg-white rounded-2xl p-6 shadow-sm border border-slate-200 space-y-6">
            <div>
                <h3 class="text-xl font-bold text-indigo-950 flex items-center gap-2">
                    <i class="fa-solid fa-calculator text-indigo-600"></i> Education Impact Calculator
                </h3>
                <p class="text-sm text-slate-600 mt-1">
                    See how increasing secondary school completion rates among girls transforms household and community outcomes.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 items-center">
                <div class="space-y-4 bg-slate-50 p-4 rounded-xl border border-slate-100">
                    <label class="block text-sm font-semibold text-slate-700">
                        Target Education Rate for Girls (%):
                        <span id="rateValue" class="text-indigo-600 font-bold ml-1">70%</span>
                    </label>
                    <input type="range" id="rateInput" min="10" max="100" value="70" class="w-full accent-indigo-600 cursor-pointer">

                    <div class="space-y-3 pt-2 text-xs text-slate-600">
                        <div class="p-3 bg-white rounded-lg border border-slate-200 shadow-2xs">
                            <span class="block text-slate-500 font-medium">Est. Household Income Boost</span>
                            <span id="incomeBoost" class="text-base font-bold text-emerald-600">+14%</span>
                        </div>
                        <div class="p-3 bg-white rounded-lg border border-slate-200 shadow-2xs">
                            <span class="block text-slate-500 font-medium">Child Mortality Reduction</span>
                            <span id="healthBoost" class="text-base font-bold text-blue-600">-35%</span>
                        </div>
                    </div>
                </div>

                <div class="md:col-span-2 h-64">
                    <canvas id="impactChart"></canvas>
                </div>
            </div>
        </section>

        <!-- Section 2: Community Outreach Toolkit -->
        <section id="toolkit" class="space-y-4">
            <div>
                <h3 class="text-xl font-bold text-indigo-950 flex items-center gap-2">
                    <i class="fa-solid fa-bullhorn text-indigo-600"></i> Community Outreach Toolkit
                </h3>
                <p class="text-sm text-slate-600">
                    Ready-to-use dialogue scripts and talking points designed for local advocates, educators, and leaders.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <!-- Template 1 -->
                <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-2xs space-y-3">
                    <div class="flex justify-between items-center">
                        <span class="text-xs font-semibold uppercase tracking-wider text-indigo-600 bg-indigo-50 px-2.5 py-1 rounded-md">
                            Radio / Mosque / Church Brief
                        </span>
                        <button onclick="copyText('script1')" class="text-xs text-slate-500 hover:text-indigo-600 flex items-center gap-1">
                            <i class="fa-regular fa-copy"></i> Copy
                        </button>
                    </div>
                    <h4 class="font-bold text-slate-800 text-sm">Reframing Marriage & Learning</h4>
                    <p id="script1" class="text-xs text-slate-600 leading-relaxed bg-slate-50 p-3 rounded-lg border border-slate-100">
                        "An educated wife and mother is a pillar of strength for her family. When a woman learns to read, manage finances, and understand healthcare, her entire household thrives. Education doesn't compete with family values—it strengthens them."
                    </p>
                </div>

                <!-- Template 2 -->
                <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-2xs space-y-3">
                    <div class="flex justify-between items-center">
                        <span class="text-xs font-semibold uppercase tracking-wider text-pink-600 bg-pink-50 px-2.5 py-1 rounded-md">
                            Leader Talking Points
                        </span>
                        <button onclick="copyText('script2')" class="text-xs text-slate-500 hover:text-indigo-600 flex items-center gap-1">
                            <i class="fa-regular fa-copy"></i> Copy
                        </button>
                    </div>
                    <h4 class="font-bold text-slate-800 text-sm">Dialogue with Community Elders</h4>
                    <p id="script2" class="text-xs text-slate-600 leading-relaxed bg-slate-50 p-3 rounded-lg border border-slate-100">
                        "1. Educated women contribute directly to family financial resilience.<br>
                        2. Literacy improves child immunization and nutrition rates.<br>
                        3. Flexible and adult learning pathways allow women to study without neglecting family duties."
                    </p>
                </div>
            </div>
        </section>

        <!-- Section 3: Open-Source Repository Section -->
        <section id="github-section" class="bg-slate-900 text-white rounded-2xl p-6 sm:p-8 space-y-4 shadow-lg">
            <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4 border-b border-slate-800 pb-4">
                <div>
                    <h3 class="text-lg font-bold flex items-center gap-2">
                        <i class="fa-brands fa-github text-2xl text-pink-500"></i> Open-Source Project Information
                    </h3>
                    <p class="text-xs text-slate-400 mt-1">
                        Licensed under the MIT License. Free for global advocacy, research, and adaptation.
                    </p>
                </div>
                <span class="bg-emerald-500/10 text-emerald-400 text-xs font-semibold px-3 py-1 rounded-full border border-emerald-500/20">
                    MIT Open Source
                </span>
            </div>

            <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 text-xs">
                <div class="bg-slate-800/60 p-3.5 rounded-xl border border-slate-700/50">
                    <i class="fa-solid fa-code text-indigo-400 text-base mb-2 block"></i>
                    <strong class="block text-slate-200">Lightweight Architecture</strong>
                    <span class="text-slate-400">Pure HTML, Tailwind CSS, and Chart.js. No complex build tools required.</span>
                </div>
                <div class="bg-slate-800/60 p-3.5 rounded-xl border border-slate-700/50">
                    <i class="fa-solid fa-mobile-screen-button text-indigo-400 text-base mb-2 block"></i>
                    <strong class="block text-slate-200">Mobile First</strong>
                    <span class="text-slate-400">Optimized for fast rendering on mobile devices and low-bandwidth connections.</span>
                </div>
                <div class="bg-slate-800/60 p-3.5 rounded-xl border border-slate-700/50">
                    <i class="fa-solid fa-users text-indigo-400 text-base mb-2 block"></i>
                    <strong class="block text-slate-200">Community Driven</strong>
                    <span class="text-slate-400">Open for pull requests, regional translations, and policy additions.</span>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-white border-t border-slate-200 py-6 px-4 text-center text-xs text-slate-500 space-y-2">
        <p>© 2026 EducateHer Initiative. Open-source code available under the MIT License.</p>
        <p class="text-slate-400">Dedicated to promoting equal access to education for every woman and girl.</p>
    </footer>

    <!-- Interactive Script -->
    <script>
        // Chart Initialization
        const ctx = document.getElementById('impactChart').getContext('2d');
        const impactChart = new Chart(ctx, {
            type: 'bar',
            data: {
                labels: ['Household Income (%)', 'Child Health Index (%)', 'Community Literacy (%)'],
                datasets: [{
                    label: 'Impact Score',
                    data: [70 * 0.2, 70 * 0.5, 70],
                    backgroundColor: ['#10b981', '#3b82f6', '#8b5cf6'],
                    borderRadius: 6
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: { legend: { display: false } },
                scales: { y: { beginAtZero: true, max: 100 } }
            }
        });

        // Interactive Slider updates
        const rateInput = document.getElementById('rateInput');
        const rateValue = document.getElementById('rateValue');
        const incomeBoost = document.getElementById('incomeBoost');
        const healthBoost = document.getElementById('healthBoost');

        rateInput.addEventListener('input', (e) => {
            const val = e.target.value;
            rateValue.textContent = `${val}%`;
            incomeBoost.textContent = `+${Math.round(val * 0.2)}%`;
            healthBoost.textContent = `-${Math.round(val * 0.5)}%`;

            impactChart.data.datasets[0].data = [val * 0.2, val * 0.5, val];
            impactChart.update();
        });

        // Copy Helper
        function copyText(elementId) {
            const text = document.getElementById(elementId).innerText;
            navigator.clipboard.writeText(text);
            alert("Script copied to clipboard!");
        }
    </script>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infographic: The Dynamic Social Contract for Algorithmic Governance</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <script src="https://cdn.plot.ly/plotly-2.32.0.min.js" charset="utf-8"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0A192F;
            color: #E6F1FF;
        }
       .accent-text { color: #64FFDA; }
       .card {
            background-color: #112240;
            border: 1px solid #233554;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
       .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.2), 0 4px 6px -2px rgba(0, 0, 0, 0.1);
        }
       .stat-card {
            background: radial-gradient(circle, #112240 0%, #0A192F 100%);
        }
        h1, h2, h3 { font-weight: 700; }
       .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
           .chart-container {
                height: 350px;
            }
        }
       .framework-container {
            perspective: 1200px;
        }
       .framework-grid {
            transform: rotateX(10deg) rotateY(-5deg);
            transform-style: preserve-3d;
            transition: transform 0.5s ease;
        }
       .framework-container:hover.framework-grid {
            transform: rotateX(0) rotateY(0);
        }
       .framework-tier {
            background-color: rgba(35, 53, 84, 0.5);
            backdrop-filter: blur(5px);
            border: 1px solid #233554;
            transform: translateZ(0);
        }
       .framework-arrow {
            font-size: 2.5rem;
            line-height: 1;
            color: #64FFDA;
            text-shadow: 0 0 10px #64FFDA;
        }
       .gemini-button {
            background-color: #64FFDA;
            color: #0A192F;
            font-weight: bold;
            transition: all 0.3s ease;
        }
       .gemini-button:hover {
            background-color: #E6F1FF;
            box-shadow: 0 0 15px #64FFDA;
        }
       .gemini-button:disabled {
            background-color: #233554;
            color: #8892b0;
            cursor: not-allowed;
        }
       .gemini-response {
            background-color: #0A192F;
            border-left: 4px solid #64FFDA;
        }
    </style>
</head>
<body class="antialiased">

    <div class="max-w-7xl mx-auto p-4 sm:p-6 lg:p-8">
        
        <header class="text-center py-12">
            <h1 class="text-4xl md:text-6xl font-black tracking-tight text-white">The <span class="accent-text">Dynamic</span> Social Contract</h1>
            <h2 class="text-2xl md:text-4xl font-bold text-gray-300 mt-2">for Algorithmic Governance</h2>
            <p class="mt-6 max-w-3xl mx-auto text-lg text-gray-400">
                A new framework, grounded in empirical evidence, reveals that citizen consent for AI in public administration is not a one-time transaction, but a continuous, dynamic process. This infographic visualizes the core principles and data from this award-winning master's thesis.
            </p>
        </header>

        <main class="space-y-16 md:space-y-24">

            <section id="big-numbers" class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
                <div class="card stat-card rounded-xl p-8">
                    <p class="text-6xl md:text-7xl font-black accent-text">87%</p>
                    <p class="mt-2 text-xl font-semibold">Express Contingent Consent</p>
                    <p class="mt-2 text-gray-400">Acceptance of AI is conditional on robust human oversight and appeal processes.</p>
                </div>
                <div class="card stat-card rounded-xl p-8">
                    <p class="text-6xl md:text-7xl font-black accent-text">74%</p>
                    <p class="mt-2 text-xl font-semibold">Prioritize Fair Process</p>
                    <p class="mt-2 text-gray-400">Citizens value the fairness of the procedure over the efficiency of the outcome.</p>
                </div>
                 <div class="card stat-card rounded-xl p-8">
                    <p class="text-6xl md:text-7xl font-black accent-text">1.50</p>
                    <p class="mt-2 text-xl font-semibold">Cohen's d Effect Size</p>
                    <p class="mt-2 text-gray-400">An overwhelming public preference for hybrid human-AI models over full automation.</p>
                </div>
            </section>

            <hr class="border-gray-700">

            <section id="principle-1">
                <div class="text-center mb-12">
                    <h3 class="text-3xl md:text-4xl font-bold">Principle 1: <span class="accent-text">Graduated Legitimacy</span></h3>
                    <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-400">
                        This principle challenges classical theory by positing that legitimacy is not a binary state but exists on a continuum. Citizen consent is a fluctuating variable, conditional on context and safeguards.
                    </p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                    <div class="card rounded-xl p-6">
                        <h4 class="text-xl font-semibold text-center mb-4">Distribution of Citizen Consent</h4>
                        <div class="chart-container">
                            <canvas id="consentDistributionChart"></canvas>
                        </div>
                        <p class="text-center mt-4 text-sm text-gray-400">Figure 5.1: The `Authority_Consent_Scale` (Mean = 3.88, SD = 0.82) shows a normal distribution, refuting a simple accept/reject model and indicating nuanced, conditional acceptance.</p>
                    </div>
                    <div class="card rounded-xl p-6">
                        <h4 class="text-xl font-semibold text-center mb-4">The Nature of Consent</h4>
                        <div class="chart-container h-[300px] md:h-[350px]">
                             <canvas id="contingentConsentChart"></canvas>
                        </div>
                         <p class="text-center mt-4 text-sm text-gray-400">Figure 5.2: The vast majority of citizens (87%) express "Contingent Consent," linking their acceptance directly to procedural conditions like human review and appeals.</p>
                    </div>
                </div>
            </section>
            
            <hr class="border-gray-700">

            <section id="principle-2">
                <div class="text-center mb-12">
                    <h3 class="text-3xl md:text-4xl font-bold">Principle 2: <span class="accent-text">Procedural Primacy</span></h3>
                    <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-400">
                        In the face of complex "black box" algorithms, citizens rationally shift their focus to the fairness of the surrounding process. Procedural justice is the primary heuristic for granting legitimacy.
                    </p>
                </div>
                <div class="card rounded-xl p-6 md:p-8">
                     <h4 class="text-xl font-semibold text-center mb-4">Predictors of Legitimacy (3D View)</h4>
                     <div id="proceduralPrimacyChart" class="w-full h-[400px] md:h-[500px]"></div>
                     <p class="text-center mt-4 text-sm text-gray-400">Figure 5.3: This 3D regression analysis visualization shows that Perceived Oversight is the most significant positive predictor of Legitimacy ($\beta =.512, p <.001$), dwarfing other factors.</p>
                </div>
            </section>

            <hr class="border-gray-700">

            <section id="principle-3">
                 <div class="text-center mb-12">
                    <h3 class="text-3xl md:text-4xl font-bold">Principle 3: <span class="accent-text">Symbiotic Governance</span></h3>
                    <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-400">
                        Legitimacy requires a complementary relationship between human and artificial agents. The public rejects technocratic replacement, instead demanding a hybrid model that preserves human moral judgment.
                    </p>
                </div>
                 <div class="card rounded-xl p-6">
                    <h4 class="text-xl font-semibold text-center mb-4">Preference for Governance Models</h4>
                    <div class="chart-container h-[300px] md:h-[350px]">
                        <canvas id="governancePreferenceChart"></canvas>
                    </div>
                    <p class="text-center mt-4 text-sm text-gray-400">Figure 5.4: An overwhelming preference for Hybrid Models is demonstrated by a large effect size (Cohen's $d = 1.50$), indicating a profound public mandate for human-AI collaboration.</p>
                </div>
            </section>
            
            <hr class="border-gray-700">
            
            <section id="framework">
                <div class="text-center mb-12">
                    <h3 class="text-3xl md:text-4xl font-bold">The Framework: <span class="accent-text">A Three-Tier Architecture</span></h3>
                    <p class="mt-4 max-w-4xl mx-auto text-lg text-gray-400">
                        These principles converge into a multi-level framework that operationalizes the Dynamic Social Contract. Legitimacy is co-produced across micro, meso, and macro levels of governance. Hover over the diagram for a flat view.
                    </p>
                </div>
                <div class="framework-container">
                    <div class="framework-grid grid grid-cols-1 md:grid-cols-5 gap-6 items-center">
                        <div class="framework-tier md:col-span-2 rounded-xl p-6">
                            <h4 class="text-xl font-bold accent-text mb-2">Tier 1: Micro-Level</h4>
                            <p class="text-lg font-semibold mb-3">Citizen-Algorithm Interface</p>
                            <ul class="space-y-2 text-gray-300 list-disc list-inside">
                                <li>Procedural Justice Activation</li>
                                <li>Human Agency Preservation</li>
                                <li>Error Correction Pathways</li>
                            </ul>
                        </div>
                        <div class="text-center framework-arrow">→</div>
                        <div class="framework-tier md:col-span-2 rounded-xl p-6">
                             <h4 class="text-xl font-bold accent-text mb-2">Tier 2: Meso-Level</h4>
                            <p class="text-lg font-semibold mb-3">Institutional Mediation</p>
                             <ul class="space-y-2 text-gray-300 list-disc list-inside">
                                <li>Transparency-Trust Conversion</li>
                                <li>Contingent Consent Calibration</li>
                                <li>Feedback Architecture</li>
                            </ul>
                        </div>
                    </div>
                     <div class="flex justify-center my-6">
                        <div class="framework-arrow">↓</div>
                    </div>
                     <div class="flex justify-center">
                         <div class="framework-tier rounded-xl p-6 max-w-xl text-center">
                             <h4 class="text-xl font-bold accent-text mb-2">Tier 3: Macro-Level</h4>
                            <p class="text-lg font-semibold mb-3">Constitutional Principles</p>
                             <ul class="space-y-2 text-gray-300 list-disc list-inside sm:flex sm:space-y-0 sm:space-x-6 sm:justify-center">
                                <li>Human Sovereignty Primacy</li>
                                <li>Dynamic Legitimacy Auditing</li>
                                <li>Algorithmic Subsidiarity</li>
                            </ul>
                        </div>
                    </div>
                </div>
                 <p class="text-center mt-8 text-sm text-gray-400">Figure 5.5: The architecture of the Dynamic Social Contract, showing how legitimacy flows from individual interactions through institutional processes to foundational societal rules.</p>
            </section>

            <hr class="border-gray-700">

            <section id="gemini-sandbox">
                <div class="text-center mb-12">
                    <h3 class="text-3xl md:text-4xl font-bold"><span class="accent-text">AI Governance</span> Sandbox</h3>
                    <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-400">
                        Apply the framework yourself. Use these Gemini-powered tools to analyze scenarios, generate policy, and compare frameworks based on the principles of the Dynamic Social Contract.
                    </p>
                </div>
                <div class="space-y-8">
                    <div class="card rounded-xl p-6">
                        <h4 class="text-2xl font-bold mb-3">✨ Policy Scenario Simulator</h4>
                        <p class="text-gray-400 mb-4">Describe a plan to use AI in public administration. Gemini will analyze its potential impact on public trust through the lens of this thesis.</p>
                        <textarea id="scenario-input" class="w-full bg-gray-900 text-white p-3 rounded-md h-32 border border-gray-600 focus:ring-2 focus:ring-accent-text focus:outline-none" placeholder="e.g., 'The city will use an AI to review and approve business permit applications to speed up the process. Decisions will be instant.'"></textarea>
                        <button id="analyze-scenario-btn" class="gemini-button w-full py-2 px-4 rounded-md mt-4">Analyze Scenario</button>
                        <div id="scenario-output" class="mt-4"></div>
                    </div>
                    <div class="card rounded-xl p-6">
                        <h4 class="text-2xl font-bold mb-3">✨ Stakeholder Policy Generator</h4>
                        <p class="text-gray-400 mb-4">Select a stakeholder and a challenge to generate tailored policy recommendations based on the framework.</p>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div>
                                <label for="stakeholder-select" class="block text-sm font-medium text-gray-300">Stakeholder</label>
                                <select id="stakeholder-select" class="w-full bg-gray-900 text-white p-3 rounded-md mt-1 border border-gray-600 focus:ring-2 focus:ring-accent-text focus:outline-none">
                                    <option>Policymaker</option>
                                    <option>Public Administrator</option>
                                    <option>System Designer</option>
                                </select>
                            </div>
                            <div>
                                <label for="challenge-select" class="block text-sm font-medium text-gray-300">Challenge</label>
                                <select id="challenge-select" class="w-full bg-gray-900 text-white p-3 rounded-md mt-1 border border-gray-600 focus:ring-2 focus:ring-accent-text focus:outline-none">
                                    <option>Low Public Trust</option>
                                    <option>Algorithmic Bias Concerns</option>
                                    <option>Implementing Meaningful Oversight</option>
                                </select>
                            </div>
                        </div>
                        <button id="generate-policy-btn" class="gemini-button w-full py-2 px-4 rounded-md mt-4">Generate Policy Ideas</button>
                        <div id="policy-output" class="mt-4"></div>
                    </div>
                    <div class="card rounded-xl p-6">
                        <h4 class="text-2xl font-bold mb-3">✨ Comparative Framework Analysis</h4>
                        <p class="text-gray-400 mb-4">Compare the Dynamic Social Contract to other major AI governance frameworks to highlight its unique contributions.</p>
                        <div>
                            <label for="framework-select" class="block text-sm font-medium text-gray-300">Select framework to compare</label>
                            <select id="framework-select" class="w-full bg-gray-900 text-white p-3 rounded-md mt-1 border border-gray-600 focus:ring-2 focus:ring-accent-text focus:outline-none">
                                <option>NIST AI Risk Management Framework (RMF)</option>
                                <option>EU AI Act Principles</option>
                                <option>OECD AI Principles</option>
                            </select>
                        </div>
                        <button id="compare-framework-btn" class="gemini-button w-full py-2 px-4 rounded-md mt-4">Compare Frameworks</button>
                        <div id="comparison-output" class="mt-4"></div>
                    </div>
                </div>
            </section>
            
            <hr class="border-gray-700">
            
            <section id="implications">
                <div class="text-center mb-12">
                    <h3 class="text-3xl md:text-4xl font-bold"><span class="accent-text">Actionable</span> Implications</h3>
                    <p class="mt-4 max-w-3xl mx-auto text-lg text-gray-400">
                        This framework provides a clear roadmap for stakeholders to build and maintain legitimate AI systems in the public sphere.
                    </p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="card rounded-xl p-6">
                        <h4 class="text-2xl font-bold mb-3">For Policymakers</h4>
                        <p class="text-gray-300">Mandate robust procedural safeguards like independent audits, human oversight for high-stakes decisions, and accessible appeal processes. Focus regulatory energy on process, not just outcomes.</p>
                    </div>
                    <div class="card rounded-xl p-6">
                        <h4 class="text-2xl font-bold mb-3">For Public Administrators</h4>
                        <p class="text-gray-300">Invest in a "Transparency-Trust Conversion" function. Actively translate technical data into meaningful public explanations. Use segmented communication for different citizen priorities.</p>
                    </div>
                    <div class="card rounded-xl p-6">
                         <h4 class="text-2xl font-bold mb-3">For System Designers</h4>
                        <p class="text-gray-300">Adopt a "Symbiotic Governance" design philosophy. Center interfaces on human-AI collaboration. Design systems to facilitate dialogue, signal uncertainty, and seamlessly escalate complex cases to human judgment.</p>
                    </div>
                </div>
            </section>

        </main>
        
        <footer class="text-center mt-24 py-8 border-t border-gray-800">
            <p class="text-gray-500">Infographic based on the master's thesis research on the Dynamic Social Contract for Algorithmic Governance.</p>
             <p class="text-xs text-gray-600 mt-2">Visualizations generated with Chart.js and Plotly.js. No SVG or Mermaid JS used. Layout by Tailwind CSS.</p>
        </footer>

    </div>

    <script>
        const accentColor = '#64FFDA';
        const textColor = '#E6F1FF';
        const gridColor = 'rgba(200, 200, 200, 0.2)';

        function wrapLabel(str, maxWidth) {
            if (str.length <= maxWidth) {
                return str;
            }
            const words = str.split(' ');
            let lines =;
            let currentLine = words;

            for (let i = 1; i < words.length; i++) {
                if (currentLine.length + words[i].length + 1 < maxWidth) {
                    currentLine += ' ' + words[i];
                } else {
                    lines.push(currentLine);
                    currentLine = words[i];
                }
            }
            lines.push(currentLine);
            return lines;
        }

        const tooltipTitleCallback = (tooltipItems) => {
            const item = tooltipItems;
            let label = item.chart.data.labels[item.dataIndex];
            if (Array.isArray(label)) {
              return label.join(' ');
            } else {
              return label;
            }
        };
        
        const chartDefaults = {
            plugins: {
                legend: {
                    labels: { color: textColor }
                },
                tooltip: {
                    callbacks: {
                        title: tooltipTitleCallback
                    }
                }
            },
            scales: {
                y: {
                    ticks: { color: textColor },
                    grid: { color: gridColor }
                },
                x: {
                    ticks: { color: textColor },
                    grid: { color: gridColor }
                }
            },
            maintainAspectRatio: false,
        };

        const contingentConsentCtx = document.getElementById('contingentConsentChart').getContext('2d');
        new Chart(contingentConsentCtx, {
            type: 'doughnut',
            data: { labels: ['Contingent Consent', 'Other'], datasets: [{ label: 'Nature of Consent', data: , backgroundColor: [accentColor, '#233554'], borderColor: '#112240', borderWidth: 4, hoverOffset: 4 }] },
            options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { position: 'bottom', labels: { color: textColor, font: { size: 14 } } }, tooltip: { callbacks: { title: tooltipTitleCallback } } }, cutout: '60%' }
        });

        const consentDistributionCtx = document.getElementById('consentDistributionChart').getContext('2d');
        new Chart(consentDistributionCtx, {
            type: 'bar',
            data: { labels: ['1', '2', '3', '4', '5'], datasets:, backgroundColor: '#1D9BF0', borderColor: accentColor, borderWidth: 1 }] },
            options: {...chartDefaults, scales: { y: { display: false }, x: {...chartDefaults.scales.x, title: { display: true, text: 'Consent Score (1=Strongly Disagree, 5=Strongly Agree)', color: textColor }} }, plugins: {...chartDefaults.plugins, legend: { display: false } } }
        });

        const governancePreferenceCtx = document.getElementById('governancePreferenceChart').getContext('2d');
        new Chart(governancePreferenceCtx, {
            type: 'pie',
            data: { labels: ['Preference for Hybrid Models', 'Preference for Fully Automated Models'], datasets: [{ data: [92.5, 7.5], backgroundColor: [accentColor, '#233554'], borderColor: '#112240', borderWidth: 4, hoverOffset: 4 }] },
            options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { position: 'bottom', labels: { color: textColor, font: { size: 14 }, boxWidth: 20 } }, tooltip: { callbacks: { title: tooltipTitleCallback } } } }
        });

        const proceduralPrimacyChartDiv = document.getElementById('proceduralPrimacyChart');
        const plotlyData =, y: [0.512, 0.150, 0.080], z: [[1], [1], [1]], marker: { color:, line: { color: '#0A192F', width: 2 } }, transforms: [{ type: 'sort', target: 'y', order: 'descending' }] }];
        const plotlyLayout = { title: { text: 'Relative Predictive Power on Legitimacy (β-coefficients)', font: { color: textColor } }, font: { color: textColor }, paper_bgcolor: 'rgba(0,0,0,0)', plot_bgcolor: 'rgba(0,0,0,0)', scene: { xaxis: { title: 'Predictor Variable', color: textColor, gridcolor: gridColor, titlefont: { color: textColor } }, yaxis: { title: 'Standardized Beta (β)', color: textColor, gridcolor: gridColor, titlefont: { color: textColor } }, zaxis: { showticklabels: false, title: '' }, camera: { eye: {x: 1.8, y: 1.8, z: 0.5} } }, margin: { l: 0, r: 0, b: 0, t: 40 } };
        Plotly.newPlot(proceduralPrimacyChartDiv, plotlyData, plotlyLayout, {responsive: true});

        // Gemini API Integration
        const analyzeBtn = document.getElementById('analyze-scenario-btn');
        const scenarioInput = document.getElementById('scenario-input');
        const scenarioOutput = document.getElementById('scenario-output');
        
        const generateBtn = document.getElementById('generate-policy-btn');
        const stakeholderSelect = document.getElementById('stakeholder-select');
        const challengeSelect = document.getElementById('challenge-select');
        const policyOutput = document.getElementById('policy-output');

        const compareBtn = document.getElementById('compare-framework-btn');
        const frameworkSelect = document.getElementById('framework-select');
        const comparisonOutput = document.getElementById('comparison-output');

        const frameworkContext = `
            You are an expert in AI governance, analyzing scenarios based on the "Dynamic Social Contract" framework. This framework has three core principles:
            1.  **Graduated Legitimacy**: Citizen consent is not binary but exists on a spectrum. It's conditional on context and safeguards. High-stakes decisions require more robust justification.
            2.  **Procedural Primacy**: The perceived fairness of the process (like transparency, oversight, and appeals) is more critical for legitimacy than the outcome's efficiency.
            3.  **Symbiotic Governance**: Legitimate systems require a hybrid, complementary relationship between humans and AI, not a full replacement of human judgment, especially in morally complex situations.
        `;

        async function callGemini(prompt) {
            const apiKey = ""; 
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-flash-latest:generateContent?key=${apiKey}`;
            
            const payload = {
                contents: [{
                    role: "user",
                    parts: [{ text: prompt }]
                }]
            };

            const response = await fetch(apiUrl, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            });

            if (!response.ok) {
                throw new Error(`API call failed with status: ${response.status}`);
            }

            const result = await response.json();
            
            if (result.candidates && result.candidates.length > 0 && result.candidates.content && result.candidates.content.parts && result.candidates.content.parts.length > 0) {
                return result.candidates.content.parts.text;
            } else {
                console.error("Unexpected API response structure:", result);
                throw new Error("Could not extract text from API response.");
            }
        }

        function showLoading(button, outputElement, loadingText = 'Analyzing...') {
            button.disabled = true;
            button.textContent = loadingText;
            outputElement.innerHTML = `<div class="text-center p-4 text-gray-400">${loadingText}</div>`;
        }

        function hideLoading(button, originalText) {
            button.disabled = false;
            button.textContent = originalText;
        }
        
        function displayOutput(element, content) {
            element.innerHTML = `<div class="gemini-response p-4 rounded-md space-y-3">${content}</div>`;
        }

        function displayError(element, error) {
            element.innerHTML = `<div class="gemini-response p-4 rounded-md border-l-4 border-red-500"><p class="font-bold text-red-400">An error occurred</p><p class="text-red-300">${error.message}</p></div>`;
        }
        
        function formatGeminiResponse(text) {
             return text
               .replace(/(\*\*|__)(.*?)\1/g, '<strong class="accent-text">$2</strong>')
               .replace(/\* (.*?)(?=\n\*|\n\n|$)/g, '<li class="mb-2 ml-4 list-disc">$1</li>')
               .replace(/\n/g, '<br>');
        }

        analyzeBtn.addEventListener('click', async () => {
            const scenario = scenarioInput.value;
            if (!scenario.trim()) {
                displayError(scenarioOutput, { message: "Please enter a scenario to analyze." });
                return;
            }

            showLoading(analyzeBtn, scenarioOutput);

            const prompt = `
                ${frameworkContext}
                
                Analyze the following AI policy scenario based *strictly* on the three principles of the Dynamic Social Contract framework.

                **Scenario**: "${scenario}"

                Provide a brief, critical analysis for each principle, highlighting potential risks and strengths. Format your response with headings for each principle.
            `;

            try {
                const responseText = await callGemini(prompt);
                displayOutput(scenarioOutput, formatGeminiResponse(responseText));
            } catch (error) {
                console.error(error);
                displayError(scenarioOutput, error);
            } finally {
                hideLoading(analyzeBtn, 'Analyze Scenario');
            }
        });

        generateBtn.addEventListener('click', async () => {
            const stakeholder = stakeholderSelect.value;
            const challenge = challengeSelect.value;

            showLoading(generateBtn, policyOutput);
            
            const prompt = `
                ${frameworkContext}

                Act as an expert advisor. A **${stakeholder}** is facing the challenge of **"${challenge}"**. 
                
                Based *strictly* on the principles of the Dynamic Social Contract, generate 3-4 concrete, actionable policy ideas or recommendations for them. Present them as a bulleted list.
            `;
            
             try {
                const responseText = await callGemini(prompt);
                displayOutput(policyOutput, `<ul>${formatGeminiResponse(responseText)}</ul>`);
            } catch (error) {
                console.error(error);
                displayError(policyOutput, error);
            } finally {
                hideLoading(generateBtn, 'Generate Policy Ideas');
            }
        });

        compareBtn.addEventListener('click', async () => {
            const frameworkToCompare = frameworkSelect.value;

            showLoading(compareBtn, comparisonOutput, 'Comparing...');
            
            const prompt = `
                ${frameworkContext}

                Act as an academic expert in AI governance. Provide a concise but insightful comparison between the "Dynamic Social Contract" framework and the "${frameworkToCompare}".

                Structure your response with the following sections:
                - **Core Focus**: Briefly state the primary goal of each framework.
                - **Key Similarities**: Identify 1-2 points of overlap or shared goals.
                - **Key Differences**: Identify 1-2 major distinctions in their approach or principles.
                - **Unique Contribution of the Dynamic Social Contract**: Explain what the Dynamic Social Contract provides that the other framework does not explicitly focus on.
            `;
            
             try {
                const responseText = await callGemini(prompt);
                displayOutput(comparisonOutput, formatGeminiResponse(responseText));
            } catch (error) {
                console.error(error);
                displayError(comparisonOutput, error);
            } finally {
                hideLoading(compareBtn, 'Compare Frameworks');
            }
        });

    </script>
</body>
</html>

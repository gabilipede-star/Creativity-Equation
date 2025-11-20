<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Creativity Equation: A Mathematical Approach</title>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    <style>
        :root {
            --primary: #2c3e50;
            --accent: #3498db;
            --highlight: #e74c3c;
            --light: #ecf0f1;
            --text: #333;
            --sidebar-width: 280px;
        }

        * { box-sizing: border-box; }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.7;
            color: var(--text);
            margin: 0;
            display: flex;
            min-height: 100vh;
            background-color: #f9f9f9;
        }

        /* Sidebar Navigation */
        .sidebar {
            width: var(--sidebar-width);
            background: var(--primary);
            color: white;
            position: fixed;
            height: 100vh;
            padding: 2rem 1rem;
            display: flex;
            flex-direction: column;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 2rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .nav-btn {
            background: none;
            border: none;
            color: rgba(255,255,255,0.7);
            text-align: left;
            padding: 1rem;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 1rem;
            border-radius: 5px;
            margin-bottom: 0.5rem;
        }

        .nav-btn:hover, .nav-btn.active {
            background: rgba(255,255,255,0.1);
            color: white;
            padding-left: 1.5rem;
        }

        /* Main Content */
        .main-content {
            margin-left: var(--sidebar-width);
            flex: 1;
            padding: 3rem 4rem;
            max-width: 1200px;
        }

        .page-section {
            display: none;
            animation: fadeIn 0.5s;
        }

        .page-section.active {
            display: block;
        }

        h1 { font-size: 2.5rem; color: var(--primary); margin-bottom: 1rem; }
        h2 { font-size: 1.8rem; color: var(--accent); margin-top: 2.5rem; border-bottom: 2px solid #eee; padding-bottom: 10px;}
        h3 { font-size: 1.4rem; color: var(--primary); margin-top: 2rem; }

        /* Cards and Callouts */
        .card {
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
            margin-bottom: 2rem;
        }

        .example-box {
            background: #f0f8ff;
            border-left: 5px solid var(--accent);
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-radius: 0 5px 5px 0;
        }

        .math-pattern {
            font-family: 'Courier New', monospace;
            background: #333;
            color: #0f0;
            padding: 1rem;
            border-radius: 5px;
            margin-top: 1rem;
        }

        /* The Equation Lab Styles */
        .slider-container {
            margin: 20px 0;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            font-weight: bold;
            margin-bottom: 5px;
        }

        input[type=range] {
            width: 100%;
            height: 10px;
            border-radius: 5px;
            background: #d3d3d3;
            outline: none;
        }

        .result-box {
            text-align: center;
            background: var(--primary);
            color: white;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }

        .result-value {
            font-size: 3rem;
            font-weight: bold;
            color: #f1c40f;
        }

        /* Interactive Typology Grid */
        .type-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .type-card {
            background: white;
            border: 1px solid #eee;
            padding: 20px;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .type-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            border-color: var(--accent);
        }

        .type-card h4 { margin-top: 0; color: var(--primary); }
        
        .tag {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            font-weight: bold;
            margin-right: 5px;
        }
        .tag.high-p { background: #ffebee; color: #c62828; }
        .tag.low-p { background: #e8f5e9; color: #2e7d32; }

        /* Quiz Styles */
        .quiz-option {
            display: block;
            padding: 15px;
            border: 2px solid #eee;
            margin-bottom: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        .quiz-option:hover { background: #f9f9f9; border-color: #ccc; }
        .quiz-option.correct { background: #d4edda; border-color: #28a745; color: #155724; }
        .quiz-option.incorrect { background: #f8d7da; border-color: #dc3545; color: #721c24; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Responsive */
        @media (max-width: 768px) {
            body { flex-direction: column; }
            .sidebar { width: 100%; height: auto; position: relative; }
            .main-content { margin-left: 0; padding: 2rem; }
        }
    </style>
</head>
<body>

    <div class="sidebar">
        <div class="logo">The Creativity Equation</div>
        <button class="nav-btn active" onclick="showPage('intro')">1. The Three Variables</button>
        <button class="nav-btn" onclick="showPage('high-p')">2. High Probability Solutions</button>
        <button class="nav-btn" onclick="showPage('low-p')">3. Low Probability Solutions</button>
        <button class="nav-btn" onclick="showPage('equation')">4. The Lab: Calculator</button>
        <button class="nav-btn" onclick="showPage('implications')">5. Implications & Methods</button>
        <button class="nav-btn" onclick="showPage('quiz')">6. Quiz</button>
    </div>

    <div class="main-content">

        <div id="intro" class="page-section active">
            <h1>Understanding Creative Solutions</h1>
            <div class="card">
                <p>Most ideas are actually combinations of existing ideas. The Wright Brothers' airplane was bicycle mechanics + combustion engine + boat propeller. But what makes some combinations "creative" and others just "routine"?</p>
                <p>To understand this, we define the "DNA" of a solution using three variables.</p>
            </div>

            <h2>The Three Variables</h2>
            
            <div class="card">
                <h3>1. Probability ($p$)</h3>
                <p><strong>"Is it obvious?"</strong> This measures how likely you are to think of the idea immediately.</p>
                <div class="example-box">
                    <strong>High $p$ (Obvious):</strong> Drinking water when thirsty.<br>
                    <strong>Low $p$ (Rare):</strong> Drinking cactus juice when lost in the desert.
                </div>
            </div>

            <div class="card">
                <h3>2. Utility ($u$)</h3>
                <p><strong>"Does it work?"</strong> This measures whether the solution actually solves the problem.</p>
                <div class="example-box">
                    <strong>High $u$ (Works):</strong> Using a key to open a door.<br>
                    <strong>Low $u$ (Fails):</strong> Using a banana to open a door.
                </div>
            </div>

            <div class="card">
                <h3>3. Prior Knowledge ($v$)</h3>
                <p><strong>"Did you know it would work?"</strong> This is the most critical variable for creativity. It measures your knowledge <em>before</em> you try the solution.</p>
                <div class="example-box">
                    <strong>High $v$ (Certainty):</strong> You know your key will start your car.<br>
                    <strong>Low $v$ (Surprise):</strong> You wiggle a paperclip in a lock, not knowing if it will open. If it does, you are surprised!
                </div>
            </div>
            
            <button class="nav-btn" style="background: var(--accent); color: white; margin-top: 20px;" onclick="showPage('high-p')">Next: The Non-Creative Types &rarr;</button>
        </div>

        <div id="high-p" class="page-section">
            <h1>High Probability Solutions ($p \rightarrow 1$)</h1>
            <p>Before defining creativity, we must understand what is <em>not</em> creative. These are ideas that come quickly to mind.</p>

            <div class="type-grid">
                <div class="type-card">
                    <span class="tag high-p">Type 1</span>
                    <h4>Routine Ideas</h4>
                    <p>You know exactly what to do, and you know it works. This is valuable for daily life, but has zero creativity.</p>
                    <div class="math-pattern">
                        p → 1 (Obvious)<br>
                        u → 1 (Works)<br>
                        v → 1 (Known)
                    </div>
                    <p><em>Example: Your morning coffee routine.</em></p>
                </div>

                <div class="type-card">
                    <span class="tag high-p">Type 2</span>
                    <h4>Lucky Guesses</h4>
                    <p>Your first instinct works, but you had no reason to think it would. You learned nothing transferable.</p>
                    <div class="math-pattern">
                        p → 1 (Obvious)<br>
                        u → 1 (Works)<br>
                        v → 0 (Unknown)
                    </div>
                    <p><em>Example: Guessing a password on the first try.</em></p>
                </div>

                <div class="type-card">
                    <span class="tag high-p">Type 3</span>
                    <h4>Spinning Your Wheels</h4>
                    <p>Repeating a solution you know doesn't work, hoping for a different result. Irrational perseveration.</p>
                    <div class="math-pattern">
                        p → 1 (Obvious)<br>
                        u → 0 (Fails)<br>
                        v → 1 (Known failure)
                    </div>
                    <p><em>Example: Using the same bad study habits but expecting an A.</em></p>
                </div>

                <div class="type-card">
                    <span class="tag high-p">Type 4</span>
                    <h4>Problem Finding</h4>
                    <p>You try an obvious solution expecting it to work, but surprisingly, it fails. This reveals a new problem.</p>
                    <div class="math-pattern">
                        p → 1 (Obvious)<br>
                        u → 0 (Fails)<br>
                        v → 0 (Surprising failure)
                    </div>
                    <p><em>Example: Scientists using Newton's laws on Mercury's orbit, finding they didn't match.</em></p>
                </div>
            </div>
        </div>

        <div id="low-p" class="page-section">
            <h1>Low Probability Solutions ($p \rightarrow 0$)</h1>
            <p>These are ideas that are rare, ignored, or require time to emerge.</p>

            <div class="type-grid">
                <div class="type-card">
                    <span class="tag low-p">Type 5</span>
                    <h4>Smart Filtering</h4>
                    <p>You rationally avoid ideas because your prior knowledge tells you they are useless.</p>
                    <div class="math-pattern">
                        p → 0 (Rare)<br>
                        u → 0 (Useless)<br>
                        v → 1 (Known useless)
                    </div>
                    <p><em>Example: Einstein not putting clowns in his relativity equations.</em></p>
                </div>

                <div class="type-card">
                    <span class="tag low-p">Type 6</span>
                    <h4>Shooting Yourself in the Foot</h4>
                    <p>Irrational suppression. You avoid a useful solution even though you know it would help.</p>
                    <div class="math-pattern">
                        p → 0 (Avoided)<br>
                        u → 1 (Useful)<br>
                        v → 1 (Known useful)
                    </div>
                    <p><em>Example: Knowing exercise helps (u=1) but refusing to do it (p=0).</em></p>
                </div>

                <div class="type-card">
                    <span class="tag low-p">Type 7</span>
                    <h4>Mind-Wandering</h4>
                    <p>Random thoughts (shower thoughts). Most are useless, but you don't know until you check.</p>
                    <div class="math-pattern">
                        p → 0 (Random)<br>
                        u → 0 (Useless)<br>
                        v → 0 (Unknown)
                    </div>
                    <p><em>Example: Random daydreaming that leads nowhere.</em></p>
                </div>

                <div class="type-card" style="border: 2px solid gold; background: #fffdf0;">
                    <span class="tag low-p" style="background:gold; color:black;">Type 8</span>
                    <h4>CREATIVE SOLUTIONS</h4>
                    <p>The only path to genuine creativity.</p>
                    <div class="math-pattern">
                        p → 0 (Not Obvious)<br>
                        u → 1 (It Works!)<br>
                        v → 0 (Surprise!)
                    </div>
                    <p><em>Example: Edison's bamboo filament. He tested 1,600 things (blind trial) before finding one that worked.</em></p>
                </div>
            </div>
        </div>

        <div id="equation" class="page-section">
            <h1>The Creativity Equation Lab</h1>
            <p>We define creativity mathematically as:</p>
            <div style="font-size: 1.5rem; text-align: center; padding: 20px; background: white; border-radius: 10px;">
                $$ c = (1 - p) \times u \times (1 - v) $$
            </div>
            <p>Where:</p>
            <ul>
                <li>$(1-p)$ = <strong>Originality</strong> (The idea is rare)</li>
                <li>$u$ = <strong>Utility</strong> (The idea works)</li>
                <li>$(1-v)$ = <strong>Surprise</strong> (You didn't know it would work)</li>
            </ul>

            <div class="card">
                <h3>Simulator</h3>
                <p>Adjust the sliders to see how the variables affect the total creativity score. Notice how if <strong>any</strong> factor is zero, the total creativity becomes zero.</p>

                <div class="slider-container">
                    <div class="slider-label">
                        <span>Initial Probability (p) - How obvious is it?</span>
                        <span id="val-p">1.0</span>
                    </div>
                    <input type="range" min="0" max="1" step="0.1" value="1" id="slider-p" oninput="calculate()">
                    <div style="font-size: 0.9rem; color: #666;">High p = Obvious routine. Low p = Rare idea.</div>
                </div>

                <div class="slider-container">
                    <div class="slider-label">
                        <span>Utility (u) - Does it work?</span>
                        <span id="val-u">1.0</span>
                    </div>
                    <input type="range" min="0" max="1" step="0.1" value="1" id="slider-u" oninput="calculate()">
                    <div style="font-size: 0.9rem; color: #666;">High u = Solves the problem. Low u = Useless.</div>
                </div>

                <div class="slider-container">
                    <div class="slider-label">
                        <span>Prior Knowledge (v) - Did you know it would work?</span>
                        <span id="val-v">1.0</span>
                    </div>
                    <input type="range" min="0" max="1" step="0.1" value="1" id="slider-v" oninput="calculate()">
                    <div style="font-size: 0.9rem; color: #666;">High v = No surprise. Low v = Genuine discovery.</div>
                </div>

                <div class="result-box">
                    <div>Creativity Score ($c$)</div>
                    <div class="result-value" id="result-c">0.00</div>
                    <div id="result-text">Routine Idea (Not Creative)</div>
                </div>
            </div>
        </div>

        <div id="implications" class="page-section">
            <h1>Implications & Methods</h1>
            
            <div class="card">
                <h2>1. The "Blindness" Requirement</h2>
                <p>For an idea to be creative, you cannot know in advance whether it will work ($v \rightarrow 0$). If you already know the outcome, you are just applying expertise, not creating. This requires:</p>
                <ul>
                    <li><strong>Risk:</strong> Trying ideas that might fail.</li>
                    <li><strong>Uncertainty Tolerance:</strong> Being comfortable not knowing.</li>
                    <li><strong>Trial and Error:</strong> Testing to discover utility (like Edison).</li>
                </ul>
            </div>

            <div class="card">
                <h2>2. Incubation & Sightedness</h2>
                <p>Creativity is inversely related to "Sightedness" (seeing the answer clearly). To find creative solutions, you must venture into low-sightedness territory.</p>
                <p><strong>Incubation:</strong> Because creative ideas have low probability ($p \rightarrow 0$), they rarely come immediately. You often need to step away (sleep, walk, shower) to let the unconscious mind make connections.</p>
            </div>

            <div class="card">
                <h2>3. Generating Ideas</h2>
                <p>How do we generate these low probability ($p \rightarrow 0$), unknown utility ($v \rightarrow 0$) ideas? The document suggests many methods, all of which follow a "Generate then Test" pattern:</p>
                <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px;">
                    <div class="example-box">
                        <strong>Generation Phase</strong><br>
                        Mind Wandering<br>
                        Combinatorial Play<br>
                        Remote Association<br>
                        Serendipity
                    </div>
                    <div class="example-box" style="border-left-color: var(--highlight);">
                        <strong>Testing Phase</strong><br>
                        Verification<br>
                        Criticism<br>
                        Experimentation<br>
                        Refutation
                    </div>
                </div>
            </div>
        </div>

        <div id="quiz" class="page-section">
            <h1>Test Your Understanding</h1>
            <p>Categorize the following scenarios based on the 8-Fold Typology.</p>

            <div class="card">
                <h3>Scenario 1</h3>
                <p>You randomly guess a password and it works, despite having no reason to think that password was correct.</p>
                <div id="q1-options">
                    <div class="quiz-option" onclick="checkAnswer(this, true, 'Correct! High Probability (first guess), High Utility (works), Low Knowledge (pure luck).')">Lucky Guess</div>
                    <div class="quiz-option" onclick="checkAnswer(this, false, 'Incorrect. In a creative solution, probability is low (not your first guess).')">Creative Solution</div>
                    <div class="quiz-option" onclick="checkAnswer(this, false, 'Incorrect. Routine ideas require prior knowledge (you knew it would work).')">Routine Idea</div>
                </div>
                <p id="q1-feedback" style="font-weight: bold;"></p>
            </div>

            <div class="card">
                <h3>Scenario 2</h3>
                <p>Scientists used Newton's equations to predict Mercury's orbit, but the numbers didn't match observations. It failed surprisingly.</p>
                <div id="q2-options">
                    <div class="quiz-option" onclick="checkAnswer(this, false, 'Incorrect. Spinning wheels implies you knew it would fail but did it anyway.')">Spinning Your Wheels</div>
                    <div class="quiz-option" onclick="checkAnswer(this, true, 'Correct! High Probability (obvious method), Low Utility (failed), Low Knowledge (surprising failure).')">Problem Finding</div>
                    <div class="quiz-option" onclick="checkAnswer(this, false, 'Incorrect. Smart filtering happens before you try the solution.')">Smart Filtering</div>
                </div>
                <p id="q2-feedback" style="font-weight: bold;"></p>
            </div>

            <div class="card">
                <h3>Scenario 3</h3>
                <p>Picasso considered adding a specific color to <em>Guernica</em>, but realized based on his experience it wouldn't fit the emotional tone, so he never tried it.</p>
                <div id="q3-options">
                    <div class="quiz-option" onclick="checkAnswer(this, true, 'Correct! Low Probability (suppressed), Low Utility (wouldnt work), High Knowledge (he knew it).')">Smart Filtering</div>
                    <div class="quiz-option" onclick="checkAnswer(this, false, 'Incorrect. Routine ideas are executed, not suppressed.')">Routine Idea</div>
                    <div class="quiz-option" onclick="checkAnswer(this, false, 'Incorrect. He knew it would fail, so v is High.')">Problem Finding</div>
                </div>
                <p id="q3-feedback" style="font-weight: bold;"></p>
            </div>

        </div>

    </div>

    <script>
        // Page Navigation Logic
        function showPage(pageId) {
            // Hide all pages
            document.querySelectorAll('.page-section').forEach(page => {
                page.classList.remove('active');
            });
            // Show selected page
            document.getElementById(pageId).classList.add('active');
            
            // Update Sidebar Buttons
            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');

            // Scroll to top
            window.scrollTo(0,0);
        }

        // Calculator Logic
        function calculate() {
            const p = parseFloat(document.getElementById('slider-p').value);
            const u = parseFloat(document.getElementById('slider-u').value);
            const v = parseFloat(document.getElementById('slider-v').value);

            // Update labels
            document.getElementById('val-p').innerText = p.toFixed(1);
            document.getElementById('val-u').innerText = u.toFixed(1);
            document.getElementById('val-v').innerText = v.toFixed(1);

            // The Equation: c = (1-p) * u * (1-v)
            const c = (1 - p) * u * (1 - v);

            // Update Result
            document.getElementById('result-c').innerText = c.toFixed(3);

            // Interpret Result
            const resultText = document.getElementById('result-text');
            
            // Logic for naming the type based on variables (approximate)
            if (c > 0.1) {
                resultText.innerText = "CREATIVE SOLUTION!";
                resultText.style.color = "#f1c40f";
            } else if (p > 0.5 && u > 0.5 && v > 0.5) {
                resultText.innerText = "Routine Idea (Boring)";
                resultText.style.color = "white";
            } else if (p > 0.5 && u > 0.5 && v < 0.5) {
                resultText.innerText = "Lucky Guess";
                resultText.style.color = "white";
            } else if (u < 0.5 && v > 0.5) {
                resultText.innerText = "Useless / Known Failure";
                resultText.style.color = "#e74c3c";
            } else if (u < 0.5 && v < 0.5 && p > 0.5) {
                resultText.innerText = "Problem Finding (Surprising Failure)";
                resultText.style.color = "#3498db";
            } else {
                resultText.innerText = "Non-Creative Combination";
                resultText.style.color = "white";
            }
        }

        // Quiz Logic
        function checkAnswer(element, isCorrect, feedbackText) {
            const parent = element.parentElement;
            const feedbackEl = parent.nextElementSibling;
            
            // Reset colors
            Array.from(parent.children).forEach(child => {
                child.classList.remove('correct', 'incorrect');
            });

            if (isCorrect) {
                element.classList.add('correct');
                feedbackEl.style.color = '#155724';
            } else {
                element.classList.add('incorrect');
                feedbackEl.style.color = '#721c24';
            }
            feedbackEl.innerText = feedbackText;
        }

        // Initialize calculator
        calculate();
    </script>
</body>
</html># Creativity-Equation

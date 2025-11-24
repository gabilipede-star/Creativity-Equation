<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Creativity: The Simonton Equation</title>
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1e40af;
            --secondary: #64748b;
            --bg: #f8fafc;
            --surface: #ffffff;
            --text: #0f172a;
            --border: #e2e8f0;
            --success: #10b981;
            --danger: #ef4444;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', system-ui, sans-serif;
        }

        body {
            background: var(--bg);
            color: var(--text);
            display: flex;
            height: 100vh;
            overflow: hidden;
        }

        /* Sidebar Navigation */
        aside {
            width: 280px;
            background: var(--surface);
            border-right: 1px solid var(--border);
            display: flex;
            flex-direction: column;
            padding: 1.5rem;
            flex-shrink: 0;
            overflow-y: auto;
        }

        aside h1 {
            font-size: 1.25rem;
            color: var(--primary);
            margin-bottom: 2rem;
            font-weight: 800;
        }

        .nav-btn {
            background: transparent;
            border: none;
            text-align: left;
            padding: 1rem;
            margin-bottom: 0.5rem;
            border-radius: 0.5rem;
            color: var(--secondary);
            cursor: pointer;
            transition: all 0.2s;
            font-weight: 600;
        }

        .nav-btn:hover {
            background: #f1f5f9;
            color: var(--primary);
        }

        .nav-btn.active {
            background: var(--primary);
            color: white;
            box-shadow: 0 4px 6px -1px rgba(37, 99, 235, 0.2);
        }

        /* Main Content */
        main {
            flex: 1;
            overflow-y: auto;
            padding: 3rem;
            scroll-behavior: smooth;
        }

        .page {
            display: none;
            max-width: 900px;
            margin: 0 auto;
            animation: fadeIn 0.4s ease;
        }

        .page.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Typography & Elements */
        h2 { font-size: 2rem; margin-bottom: 1.5rem; color: var(--text); }
        h3 { font-size: 1.5rem; margin-top: 2rem; margin-bottom: 1rem; color: var(--primary-dark); }
        p { line-height: 1.7; margin-bottom: 1rem; color: #334155; }
        
        .highlight-box {
            background: #eff6ff;
            border-left: 4px solid var(--primary);
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-radius: 0 0.5rem 0.5rem 0;
        }

        .equation-box {
            background: var(--text);
            color: white;
            padding: 2rem;
            border-radius: 1rem;
            text-align: center;
            font-family: 'Courier New', monospace;
            font-size: 1.5rem;
            margin: 2rem 0;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }

        /* Type Cards */
        .grid-types {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .type-card {
            background: white;
            border: 1px solid var(--border);
            padding: 1.5rem;
            border-radius: 1rem;
            transition: transform 0.2s;
        }

        .type-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.05);
        }

        .type-card.creative {
            border: 2px solid var(--success);
            background: #f0fdf4;
        }

        .math-pattern {
            background: #f8fafc;
            padding: 1rem;
            border-radius: 0.5rem;
            font-family: monospace;
            margin-top: 1rem;
            font-size: 0.9rem;
            border: 1px solid var(--border);
        }

        .param-badge {
            display: inline-block;
            padding: 0.25rem 0.5rem;
            border-radius: 4px;
            font-weight: bold;
            font-size: 0.8rem;
            margin-right: 5px;
        }
        .bg-p { background: #dbeafe; color: #1e40af; }
        .bg-u { background: #dcfce7; color: #166534; }
        .bg-v { background: #fee2e2; color: #991b1b; }

        /* Quiz Styles */
        .quiz-item {
            background: white;
            padding: 1.5rem;
            border-radius: 0.5rem;
            margin-bottom: 1.5rem;
            border: 1px solid var(--border);
        }

        .quiz-options {
            display: grid;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .quiz-btn {
            padding: 1rem;
            border: 1px solid var(--border);
            background: var(--bg);
            text-align: left;
            cursor: pointer;
            border-radius: 0.5rem;
        }

        .quiz-btn:hover { background: #e2e8f0; }
        .quiz-btn.correct { background: #dcfce7; border-color: var(--success); }
        .quiz-btn.incorrect { background: #fee2e2; border-color: var(--danger); }

        /* Calculator */
        .slider-group { margin-bottom: 1.5rem; }
        input[type=range] { width: 100%; margin-top: 0.5rem; }

        @media (max-width: 768px) {
            body { flex-direction: column; overflow: auto; }
            aside { width: 100%; height: auto; padding: 1rem; }
            main { padding: 1.5rem; }
        }
    </style>
</head>
<body>

    <aside>
        <h1>Creativity Master</h1>
        <nav>
            <button class="nav-btn active" onclick="showPage('intro')">1. Introduction</button>
            <button class="nav-btn" onclick="showPage('variables')">2. The 3 Variables</button>
            <button class="nav-btn" onclick="showPage('types')">3. The 8 Types of Solutions</button>
            <button class="nav-btn" onclick="showPage('equation')">4. The Equation</button>
            <button class="nav-btn" onclick="showPage('process')">5. The Process (Incubation)</button>
            <button class="nav-btn" onclick="showPage('tools')">6. Tools & Techniques</button>
            <button class="nav-btn" onclick="showPage('quiz')">7. Quiz: Test Yourself</button>
        </nav>
    </aside>

    <main>
        
        <div id="intro" class="page active">
            <h2>Introduction: Solutions as Combinations</h2>
            <p>Most solutions are actually combinations of existing ideas[cite: 5]. Consider these famous examples:</p>
            <ul>
                <li><strong>The Wright Brothers' airplane:</strong> bicycle mechanics + combustion engine + boat propeller [cite: 6]</li>
                <li><strong>Watson and Crick's DNA model:</strong> X-ray crystallography + chemical bonding rules + double helix structure [cite: 7]</li>
            </ul>
            
            <div class="highlight-box">
                <p>For decades, researchers asked "What is creativity?" Professor Dean Keith Simonton discovered we've been asking the wrong question. Instead, we should first ask: <strong>"What makes a solution NOT creative?"</strong> [cite: 13-14]</p>
            </div>
        </div>

        <div id="variables" class="page">
            <h2>The "DNA" of a Solution</h2>
            <p>We can describe all solutions using three variables (0 to 1)[cite: 16]:</p>

            <div class="grid-types">
                <div class="type-card">
                    <h3>p (Probability)</h3>
                    <p><strong>"Is it obvious?"</strong> [cite: 18]</p>
                    <p>High p (→1): The idea is obvious. First thing that pops into your head. <br><em>Ex: Drinking water when thirsty.</em> [cite: 19-20]</p>
                    <p>Low p (→0): The idea is rare. <br><em>Ex: Drinking cactus juice in the desert.</em> [cite: 21-22]</p>
                </div>

                <div class="type-card">
                    <h3>u (Utility)</h3>
                    <p><strong>"Does it work?"</strong> [cite: 23]</p>
                    <p>High u (→1): Works perfectly. <br><em>Ex: Using a key to open a door.</em> [cite: 24-25]</p>
                    <p>Low u (→0): Fails completely. <br><em>Ex: Using a banana to open a door.</em> [cite: 26-27]</p>
                </div>

                <div class="type-card">
                    <h3>v (Prior Knowledge)</h3>
                    <p><strong>"Did you know it would work?"</strong> [cite: 28]</p>
                    <p>High v (→1): You knew it would work beforehand. No surprise. <br><em>Ex: Your car key starting your car.</em> [cite: 30-32]</p>
                    <p>Low v (→0): You had to test it to find out. <br><em>Ex: Wiggling a paperclip in a lock.</em> [cite: 33-35]</p>
                </div>
            </div>
            <div class="highlight-box">
                <p><strong>Crucial:</strong> v is the most important variable for creativity[cite: 28]. If you already know it will work (v→1), you are just executing expertise, not creating.</p>
            </div>
        </div>

        <div id="types" class="page">
            <h2>The 8 Types of Solutions</h2>
            <p>There are 7 types of non-creative solutions and only 1 type of creative solution[cite: 38].</p>

            <h3>Category 1: High Probability (Obvious Ideas) [cite: 41]</h3>
            
            <div class="grid-types">
                <div class="type-card">
                    <h4>1. Routine Ideas</h4>
                    <p>Habitual responses. You know what to do, and it works. <br><em>Ex: Your morning coffee routine.</em> [cite: 42-45]</p>
                    <div class="math-pattern">
                        p→1 (Immediate)<br>
                        u→1 (Works)<br>
                        v→1 (Known) [cite: 49-52]
                    </div>
                </div>

                <div class="type-card">
                    <h4>2. Lucky Guesses</h4>
                    <p>Your first instinct works, but you didn't know it would. <br><em>Ex: Guessing a birth year as a password.</em> [cite: 53-56]</p>
                    <div class="math-pattern">
                        p→1 (First instinct)<br>
                        u→1 (Works)<br>
                        v→0 (Unknown) [cite: 62-65]
                    </div>
                </div>

                <div class="type-card">
                    <h4>3. Spinning Your Wheels</h4>
                    <p>Irrational Perseveration. Repeating a failed solution hoping for a different result. <br><em>Ex: Returning to a toxic relationship.</em> [cite: 66-71]</p>
                    <div class="math-pattern">
                        p→1 (Habitual)<br>
                        u→0 (Fails)<br>
                        v→1 (You know it fails) [cite: 75-78]
                    </div>
                </div>

                <div class="type-card">
                    <h4>4. Problem Finding</h4>
                    <p>You expect it to work, but surprisingly it fails. This reveals a new problem. <br><em>Ex: Mercury's orbit violating Newton's laws.</em> [cite: 79-84]</p>
                    <div class="math-pattern">
                        p→1 (Obvious)<br>
                        u→0 (Fails)<br>
                        v→0 (Surprise failure) [cite: 92-95]
                    </div>
                </div>
            </div>

            <h3>Category 2: Low Probability (Rare Ideas) [cite: 97]</h3>

            <div class="grid-types">
                <div class="type-card">
                    <h4>5. Smart Filtering</h4>
                    <p>Rational Suppression. Avoiding ideas you know are useless. <br><em>Ex: Einstein not putting clowns in his equations.</em> [cite: 98-100]</p>
                    <div class="math-pattern">
                        p→0 (Avoided)<br>
                        u→0 (Useless)<br>
                        v→1 (Known useless) [cite: 107-110]
                    </div>
                </div>

                <div class="type-card">
                    <h4>6. Shooting Yourself in the Foot</h4>
                    <p>Irrational Suppression. Avoiding useful ideas you know would work. <br><em>Ex: Refusing to exercise despite doctor's orders.</em> [cite: 111-115]</p>
                    <div class="math-pattern">
                        p→0 (Avoided)<br>
                        u→1 (Useful)<br>
                        v→1 (Known useful) [cite: 118-121]
                    </div>
                </div>

                <div class="type-card">
                    <h4>7. Mind-Wandering</h4>
                    <p>Random daydreams. Mostly useless, but occasionally magical. <br><em>Ex: Random shower thoughts.</em> [cite: 122-127]</p>
                    <div class="math-pattern">
                        p→0 (Random)<br>
                        u→0 (Useless)<br>
                        v→0 (Unknown) [cite: 128-131]
                    </div>
                </div>

                <div class="type-card creative">
                    <h4>8. CREATIVE SOLUTIONS</h4>
                    <p>The Golden Combination. <br><em>Ex: Edison's bamboo filament.</em> [cite: 140-146]</p>
                    <ul>
                        <li><strong>Low p:</strong> Not obvious (Edison tried 1600+ things).</li>
                        <li><strong>High u:</strong> It actually works.</li>
                        <li><strong>Low v:</strong> Genuine surprise (Blind to utility).</li>
                    </ul>
                    <div class="math-pattern">
                        p→0 (Original)<br>
                        u→1 (Useful)<br>
                        v→0 (Surprising) [cite: 150-153]
                    </div>
                </div>
            </div>
        </div>

        <div id="equation" class="page">
            <h2>The Mathematical Formula</h2>
            
            <div class="equation-box">
                c = (1 - p) × u × (1 - v)
            </div>
            
            <p>Where:<br>
            <strong>(1 - p)</strong> = Originality [cite: 165]<br>
            <strong>u</strong> = Utility [cite: 166]<br>
            <strong>(1 - v)</strong> = Surprise [cite: 167]</p>

            <div class="highlight-box">
                <h3>Why Multiplication?</h3>
                <p>Because each factor is <strong>necessary but not sufficient</strong>[cite: 171]. If ANY factor is zero, the total creativity is zero.</p>
                <p><em>Example:</em> A <strong>perpetual motion machine</strong> is highly original and surprising, but because it violates physics (u=0), it has <strong>zero creativity</strong>. Multiplication captures this "veto power." [cite: 178-179]</p>
            </div>

            <div class="type-card">
                <h3>Try the Calculator</h3>
                <p>Adjust the sliders to see how creativity changes.</p>
                
                <div class="slider-group">
                    <label>Originality (1-p): <span id="val-p">0.5</span></label>
                    <input type="range" id="input-p" min="0" max="1" step="0.1" value="0.5" oninput="calc()">
                </div>
                <div class="slider-group">
                    <label>Utility (u): <span id="val-u">0.5</span></label>
                    <input type="range" id="input-u" min="0" max="1" step="0.1" value="0.5" oninput="calc()">
                </div>
                <div class="slider-group">
                    <label>Surprise (1-v): <span id="val-v">0.5</span></label>
                    <input type="range" id="input-v" min="0" max="1" step="0.1" value="0.5" oninput="calc()">
                </div>
                
                <h3 style="text-align: center;">Creativity Score (c) = <span id="result-c" style="color: var(--primary);">0.125</span></h3>
            </div>
            <p><em>Note: Mathematically, high creativity scores are extremely rare because you are multiplying three decimals. [cite: 300-302]</em></p>
        </div>

        <div id="process" class="page">
            <h2>The Process: Incubation & Sightedness</h2>
            
            <div class="highlight-box">
                <h3>Creativity and "Sightedness" are Opposites</h3>
                <p>As sightedness (knowing what to do) increases, creativity decreases. To be creative, you must venture into territory where you don't know if ideas will work (v→0) and they aren't obvious (p→0). [cite: 296-298]</p>
            </div>

            <h3>The Role of Incubation</h3>
            <p>Ideas that require incubation tend to be more creative. [cite: 254]</p>
            <p><strong>Wallas' Four Stages (1926):</strong></p>
            <ol>
                <li><strong>Preparation:</strong> Gather info, define problem. [cite: 257]</li>
                <li><strong>Incubation:</strong> Step away. Unconscious work. p shifts from 1 to 0. [cite: 258-260]</li>
                <li><strong>Illumination:</strong> The "Aha!" moment. [cite: 261]</li>
                <li><strong>Verification:</strong> Test it (discover u). [cite: 263]</li>
            </ol>
            
            <p><strong>Takeaway:</strong> You must be "blind to eventual utility." If you already know it works, it's not creative. [cite: 276]</p>
        </div>

        <div id="tools" class="page">
            <h2>Tools & Techniques</h2>
            <p>Where do ideas come from? Scientists list many tools, but they all share one thing: they help generate ideas where you don't know the utility in advance (v→0). You generate, then test. [cite: 336-337]</p>
            
            <h3>Common Techniques [cite: 315-334]:</h3>
            <ul style="column-count: 2; gap: 2rem;">
                <li>Remote Association</li>
                <li>Bisociation of Matrices</li>
                <li>Combinatorial Play</li>
                <li>Divergent Thinking</li>
                <li>Abductive Reasoning</li>
                <li>Mind Wandering</li>
                <li>Serendipity</li>
                <li>Tinkering</li>
            </ul>

            <div class="highlight-box">
                <h3>Focus for this Class:</h3>
                <p>We will focus on two specific methods [cite: 339-342]:</p>
                <ol>
                    <li><strong>Pursuing your interests:</strong> Why this helps generate solutions.</li>
                    <li><strong>Story:</strong> Why storytelling helps discover creative solutions.</li>
                </ol>
            </div>
        </div>

        <div id="quiz" class="page">
            <h2>Exercise: Categorize These Solutions</h2>
            <p>Identify which of the 8 types these scenarios represent [cite: 344-352].</p>

            <div class="quiz-item">
                <p><strong>Scenario A:</strong> You solve a crossword puzzle clue immediately because you know the answer. [cite: 346]</p>
                <div class="quiz-options">
                    <button class="quiz-btn" onclick="check(this, true)">Routine Idea (p→1, u→1, v→1)</button>
                    <button class="quiz-btn" onclick="check(this, false)">Lucky Guess (p→1, u→1, v→0)</button>
                    <button class="quiz-btn" onclick="check(this, false)">Creative Solution (p→0, u→1, v→0)</button>
                </div>
            </div>

            <div class="quiz-item">
                <p><strong>Scenario B:</strong> You randomly guess a password and it works, despite having no reason to think it was correct. [cite: 347]</p>
                <div class="quiz-options">
                    <button class="quiz-btn" onclick="check(this, false)">Routine Idea</button>
                    <button class="quiz-btn" onclick="check(this, true)">Lucky Guess (p→1, u→1, v→0)</button>
                    <button class="quiz-btn" onclick="check(this, false)">Problem Finding</button>
                </div>
            </div>

            <div class="quiz-item">
                <p><strong>Scenario C:</strong> A scientist keeps using a disproven theory because they refuse to accept it's wrong. [cite: 348]</p>
                <div class="quiz-options">
                    <button class="quiz-btn" onclick="check(this, false)">Problem Finding</button>
                    <button class="quiz-btn" onclick="check(this, true)">Spinning Your Wheels (p→1, u→0, v→1)</button>
                    <button class="quiz-btn" onclick="check(this, false)">Smart Filtering</button>
                </div>
            </div>

            <div class="quiz-item">
                <p><strong>Scenario D:</strong> You try to open a stuck jar using your usual method, but surprisingly it doesn't work this time. [cite: 349]</p>
                <div class="quiz-options">
                    <button class="quiz-btn" onclick="check(this, true)">Problem Finding (p→1, u→0, v→0)</button>
                    <button class="quiz-btn" onclick="check(this, false)">Creative Solution</button>
                    <button class="quiz-btn" onclick="check(this, false)">Spinning Your Wheels</button>
                </div>
            </div>
            
             <div class="quiz-item">
                <p><strong>Scenario E:</strong> You know exercising would improve your health, but you never do it. [cite: 350]</p>
                <div class="quiz-options">
                    <button class="quiz-btn" onclick="check(this, false)">Smart Filtering</button>
                    <button class="quiz-btn" onclick="check(this, true)">Shooting Yourself in the Foot (p→0, u→1, v→1)</button>
                    <button class="quiz-btn" onclick="check(this, false)">Mind Wandering</button>
                </div>
            </div>
            
             <div class="quiz-item">
                <p><strong>Scenario F:</strong> Picasso considered adding a color to Guernica, tested it, realized it didn't fit, and filtered it out. [cite: 351]</p>
                <div class="quiz-options">
                    <button class="quiz-btn" onclick="check(this, true)">Smart Filtering (p→0, u→0, v→1)</button>
                    <button class="quiz-btn" onclick="check(this, false)">Shooting Yourself in the Foot</button>
                    <button class="quiz-btn" onclick="check(this, false)">Creative Solution</button>
                </div>
            </div>

        </div>

    </main>

    <script>
        // Navigation Logic
        function showPage(pageId) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            document.getElementById(pageId).classList.add('active');
            
            document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
            event.target.classList.add('active');
        }

        // Calculator Logic
        function calc() {
            let p = parseFloat(document.getElementById('input-p').value);
            let u = parseFloat(document.getElementById('input-u').value);
            let v = parseFloat(document.getElementById('input-v').value);

            document.getElementById('val-p').innerText = p.toFixed(1);
            document.getElementById('val-u').innerText = u.toFixed(1);
            document.getElementById('val-v').innerText = v.toFixed(1);

            // c = (1-p) * u * (1-v) -- NOTE: Inputs are already "Originality", "Utility", "Surprise"
            // Wait, slider labels say "Originality (1-p)". So the input value IS the term (1-p).
            // Let's fix logic: The equation is c = Org * Util * Surp.
            let c = p * u * v; 
            document.getElementById('result-c').innerText = c.toFixed(3);
        }

        // Quiz Logic
        function check(btn, isCorrect) {
            // Reset siblings
            let parent = btn.parentElement;
            let siblings = parent.getElementsByClassName('quiz-btn');
            for(let sib of siblings) {
                sib.classList.remove('correct', 'incorrect');
            }

            if(isCorrect) {
                btn.classList.add('correct');
                btn.innerText += " ✅ Correct!";
            } else {
                btn.classList.add('incorrect');
                btn.innerText += " ❌ Try again";
            }
        }
        
        // Init calc
        calc();
    </script>
</body>
</html>

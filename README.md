<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Hamna Munir · GitHub Profile</title>
    <!-- Font Awesome (for icons) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Fira Code', system-ui, sans-serif;
        }

        body {
            background: #f7f3eb;
            color: #3c2f1f;
            padding: 2rem 1rem;
            display: flex;
            justify-content: center;
        }

        .container {
            max-width: 1000px;
            width: 100%;
            background: #fcf9f5;
            border-radius: 28px;
            box-shadow: 0 12px 40px rgba(100, 70, 40, 0.12);
            padding: 2.5rem 2rem;
            border: 1px solid #d9c8b0;
        }

        /* --- Typography --- */
        h1,
        h2,
        h3 {
            font-weight: 600;
            letter-spacing: -0.02em;
        }

        h1 {
            font-size: 2.4rem;
            color: #7a5a3a;
            display: flex;
            align-items: center;
            gap: 10px;
            flex-wrap: wrap;
        }

        h1 small {
            font-size: 1rem;
            font-weight: 400;
            color: #a58363;
            margin-left: 6px;
        }

        h2 {
            font-size: 1.5rem;
            color: #6b4e30;
            border-bottom: 2px solid #e2d2be;
            padding-bottom: 0.4rem;
            margin: 2rem 0 1.2rem 0;
        }

        h3 {
            font-size: 1.1rem;
            color: #7a5a3a;
            margin-bottom: 0.5rem;
        }

        a {
            color: #8b6a47;
            text-decoration: none;
            font-weight: 500;
            transition: 0.2s;
        }

        a:hover {
            color: #b58b5f;
            text-decoration: underline;
        }

        .badge-gold {
            background: #d9b382;
            color: #2d1f11;
            padding: 0.15rem 0.8rem;
            border-radius: 30px;
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 0.3px;
            text-transform: uppercase;
            display: inline-block;
        }

        /* --- Header / Profile --- */
        .profile-header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .profile-left {
            display: flex;
            align-items: center;
            gap: 18px;
            flex-wrap: wrap;
        }

        .avatar {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: #d9c8b0;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.8rem;
            font-weight: 600;
            color: #5a3f28;
            border: 3px solid #c6a887;
            box-shadow: 0 4px 12px rgba(140, 100, 60, 0.15);
            background: #e7d7c4;
        }

        .profile-meta {
            display: flex;
            flex-wrap: wrap;
            gap: 8px 18px;
            color: #5f4935;
            font-size: 0.95rem;
        }

        .profile-meta i {
            color: #a58363;
            width: 20px;
        }

        .follow-btn {
            background: #b58b5f;
            color: #fcf9f5;
            border: none;
            padding: 0.5rem 1.6rem;
            border-radius: 40px;
            font-weight: 600;
            font-size: 0.9rem;
            cursor: default;
            box-shadow: 0 4px 8px rgba(160, 120, 70, 0.2);
            letter-spacing: 0.3px;
        }

        /* --- Who Am I / About cards --- */
        .whoami-grid {
            background: #f4ede6;
            border-radius: 20px;
            padding: 1.2rem 1.6rem;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(170px, 1fr));
            gap: 6px 20px;
            border-left: 6px solid #b58b5f;
            margin: 1.2rem 0 1.8rem 0;
        }

        .whoami-grid span {
            font-weight: 400;
            color: #3c2f1f;
            padding: 0.2rem 0;
        }

        .whoami-grid strong {
            color: #7a5a3a;
            font-weight: 600;
            display: inline-block;
            min-width: 80px;
        }

        .whoami-grid .label {
            color: #8f7357;
            font-weight: 500;
        }

        /* --- Tech Stack --- */
        .tech-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 18px 28px;
            margin: 1rem 0 0.2rem 0;
        }

        .tech-category {
            background: #f4ede6;
            border-radius: 16px;
            padding: 0.8rem 1.2rem;
            flex: 1 1 160px;
            border: 1px solid #e2d2be;
        }

        .tech-category h4 {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.6px;
            color: #a58363;
            margin-bottom: 6px;
        }

        .tech-tag {
            display: inline-block;
            background: #e7d7c4;
            color: #3c2f1f;
            padding: 0.2rem 0.8rem;
            border-radius: 30px;
            font-size: 0.8rem;
            font-weight: 500;
            margin: 0.2rem 0.2rem 0 0;
            border: 1px solid #d9c8b0;
        }

        .tech-tag i {
            margin-right: 4px;
            color: #8b6a47;
        }

        /* --- Stats Cards --- */
        .stats-row {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin: 1.8rem 0 1rem 0;
        }

        .stat-card {
            background: #f4ede6;
            border-radius: 20px;
            padding: 0.8rem 1.5rem;
            flex: 1 1 120px;
            border: 1px solid #e2d2be;
            text-align: center;
        }

        .stat-number {
            font-size: 2rem;
            font-weight: 700;
            color: #7a5a3a;
            line-height: 1.2;
        }

        .stat-label {
            font-size: 0.8rem;
            color: #8f7357;
            font-weight: 500;
        }

        /* --- Contribution Graph (simulated) --- */
        .graph-placeholder {
            background: #f4ede6;
            border-radius: 20px;
            padding: 1.2rem 1.5rem;
            margin: 1.2rem 0;
            border: 1px solid #e2d2be;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
        }

        .graph-bars {
            display: flex;
            align-items: flex-end;
            gap: 6px;
            flex-wrap: wrap;
            margin: 0.5rem 0;
        }

        .bar {
            width: 28px;
            background: #d9c8b0;
            border-radius: 6px 6px 0 0;
            transition: 0.2s;
            min-height: 10px;
        }

        .bar.gold {
            background: #c6a887;
        }

        .bar.dark {
            background: #b58b5f;
        }

        .graph-legend {
            font-size: 0.75rem;
            color: #6b4e30;
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
        }

        /* --- Currently working on (table) --- */
        .work-table {
            width: 100%;
            border-collapse: collapse;
            background: #f4ede6;
            border-radius: 16px;
            overflow: hidden;
            margin: 1rem 0;
        }

        .work-table td {
            padding: 0.8rem 1.2rem;
            border-bottom: 1px solid #e2d2be;
            font-size: 0.95rem;
        }

        .work-table tr:last-child td {
            border-bottom: none;
        }

        .work-table td:first-child {
            font-weight: 600;
            color: #6b4e30;
        }

        .work-table td:last-child {
            color: #5f4935;
        }

        /* --- Quote --- */
        .quote-box {
            background: #f4ede6;
            border-radius: 20px;
            padding: 1.2rem 1.8rem;
            margin: 1.8rem 0 1.2rem 0;
            border-left: 6px solid #b58b5f;
            font-style: italic;
            color: #3c2f1f;
        }

        .quote-box i {
            color: #b58b5f;
            margin-right: 8px;
        }

        .quote-author {
            font-style: normal;
            font-weight: 500;
            color: #7a5a3a;
            margin-top: 4px;
        }

        /* --- Connect / footer --- */
        .connect-links {
            display: flex;
            flex-wrap: wrap;
            gap: 18px 30px;
            margin: 1.8rem 0 0.6rem 0;
            padding-top: 1rem;
            border-top: 2px solid #e2d2be;
        }

        .connect-links a {
            font-size: 1rem;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: #f4ede6;
            padding: 0.4rem 1.2rem;
            border-radius: 40px;
            border: 1px solid #d9c8b0;
            transition: 0.15s;
            color: #5f4935;
        }

        .connect-links a:hover {
            background: #e7d7c4;
            border-color: #b58b5f;
            color: #3c2f1f;
            text-decoration: none;
        }

        .connect-links i {
            color: #b58b5f;
        }

        .footer-note {
            text-align: center;
            color: #8f7357;
            font-size: 0.85rem;
            margin-top: 2rem;
            letter-spacing: 0.3px;
        }

        /* responsive */
        @media (max-width: 600px) {
            .container {
                padding: 1.2rem;
            }
            h1 {
                font-size: 1.8rem;
            }
            .profile-left {
                gap: 12px;
            }
            .avatar {
                width: 60px;
                height: 60px;
                font-size: 2rem;
            }
            .follow-btn {
                padding: 0.3rem 1rem;
                font-size: 0.8rem;
            }
            .whoami-grid {
                grid-template-columns: 1fr;
                padding: 1rem;
            }
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- ===== HEADER ===== -->
        <div class="profile-header">
            <div class="profile-left">
                <div class="avatar">MA</div>
                <div>
                    <h1>
                        Maria Aqdas
                        <small>she/her</small>
                    </h1>
                    <div class="profile-meta">
                        <span><i class="fas fa-map-pin"></i> Faisalabad</span>
                        <span><i class="fas fa-envelope"></i> maria.aqdas@example.com</span>
                        <span><i class="fas fa-globe"></i> <a href="#">maria-aqdas.dev</a></span>
                        <span><i class="fab fa-github"></i> <a href="#">maria-aqdas</a></span>
                    </div>
                </div>
            </div>
            <div>
                <span class="follow-btn"><i class="fas fa-user-plus"></i> Follow</span>
            </div>
        </div>

        <!-- subtitle -->
        <p style="font-size:1.1rem; color:#5f4935; margin-bottom:0.2rem;">
            <i class="fas fa-code" style="color:#b58b5f;"></i>
            Transforming Raw Data into Insights &nbsp;·&nbsp; Python &amp; ML Enthusiast
        </p>

        <!-- ===== WHO AM I (Hamna style) ===== -->
        <div class="whoami-grid">
            <span><span class="label">name:</span> <strong>Maria Aqdas</strong></span>
            <span><span class="label">role:</span> <strong>BS Data Science Student</strong></span>
            <span><span class="label">focus:</span> <strong>Machine Learning &amp; Data Science</strong></span>
            <span><span class="label">passion:</span> <strong>Data-driven solutions that matter</strong></span>
            <span><span class="label">philosophy:</span> <strong>Kaizen – 1% better, every single day</strong></span>
            <span><span class="label">location:</span> <strong>Pakistan PK</strong></span>
            <span><span class="label">status:</span> <strong>Always learning, always building</strong></span>
        </div>

        <!-- ===== ABOUT ===== -->
        <h2><i class="fas fa-user-astronaut" style="color:#b58b5f;"></i> About Me</h2>
        <ul style="list-style:none; display:flex; flex-wrap:wrap; gap:0.2rem 1.8rem; background:#f4ede6; padding:0.8rem 1.6rem; border-radius:16px; border:1px solid #e2d2be;">
            <li style="padding:0.2rem 0;">📊 BS Data Science student</li>
            <li style="padding:0.2rem 0;">🧠 Exploring Machine Learning &amp; AI</li>
            <li style="padding:0.2rem 0;">📈 Interested in data-driven solutions</li>
            <li style="padding:0.2rem 0;">⚙️ Sharpening Data Structures &amp; Algorithms</li>
            <li style="padding:0.2rem 0;">🔬 Learning deep learning fundamentals</li>
            <li style="padding:0.2rem 0;">🌍 Passionate about real-world AI applications</li>
            <li style="padding:0.2rem 0;">🎯 Goal: Become an ML/AI Engineer</li>
            <li style="padding:0.2rem 0;">😂 Fun fact: I debug with print statements and no regrets</li>
        </ul>

        <!-- ===== TECH STACK ===== -->
        <h2><i class="fas fa-microchip" style="color:#b58b5f;"></i> Tech Stack &amp; Tools</h2>
        <div class="tech-grid">
            <div class="tech-category">
                <h4><i class="fas fa-code"></i> Languages &amp; Web</h4>
                <span class="tech-tag"><i class="fab fa-python"></i> Python</span>
                <span class="tech-tag"><i class="fas fa-code"></i> C++</span>
                <span class="tech-tag"><i class="fab fa-html5"></i> HTML5</span>
                <span class="tech-tag"><i class="fab fa-css3-alt"></i> CSS3</span>
                <span class="tech-tag"><i class="fab fa-js"></i> JavaScript</span>
                <span class="tech-tag"><i class="fas fa-database"></i> SQL</span>
            </div>
            <div class="tech-category">
                <h4><i class="fas fa-brain"></i> Machine Learning &amp; Data</h4>
                <span class="tech-tag"><i class="fas fa-brain"></i> Scikit-learn</span>
                <span class="tech-tag"><i class="fas fa-chart-line"></i> Pandas</span>
                <span class="tech-tag"><i class="fas fa-calculator"></i> NumPy</span>
                <span class="tech-tag"><i class="fas fa-chart-bar"></i> Matplotlib</span>
                <span class="tech-tag"><i class="fas fa-book"></i> Jupyter</span>
                <span class="tech-tag"><i class="fas fa-cube"></i> Anaconda</span>
            </div>
            <div class="tech-category">
                <h4><i class="fas fa-tools"></i> Tools &amp; Environment</h4>
                <span class="tech-tag"><i class="fab fa-github"></i> GitHub</span>
                <span class="tech-tag"><i class="fas fa-code"></i> VS Code</span>
                <span class="tech-tag"><i class="fab fa-linux"></i> Linux</span>
                <span class="tech-tag"><i class="fas fa-code-branch"></i> Git</span>
                <span class="tech-tag"><i class="fas fa-terminal"></i> Cursor AI</span>
            </div>
        </div>

        <!-- ===== STATS ===== -->
        <h2><i class="fas fa-chart-simple" style="color:#b58b5f;"></i> GitHub Stats</h2>
        <div class="stats-row">
            <div class="stat-card"><div class="stat-number">39</div><div class="stat-label">Public Repos</div></div>
            <div class="stat-card"><div class="stat-number">1.5k</div><div class="stat-label">Total Commits</div></div>
            <div class="stat-card"><div class="stat-number">0</div><div class="stat-label">Total PRs</div></div>
            <div class="stat-card"><div class="stat-number">30</div><div class="stat-label">Contributed to</div></div>
            <div class="stat-card"><div class="stat-number">709</div><div class="stat-label">⭐ Total Stars</div></div>
        </div>

        <!-- ===== CONTRIBUTION GRAPH (simulated) ===== -->
        <div class="graph-placeholder">
            <div style="font-weight:600; color:#6b4e30;"><i class="fas fa-calendar-alt"></i> Contributions in the last year</div>
            <div class="graph-bars">
                <div class="bar dark" style="height:40px;"></div>
                <div class="bar gold" style="height:70px;"></div>
                <div class="bar" style="height:30px;"></div>
                <div class="bar dark" style="height:90px;"></div>
                <div class="bar gold" style="height:60px;"></div>
                <div class="bar" style="height:45px;"></div>
                <div class="bar dark" style="height:80px;"></div>
                <div class="bar gold" style="height:55px;"></div>
                <div class="bar" style="height:35px;"></div>
                <div class="bar dark" style="height:100px;"></div>
                <div class="bar gold" style="height:65px;"></div>
                <div class="bar" style="height:25px;"></div>
            </div>
            <div class="graph-legend">
                <span>📅 Aug 2025 – Aug 2026</span>
                <span><span style="background:#b58b5f; display:inline-block; width:12px; height:12px; border-radius:4px;"></span> 1.51k contributions</span>
            </div>
        </div>

        <!-- ===== TOP LANGUAGES (text) ===== -->
        <div style="display:flex; flex-wrap:wrap; gap:0.5rem 2rem; background:#f4ede6; border-radius:16px; padding:0.6rem 1.4rem; border:1px solid #e2d2be; margin:0.4rem 0 1.2rem 0;">
            <span><strong style="color:#7a5a3a;">Top Languages:</strong> Python, Jupyter Notebook, HTML, C++, CSS, JavaScript</span>
            <span><strong style="color:#7a5a3a;">By Repo:</strong> Python · Jupyter · HTML · C++</span>
        </div>

        <!-- ===== CURRENTLY WORKING ON ===== -->
        <h2><i class="fas fa-bolt" style="color:#b58b5f;"></i> Currently Working On</h2>
        <table class="work-table">
            <tr><td>ML algorithm theory &amp; implementation</td><td>Build deep understanding, not just syntax</td></tr>
            <tr><td>Python-based ML mini-projects</td><td>Learn by building real things</td></tr>
            <tr><td>Data analysis with Pandas &amp; NumPy</td><td>Foundation for every ML project</td></tr>
            <tr><td>DSA practice &amp; problem-solving</td><td>Write efficient, clean code</td></tr>
            <tr><td>Open-source contributions</td><td>Give back, learn from experts</td></tr>
        </table>

        <!-- ===== QUOTE ===== -->
        <div class="quote-box">
            <i class="fas fa-quote-left"></i> “So much complexity in software comes from trying to make one thing do two things.”
            <div class="quote-author">— Ryan Singer</div>
            <div style="margin-top:8px; font-style:normal; color:#8f7357; font-size:0.9rem;">
                <i class="fas fa-water" style="color:#b58b5f;"></i> “Still your waters.” — Josh Waitzkin
            </div>
        </div>

        <!-- ===== CERTIFICATIONS ===== -->
        <h2><i class="fas fa-certificate" style="color:#b58b5f;"></i> Top Certifications</h2>
        <ul style="background:#f4ede6; border-radius:16px; padding:0.8rem 1.6rem; border:1px solid #e2d2be; list-style:none;">
            <li style="padding:0.2rem 0;">🧠 <strong>Neural Networks and Deep Learning</strong> – DeepLearning.AI</li>
            <li style="padding:0.2rem 0;">🌐 <strong>The Data Science Profession</strong> – University of London</li>
            <li style="padding:0.2rem 0;">📊 <strong>Foundations: Data, Data, Everywhere</strong> – Google Digital Academy</li>
            <li style="padding:0.2rem 0;">🐍 <strong>Programming for Everybody (Python)</strong> – University of Michigan</li>
        </ul>

        <!-- ===== CONNECT ===== -->
        <div class="connect-links">
            <a href="#"><i class="fab fa-github"></i> @maria-aqdas</a>
            <a href="#"><i class="fab fa-linkedin-in"></i> Connect</a>
            <a href="#"><i class="fab fa-kaggle"></i> Follow</a>
            <a href="#"><i class="fas fa-folder-open"></i> Portfolio</a>
        </div>

        <div style="margin-top:0.8rem; color:#8f7357; font-weight:500; font-size:0.95rem;">
            <i class="fas fa-handshake" style="color:#b58b5f;"></i> Open to collaborations, ML projects, and internship opportunities!
        </div>

        <!-- ===== FOOTER ===== -->
        <div class="footer-note">
            <i class="fas fa-rocket" style="color:#b58b5f;"></i> Keep Building. Keep Growing.
            <br />
            <span style="font-size:0.75rem; color:#a58363;">⭐ If you like my journey, feel free to star my repositories!</span>
        </div>

        <!-- wave -->
        <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=80&section=footer" width="100%" style="margin-top:1.2rem; border-radius:12px; opacity:0.7;" alt="wave" />

    </div>
    <!-- /container -->

</body>
</html>

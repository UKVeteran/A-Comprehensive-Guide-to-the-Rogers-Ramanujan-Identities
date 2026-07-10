<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Comprehensive Guide to the Rogers-Ramanujan Identities</title>
    <!-- MathJax for rendering LaTeX equations beautifully -->
    <script>
        window.MathJax = {
            tex: {
                inlineMath: [['\\(', '\\)']],
                displayMath: [['\\[', '\\]']]
            }
        };
    </script>
    <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
    
    <style>
        :root {
            --bg-color: #ffffff;
            --text-color: #24292f;
            --border-color: #d0d7de;
            --code-bg: #f6f8fa;
            --accent-color: #0969da;
            --quote-bg: #f8f9fa;
            --quote-border: #cbd5e1;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--bg-color);
            max-width: 850px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }

        .header {
            text-align: center;
            margin-bottom: 2rem;
        }

        h1 {
            font-size: 2rem;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 0.3rem;
            margin-top: 24px;
            margin-bottom: 16px;
            font-weight: 600;
        }

        h2 {
            font-size: 1.5rem;
            border-bottom: 1px solid var(--border-color);
            padding-bottom: 0.3rem;
            margin-top: 24px;
            margin-bottom: 16px;
            font-weight: 600;
        }

        h3 {
            font-size: 1.25rem;
            margin-top: 24px;
            margin-bottom: 16px;
            font-weight: 600;
        }

        .badges {
            margin-bottom: 1rem;
        }

        .badges img {
            margin: 0 4px;
            vertical-align: middle;
        }

        p {
            margin-top: 0;
            margin-bottom: 16px;
        }

        hr {
            height: 0.25em;
            padding: 0;
            margin: 24px 0;
            background-color: var(--border-color);
            border: 0;
        }

        code {
            padding: 0.2em 0.4em;
            margin: 0;
            font-size: 85%;
            background-color: var(--code-bg);
            border-radius: 6px;
            font-family: ui-monospace, SFMono-Regular, SF Mono, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
        }

        pre {
            padding: 16px;
            overflow: auto;
            font-size: 85%;
            line-height: 1.45;
            background-color: var(--code-bg);
            border-radius: 6px;
            margin-bottom: 16px;
        }

        pre code {
            padding: 0;
            background-color: transparent;
            font-size: 100%;
            word-break: normal;
            white-space: pre;
        }

        table {
            display: table;
            width: 100%;
            width: max-content;
            max-width: 100%;
            overflow: auto;
            border-spacing: 0;
            border-collapse: collapse;
            margin-top: 0;
            margin-bottom: 16px;
        }

        table th, table td {
            padding: 6px 13px;
            border: 1px solid var(--border-color);
        }

        table tr {
            background-color: var(--bg-color);
            border-top: 1px solid var(--border-color);
        }

        table tr:nth-child(2n) {
            background-color: var(--code-bg);
        }

        blockquote {
            padding: 0 1em;
            color: #57606a;
            border-left: .25em solid var(--quote-border);
            background-color: var(--quote-bg);
            margin: 0 0 16px 0;
        }

        ol, ul {
            padding-left: 2em;
            margin-top: 0;
            margin-bottom: 16px;
        }

        li {
            margin-top: 0.25em;
        }

        a {
            color: var(--accent-color);
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        .footer {
            text-align: center;
            margin-top: 3rem;
            font-style: italic;
            color: #57606a;
        }
    </style>
</head>
<body>

<div class="header">
    <h1>🧮 A Comprehensive Guide to the Rogers-Ramanujan Identities</h1>
    
    <div class="badges">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT">
        <img src="https://img.shields.io/badge/python-3.10+-blue.svg" alt="Python 3.10+">
        <img src="https://img.shields.io/badge/Math-Combinatorics-orange.svg" alt="Math: Combinatorics">
    </div>

    <p><em>A computational and theoretical repository dedicated to exploring, verifying, and visualizing the famous Rogers-Ramanujan identities.</em></p>
</div>

<hr>

<h2>📖 Overview</h2>
<p>This repository serves as a comprehensive guide and computational toolkit for the <strong>Rogers-Ramanujan Identities</strong>—two of the most remarkable and deep results in the theory of integer partitions and basic hypergeometric series.</p>
<p>Discovered first by L. J. Rogers in 1894, famously rediscovered by Srinivasa Ramanujan in 1913, and independently proved by Issai Schur in 1917, these identities bridge analytical number theory, combinatorics, and even statistical mechanics.</p>

<hr>

<h2>🔢 The Identities</h2>
<p>The identities are typically expressed in terms of \(q\)-series, where \(|q| < 1\). We use the standard \(q\)-Pochhammer symbol notation:</p>
<p>\[(a; q)_n = \prod_{k=0}^{n-1} (1 - aq^k)\]</p>

<h3>The First Rogers-Ramanujan Identity</h3>
<p>\[ \sum_{n=0}^{\infty} \frac{q^{n^2}}{(q; q)_n} = \prod_{j=0}^{\infty} \frac{1}{(1-q^{5j+1})(1-q^{5j+4})} \]</p>

<h3>The Second Rogers-Ramanujan Identity</h3>
<p>\[ \sum_{n=0}^{\infty} \frac{q^{n^2+n}}{(q; q)_n} = \prod_{j=0}^{\infty} \frac{1}{(1-q^{5j+2})(1-q^{5j+3})} \]</p>

<hr>

<h2>🧩 Combinatorial Interpretation</h2>
<p>Beyond their analytical beauty, these identities have profound combinatorial meanings (first noted by Percy MacMahon and Issai Schur), relating to integer partitions.</p>

<table>
    <thead>
        <tr>
            <th>Identity</th>
            <th>Analytical Side (Series)</th>
            <th>Infinite Product Side</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><strong>First</strong></td>
            <td>Number of partitions of \(n\) such that the difference between any two consecutive parts is at least 2.</td>
            <td>Number of partitions of \(n\) into parts congruent to \(1\) or \(4 \pmod 5\).</td>
        </tr>
        <tr>
            <td><strong>Second</strong></td>
            <td>Number of partitions of \(n\) such that the difference between any two consecutive parts is at least 2, and the part 1 is not allowed.</td>
            <td>Number of partitions of \(n\) into parts congruent to \(2\) or \(3 \pmod 5\).</td>
        </tr>
    </tbody>
</table>

<hr>

<h2>📂 Repository Structure</h2>
<pre><code>rogers-ramanujan/
│
├── docs/                   # Mathematical proofs and historical essays
│   ├── history.md
│   └── algebraic_proofs.pdf
│
├── src/                    # Source code for computational verification
│   ├── series_expansion.py # Taylor expansion of the infinite products
│   ├── combinatorics.py    # Integer partition generators
│   └── tests.py            # Unit tests verifying up to q^1000
│
├── requirements.txt        # Python dependencies
└── README.md               # This file</code></pre>

<hr>

<h2>🚀 Installation & Usage</h2>
<p>To run the computational verifications locally, you will need Python 3.10+.</p>

<p><strong>1. Clone the repository:</strong></p>
<pre><code class="language-bash">git clone https://github.com/yourusername/rogers-ramanujan.git
cd rogers-ramanujan</code></pre>

<p><strong>2. Install dependencies:</strong></p>
<pre><code class="language-bash">pip install -r requirements.txt</code></pre>

<p><strong>3. Run the basic verification script:</strong></p>
<pre><code class="language-bash">python src/series_expansion.py --terms 50</code></pre>

<h3>Example Output</h3>
<p>The script <code>series_expansion.py</code> expands both sides of the identities to visually confirm they match up to \(O(q^N)\).</p>

<pre><code class="language-python"># Output for the First Identity up to 10 terms
Series Side:  1 + q + q^2 + q^3 + 2q^4 + 2q^5 + 3q^6 + 3q^7 + 4q^8 + 5q^9 + 6q^10
Product Side: 1 + q + q^2 + q^3 + 2q^4 + 2q^5 + 3q^6 + 3q^7 + 4q^8 + 5q^9 + 6q^10
Match: TRUE</code></pre>

<hr>

<h2>🤝 Contributing</h2>
<p>Contributions are welcome! Whether you are adding a new proof technique (like the Gordon generalizations), improving the partition algorithms, or translating the algebraic logic into a new programming language, please feel free to open a Pull Request.</p>

<ol>
    <li>Fork the Project</li>
    <li>Create your Feature Branch (<code>git checkout -b feature/AmazingFeature</code>)</li>
    <li>Commit your Changes (<code>git commit -m 'Add some AmazingFeature'</code>)</li>
    <li>Push to the Branch (<code>git push origin feature/AmazingFeature</code>)</li>
    <li>Open a Pull Request</li>
</ol>

<hr>

<h2>📜 License</h2>
<p>Distributed under the MIT License. See <code>LICENSE</code> for more information.</p>

<div class="footer">
    <blockquote>"An equation for me has no meaning, unless it expresses a thought of God." — Srinivasa Ramanujan</blockquote>
</div>

</body>
</html>

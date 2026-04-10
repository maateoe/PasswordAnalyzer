<h1> Password Wizards: Password Analyzer </h1>
<h2> ShellHacks 2024 </h2>
<p>
This project provides a <b>defensive security interface</b> designed to quantify password entropy and predict resistance against modern brute-force attacks. By leveraging the <b>zxcvbn</b> algorithm, this tool moves beyond archaic character-requirement checklists to evaluate passwords based on pattern recognition and dictionary-match frequency.
</p>

<h2>Utilities Used</h2>
<ul>
<li><b>Streamlit:</b> High-performance framework for the security dashboard UI.</li>
<li><b>zxcvbn Library:</b> A realistic password strength estimator inspired by Dropbox's password crackers.</li>
<li><b>Python 3.x:</b> Backend logic and cryptographic data processing.</li>
<li><b>Custom CSS/HTML:</b> For enhanced visual feedback on vulnerability metrics.</li>
</ul>

<h2>Analysis Framework & Strength Metrics</h2>
<p>
Password Wizards evaluates input based on <b>spatial patterns</b> (keyboard walks), <b>sequence analysis</b> (123456), and <b>frequency lists</b> (names, dates, and common passwords). The scoring system provides a predictive "Time-to-Crack" based on a standard online throttling scenario.
</p>

<table border="1">
<tr>
<th>Security Score</th>
<th>Strength Rating</th>
<th>Resilience Profile</th>
</tr>
<tr>
<td>0 - 1</td>
<td><b>Very Weak</b></td>
<td>Vulnerable to instant dictionary attacks.</td>
</tr>
<tr>
<td>2</td>
<td><b>Moderate</b></td>
<td>Resistant to basic automated brute-force.</td>
</tr>
<tr>
<td>3</td>
<td><b>Strong</b></td>
<td>High entropy; requires significant compute time.</td>
</tr>
<tr>
<td>4</td>
<td><b>Very Strong</b></td>
<td><b>Hardened (Cryptographically Robust)</b></td>
</tr>
</table>

<br />

<h2>Tool Functionality</h2>

<h3>Step 1: Real-Time Entropy Evaluation</h3>
<p>
The core engine analyzes the password string as the user inputs it. It identifies "Low Entropy" segments—such as common words or dates—that would be the first targets in a <b>Rule-Based Mutation</b> attack (like those performed with John the Ripper).
</p>

<br />

<h3>Step 2: Crack-Time Prediction</h3>
<p>
The tool calculates a <b>"Crack Time"</b> metric based on an "Online No-Throttling" attack vector. This provides users with a tangible understanding of their risk profile in the event of a credential stuffing attempt.
</p>

<br />

<h3>Step 3: Dynamic Remediation Advice</h3>
<p>
Based on the specific weaknesses found (e.g., repeating characters, common sequences), the wizard generates <b>real-time suggestions</b> to harden the credential before it is ever committed to a database.
</p>

<br />

<h2>🛡️ Security Best Practices & Mitigation</h2>
<p>
To defend against the multi-vector attacks identified in our hash analysis research, we recommend the following credential policies:
</p>
<ol>
<li><b>Entropy Over Complexity:</b> Focus on <b>Passphrases</b> (long strings of random words) rather than short, complex passwords. Length is the primary defender against brute-force.</li>
<li><b>Avoid Predictable Substitutions:</b> Standard "l33tspeak" (e.g., @ for a) is easily defeated by modern cracking rulesets. Use unique, non-standard substitutions if necessary.</li>
<li><b>Implement MFA:</b> Even a "Very Strong" password can be stolen via phishing. Multi-Factor Authentication acts as the final line of defense when a password is compromised.</li>
</ol>

<hr />

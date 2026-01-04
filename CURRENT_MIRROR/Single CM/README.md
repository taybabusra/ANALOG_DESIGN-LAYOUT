<h1>CMOS Current Mirror Architectures – Design & Analysis</h1>

<p>
This repository presents a <b>progressive design study of CMOS current mirrors</b>,
starting from a basic mirror and evolving toward
<b>high-output-resistance, low-voltage, high-swing architectures</b>.
Each configuration is evaluated through schematic design and simulation results,
with emphasis on operating region, output resistance, and compliance voltage.
</p>

<hr>

<h2>Configuration 1: Simple MOS Current Mirror</h2>

<h3>Schematic</h3>
<img src="https://github.com/user-attachments/assets/5c4661a2-e47c-4803-8a00-c3fb42250d31" width="700">

<h3>Description</h3>
<p>
Two identical NMOS transistors are used.
The reference transistor is diode-connected, fixing V<sub>GS</sub>,
which is shared with the output transistor to mirror the current.
</p>

<h3>Simulation Result</h3>
<img src="https://github.com/user-attachments/assets/363d0d04-508a-4804-b860-295ca235a01a" width="900">

<h3>Key Observations</h3>
<ul>
  <li>Output resistance: <b>R<sub>out</sub> ≈ 1.346 MΩ</b></li>
  <li>Minimum required V<sub>DD</sub> ≈ V<sub>TH</sub> + V<sub>OV</sub> ≈ 450 mV</li>
  <li>Drain of the output transistor is directly connected to V<sub>DD</sub></li>
  <li>Very limited saturation operating region</li>
</ul>

<p>
<b>Conclusion:</b> Although compact and simple, this mirror is highly sensitive to
V<sub>DD</sub> variation and exhibits poor current regulation.
</p>

<hr>

<h2>Configuration 2: Modified Simple Current Mirror</h2>

<h3>Schematic</h3>
<img src="https://github.com/user-attachments/assets/2eebfced-b749-4d83-bb37-51544a2fba3f" width="700">

<h3>Description</h3>
<p>
This configuration introduces structural changes intended to reduce the
direct dependence of output current on supply voltage by improving
drain voltage control of the mirroring device.
</p>

<h3>Simulation Result</h3>
<img src="https://github.com/user-attachments/assets/d8dc6f72-d2eb-4872-b4cf-f1547ff80491" width="700">

<h3>Observations</h3>
<ul>
  <li>Improved saturation margin compared to Configuration 1</li>
  <li>Reduced current variation with V<sub>DD</sub></li>
  <li>Output resistance still limited by channel-length modulation</li>
</ul>

<hr>

<h2>Configuration 2 (Updated)</h2>

<h3>Schematic</h3>
<img src="https://github.com/user-attachments/assets/e6527504-b791-4fec-a464-8d46909d1c23" width="700">

<h3>Simulation Result</h3>
<img src="https://github.com/user-attachments/assets/8779f253-34d0-4605-b9fb-e45e88313acf" width="500">

<h3>Analysis</h3>
<p>
The updated configuration further improves operating-region robustness,
but the achievable output resistance remains constrained by finite
channel-length modulation.
</p>

<hr>

<h2>Configuration 3: Improved Wilson Current Mirror</h2>

<h3>Schematic</h3>
<img src="https://github.com/user-attachments/assets/4088a99c-b840-4645-a0cd-e31d603fbca5" width="700">

<h3>Description</h3>
<p>
The Improved Wilson Current Mirror employs internal feedback to suppress
the effect of channel-length modulation, significantly increasing output resistance
and current accuracy.
</p>

<h3>Expected Characteristics</h3>
<ul>
  <li>Very high output resistance</li>
  <li>Excellent current matching</li>
  <li>Reduced sensitivity to V<sub>DS</sub> variations</li>
</ul>

<p>
<b>Trade-off:</b> Increased voltage headroom and reduced output swing
compared to simpler mirrors.
</p>

<hr>

<h2>Configuration 4: High-Swing Current Mirror</h2>

<h3>Description</h3>
<p>
The High-Swing Current Mirror is designed to achieve
<b>cascode-level output resistance</b> while minimizing voltage headroom.
All transistors are biased such that saturation is maintained over
a wide output voltage range.
</p>

<h3>Design Insight</h3>
<p>
This topology provides the best balance between
<b>output resistance, voltage compliance, and robustness</b>,
making it suitable for low-voltage analog and RF IC biasing.
</p>

<hr>

<h2>Architecture Comparison</h2>

<table border="1" cellpadding="6">
  <tr>
    <th>Topology</th>
    <th>Output Resistance</th>
    <th>Voltage Headroom</th>
    <th>Complexity</th>
  </tr>
  <tr>
    <td>Simple Mirror</td>
    <td>Low</td>
    <td>Low</td>
    <td>Very Low</td>
  </tr>
  <tr>
    <td>Modified Simple</td>
    <td>Medium</td>
    <td>Medium</td>
    <td>Low</td>
  </tr>
  <tr>
    <td>Wilson Mirror</td>
    <td>High</td>
    <td>High</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>High-Swing Mirror</td>
    <td>High</td>
    <td>Low</td>
    <td>Medium</td>
  </tr>
</table>

<hr>

<h2>Key Takeaway</h2>
<p>
Current mirror design is fundamentally a trade-off between
<b>output resistance, voltage headroom, and circuit complexity</b>.
High-swing architectures offer the most practical solution
for modern low-voltage CMOS analog systems.
</p>

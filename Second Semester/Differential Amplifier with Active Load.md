Consider M3 and M4, which are diode connected as the active loads, Differential Mode Analysis

The differential mode ac voltage gain is:

and since 

$A_{vdd} = \frac{v_{o1} - v_{o2}}{v_{i1} - v_{i2}} \equiv \frac{v_{o1} - v_{o2}}{v_{id}}$

recalling previous result:

$A_{vdd} = -g_{m1}(r_{ds1} \\parallel r_{ds3} \\parallel \frac{1}{g_{m3}})$

and since $\frac{1}{g_m} \ll r_{ds}$

then $A_{vdd} = -\frac{g_{m1}}{g_{m3}}$

$A_{vdd} = -\frac{\sqrt{2K'_n(W/L)_1 (I_B/2)}}{\sqrt{2K'_p(W/L)_3(I_B/2)}}$

$A_{vdd} = -\sqrt{\frac{k'_n}{k'_p} \frac{(W/L)_1}{(W/L)_3}}$

AC output resistance for differential output:

$r_{out} = r_{out1} + r_{out2}$, where $r_{out1} = r_{ds1} \\parallel r_{ds2} \\parallel \frac{1}{g_{m3}}$

approx $\frac{1}{g_{m3}}$

therefore $r_{out} = \frac{1}{g_{m3}} + \frac{1}{g_{m4}}$

$r_{out} = \frac{2}{g_{m3}}$

M3 and M4 are matched

Current Sources as active loads:

M3 and M4 are now transistors in pinchoff acting as current-source active loads, again, M3 and M4 are matched.
Differential mode operation, i.e. differential input differential output.
![[Pasted image 20251017112020.png]]

$A_{vdd} = -g_{m1}(r_{ds1} \\parallel r_{ds3})$

$= -\frac{g_{m1}}{g_{ds1} + g_{ds3}}$

In terms of design parameters:

$A_{vdd} = -\frac{\sqrt{2k'_n(W/L)(I_B/2)}}{\lambda_n(I_B/2) + \lambda_p(I_B/2)}$

$= -\frac{\sqrt{2K'_n(W/L)_1/(I_B/2)}}{\lambda_n + \lambda_p}$

Therefore:

$A_v \propto \sqrt{W/L_1}$

and

$A_v \propto \frac{1}{\sqrt{I_B}}$

In order to increase $A_{vdd}$, $W/L_1$ can be increased (resulting in larger silicon area) and/or the DC biasing current $I_B$ decreased.

Note that decreasing $I_B$ also decreases the DC power dissipation needed for the differential amplifier to operate:

$P_{dc} = V_{dc} \cdot I_{dc}$

$P_{dc} = V_{dc} \cdot I_B$

AC output resistance for differential output:

$r_{out} = r_{out1} + r_{out2}$

where $r_{out1} = r_{out2} = r_{ds1} \\parallel r_{ds2}$

Common mode voltage gain $A_{cs} = -g_{m1}$

$A_{cs} = \frac{V_{O1}}{V_{CM}}$

$= -\frac{g_{m1}R}{1 + 2g_{m1}r_{ds7}}$

$A_{cs}$ is now given by:

$A_{cs} \approx -\frac{r_{ds3}}{2r_{ds7}}$

$\text{CMRR} = \left| \frac{A_{vds}}{A_{cs}} \right|$

Where $A_{vds}$ is the differential input, single-ended output voltage gain, and thus $A_{vds} = \frac{1}{2}A_{vdd}$

Therefore $A_{vds} = -\frac{1}{2}\left(\frac{g_{m1}}{g_{ds1} + g_{ds2}}\right)$

$\text{CMRR} = \frac{1}{2} \frac{g_{m1}}{g_{ds1} + g_{ds3}} \cdot \frac{2r_{ds7}}{r_{ds3}}$

$\text{CMRR} \approx \frac{g_{m1}g_{ds3}r_{ds7}}{g_{ds1} + g_{ds3}}$


 Differential Amplifier with current Mirror Load
 ![[Pasted image 20251017114302.png]]
 M3,M4 form a  current mirror acting as the active load of M1,M2. Note that the output is now single-ended.


AC Voltage gain:

$A_{vd} = \frac{v_o}{v_{i1} - v_{i2}} = \frac{v_o}{v_{id}}$

Draw the AC equivalent circuit:
![[Pasted image 20251017115927.png]]

M1 matched with M2, M3 matched with M4
also $V_{gs4} = V_{gs3}$

$v_o = -[g_{m2}V_{gs2} + g_{m4}V_{gs4}](r_{ds2} \\parallel r_{ds4})$

Remember: for a differential input $V_{id}$, $v_{gs1} = \frac{v_{id}}{2}$, $v_{gs2} = -\frac{v_{id}}{2}$

Also: $V_{gs4} = -g_{m1}v_{gs1}(r_{ds1} \\parallel r_{ds3} \\parallel \frac{1}{g_{m3}}) \approx -\frac{g_{m1}v_{gs1}}{g_{m3}}$

Therefore:

$v_o = -[g_{m2}(-\frac{v_{id}}{2}) + g_{m4}(-\frac{g_{m1}}{g_{m3}} \cdot \frac{v_{id}}{2})](r_{ds2} \\parallel r_{ds4})$

$= \frac{g_{m2}v_{id}}{g_{ds2} + g_{ds4}}$

$A_{vd} = \frac{g_{m2}}{g_{ds2} + g_{ds4}}$

In terms of design parameters:

$A_{vd} = \frac{\sqrt{2k'_n(W/L)_2(I_B/2)}}{(\lambda_n + \lambda_p)(I_B/2)}$



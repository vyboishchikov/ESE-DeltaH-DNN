<html>

<font face="Open Sans">

<h1>ESE-&Delta;H-DNN &ndash; A dense Neural Network for evaluation of solvation free 
energy and enthalpy based on Generalized-Born terms</h1>

<h2>Introduction and User's Guide</h2>

<p><i>ESE-&Delta;H-DNN</i> is a method for evaluation of <b>solvation free energy</b> and 
<b>enthalpy</b> of neutral molecules in organic solvents [2]. It  requires the solute molecular
geometry only. To obtain the solvation free energy, first <i>electronegativity-equalization</i>
atomic charges are calculated. Subsequently, the Born-type terms, atomic surfaces and volumes
are evaluated and, along with five solvent features, are fed into a <i>Dense Neural Network</i>.</p>

<p>The present scheme is an adaptation of my previous ESE-GB-DNN method. In contrast to 
the previous ESE-GB-DNN scheme [3], the <b>ESE-&Delta;H-DNN</b> method yields 
&Delta;<i>G</i><sub>solv</sub> and &Delta;<i>H</i><sub>solv</sub>. However, ESE-&Delta;H-DNN was trained 
on a database of neutral solutes in organic solvents. Therefore, if you need aqueous 
solutions or ions, please use <a href="https://github.com/vyboishchikov/ESE-GB-DNN">ESE-
GB-DNN</a> 

<p>The present <b>ESE-&Delta;H-DNN</b> scheme is a continuation of my previous works 
[3&ndash;5] and is loosely based on the <a href="https://github.com/vyboishchikov/ESE">uESE</a> 
[7] and xESE [8] that we developed jointly with Alexander Voityuk.</p>

<p>The supported elements are H, C, N, O, F, Si, P, S, Cl, Br, I.</p>

<p style='margin-top:12pt;margin-bottom:0cm'> &Delta;<i>G</i><sub>solv</sub> and &Delta;<i>H</i><sub>solv</sub>
can be calculated by the program ESE-DeltaH-DNN, which can be downloaded here free of charge:</p>

<p style='margin:0cm;margin-bottom:0pt'>
<a href="https://github.com/vyboishchikov/ESE-DeltaH-DNN/blob/main/ESE-DeltaH-DNN.exe">ESE-DeltaH-DNN.exe</a> &ndash; Windows version</p>
<a href="https://github.com/vyboishchikov/ESE-DeltaH-DNN/blob/main/ESE-DeltaH-DNN.x">ESE-DeltaH-DNN.x</a> &ndash; Linux version.</p>

<p style='margin:0cm;margin-top:12pt'>
The ESE-&Delta;H-DNN program can be run from the command line as follows:</p>

<p style='margin-top:6pt;margin-bottom:0cm'>
<code><b>ESE-DeltaH-DNN.exe <i>xyz-file</i> -solvent <i>solvent</i></b></code></p>

<p><i><b>Warning:</b></i> The xyz-file should contain atomic symbols (or numbers) and 
Cartesian coordinates (in &#8491;) and an empty line at the end. It should not contain
any header.

<p style='margin-top:12pt;margin-bottom:0pt'>
If your solvent is not in this <a href="https://github.com/vyboishchikov/ESE-DeltaH-DNN/blob/main/solvent-list.md">list</a>, you can use the following call format:</p>

<p style='margin-top:6pt;margin-bottom:12pt'><code><b>ESE-DeltaH-DNN.exe <i>xyz-file</i> -Eps <i>dielectric_constant</i> -BP <i>boiling_point_&deg;C</i> -Nheavy <i> number_of_non_hydrogen_atoms_in_solvent</i> -MolVolume <i>molar-volume</i> -H-bond <i>number_of_hydrogen_bon_centers></i></b> </code></p>

<p style='margin:0cm'>
Once you use results calculated by the ESE-&Delta;H-DNN program, you should include at least the following citations:</p>

<p style='margin:0cm'>
<b>1</b>. S. F. Vyboishchikov, <i>ESE-&Delta;H-DNN program</i>, Girona, <b>2024</b></p>
<p style='margin:0cm'>
<b>2</b>. S. F. Vyboishchikov, <i>Liquids</i>, <b>2024</b>, <i>submitted</i>.

<p style='margin:0cm;margin-bottom:12pt'>
<b>3</b>. S. F. Vyboishchikov, <i>J. Chem. Theory Comput</i>., <b>2023</b>, <i>19</i>, 8340&ndash;8350.
<a href="https://doi.org/10.1021/acs.jctc.3c00858">DOI: 10.1021/acs.jctc.3c00858</a></p>
<p style='margin-bottom:0pt'>

and preferably also cite some our previous related work:</p>

<p style='margin:0cm;margin-bottom:0pt'>
<b>4</b>. S. F. Vyboishchikov, <i>J. Chem. Inf. Model</i>., <b>2023</b>, <i>63</i>, 6283&ndash;6292.
<a href="https://doi.org/10.1021/acs.jcim.3c00922">DOI: 10.1021/acs.jcim.3c00922</a></p>

<p style='margin:0cm;margin-bottom:0pt'>
<b>5</b>. S. F. Vyboishchikov, <i>J. Comput. Chem.</i>, <b>2023</b>, <i>44</i>, 307&ndash;318. 
<a href="https://doi.org/10.1002/jcc.26894">DOI: 10.1002/jcc.26894</a></p>

<p style='margin:0cm;margin-bottom:0pt'>
<b>6</b>. S. F. Vyboishchikov, A. A. Voityuk, <i> Chemical Reactivity, vol. 2:
Approaches and applications, S. Kaya, L. von Szentp&aacute;ly, G. Serdaro&gbreve;lu, K. Guo (Eds.)</i>,
Elsevier, Amsterdam, <b>2023</b>, 399&ndash;427. <a href="https://doi.org/10.1016/B978-0-32-390259-5.00021-4">
DOI: 10.1016/B978-0-32-390259-5.00021-4</a></p>

<p style='margin:0cm;margin-bottom:0pt'>
<b>7</b>. S. F. Vyboishchikov, A. A. Voityuk, <a href="https://pubs.acs.org/doi/10.1021/acs.jcim.1c00885">
<i>J. Chem. Inf. Model., </i><b>2021</b>, <i>61</i></a>, 4544&ndash;4553. DOI: 10.1021/acs.jcim.1c00885 </p>

<p style='margin:0cm;margin-bottom:0pt'>
<b>8</b>. S. F. Vyboishchikov, A. A. Voityuk, <a href="https://onlinelibrary.wiley.com/doi/abs/10.1002/jcc.26531">
<i>J. Comput. Chem., </i><b>2021</b>, <i>42</i></a>, 1184&ndash;1194. DOI: 10.1002/jcc.26531</p>

<p style='margin:0cm;margin-bottom:0pt'>
<b>9</b>. A. A. Voityuk, S. F. Vyboishchikov,
<a href="https://pubs.rsc.org/en/content/articlelanding/2020/cp/d0cp02667k">
<i>Phys. Chem. Chem. Phys.</i> <b>2020</b>, <i>22</i></a>, 14591&ndash;14598. DOI: 10.1039/d0cp02667k</p>

<p style='margin:0cm;margin-bottom:0pt'>
<b>10</b>. A. A. Voityuk, S. F. Vyboishchikov, <a href="https://pubs.rsc.org/en/content/articlelanding/2019/cp/c9cp03010g">
<i>Phys. Chem. Chem. Phys.</i>, <b>2019</b>, <i>21</i></a>, 875&ndash;874. DOI: 10.1039/c9cp03010g</p>

<p style='margin:0cm;margin-top:12pt'><span style='font-family: "Open Sans"'>
Questions related to the ESE-&Delta;H-DNN method and program should be addressed to
<a href="mailto:vyboishchikov@googlemail.com">Sergei Vyboishchikov</a>.</p>

</html>

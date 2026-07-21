# MA_LLM_Reliability_Visualization_Active_Distribution_Networks

This repository provides supplementary materials and reproducible resources for the paper:

**"Bayesian-Network-Informed Multi-Agent LLM Clustering for Reliability-Oriented Visualization of DER-Rich Active Distribution Networks"**

**Authors:**  
**Rouzbeh Haghighi**, Graduate Student Member IEEE, **Van-Hai Bui**, Senior Member IEEE, **Mengqi Wang**, Senior Member IEEE, **Wencong Su**, Senior Member IEEE

**Note:** This paper has been submitted to **Elsevier - Applied Energy**.

**Paper link:** (to be added)

## Description

This repository includes mathematical formulations, tables, and figures discussed in the paper. It aims to provide additional resources and data to support the research findings and facilitate further studies.

## Contents

### I. DER Generation Models

This study adopts standard steady-state WT and PV generation models to represent time-varying active-power injections from inverter-interfaced DERs. Environmental inputs are mapped to active-power outputs that serve as exogenous injections in the power-flow model and the subsequent VVC optimization.

$$
P_{\mathrm{WT}}(v)=
\begin{cases}
0, & v < v_{\mathrm{ci}} \text{ or } v \ge v_{\mathrm{co}}, \\
C_1 v^3 - C_2 P_{\mathrm{WT}}^{\mathrm{r}}, & v_{\mathrm{ci}} \le v \le v_{\mathrm{r}}, \\
P_{\mathrm{WT}}^{\mathrm{r}}, & v_{\mathrm{r}} \le v \le v_{\mathrm{co}}
\end{cases}
$$

$$
C_1=\frac{P_{\mathrm{WT}}^{\mathrm{r}}}{v_{\mathrm{r}}^{3}-v_{\mathrm{ci}}^{3}},
\qquad
C_2=\frac{v_{\mathrm{ci}}^{3}}{v_{\mathrm{r}}^{3}-v_{\mathrm{ci}}^{3}}
$$

where $P_{\mathrm{WT}}^{\mathrm{r}}$ is the rated WT active power (kW); $v$ is the wind speed (m/s); and $v_{\mathrm{ci}}$, $v_{\mathrm{r}}$, and $v_{\mathrm{co}}$ denote the cut-in, rated, and cut-out wind speeds, respectively.

For PV units, the cell temperature is approximated using the NOCT model, and the PV active power $P_{\mathrm{PV}}$ is computed using an irradiance- and temperature-corrected linear model:

$$
T_{\mathrm{c}} = T_{\mathrm{a}} + \frac{G_{\mathrm{irr}}(\mathrm{NOCT}-20)}{800}
$$

$$
P_{\mathrm{PV}}(G_{\mathrm{irr}},T_{\mathrm{c}})=
P_{\mathrm{PV}}^{\mathrm{r}}
\left(\frac{G_{\mathrm{irr}}}{G_{\mathrm{ref}}}\right)
\left[1+\eta_T(T_{\mathrm{c}}-T_{\mathrm{ref}})\right]
$$

where $P_{\mathrm{PV}}^{\mathrm{r}}$ is the rated PV active power (kW); $G_{\mathrm{irr}}$ is the solar irradiance (W/m²); $T_{\mathrm{a}}$ is the ambient temperature (°C); $\eta_T$ is the PV temperature coefficient (1/°C); $G_{\mathrm{ref}}$ is the reference irradiance; and $T_{\mathrm{ref}}$ is the reference cell temperature.


<img width="1000" height="250" alt="Git_Converter_Topology" src="https://github.com/user-attachments/assets/b2a3b9ac-4461-42a2-998e-503ffed38c4e" />



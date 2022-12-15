##### 1 Objective function

The agent's value function is 
$$
V_t = u_t + \delta E_t[V_{t+1}]
$$
where the utility function takes a CRRA-style form:
$$
u_t = \frac{m_t^{1-\gamma_1}}{1-\gamma_1}+\kappa\psi_t\frac{w_t^{1-\gamma_2}}{1-\gamma_2}
$$
and 
$$
m_t = [\alpha_1 c_t^{\rho} + \alpha_2h_t^{\rho} + \alpha_3g_t^\rho]^{1/\rho}
$$

$$
g_t = \left\{
\begin{split}
& \bar{g} + (a^g_t - G) & \;\text{if}\; g_{t-1}<\bar{g},a^g_t<G \\
& \bar{g} & \; \text{else} \\
\end{split}
\right.
$$




##### 2 recession risk and asset returns

the state of economy $e_t \in \{0,1\}$ 

decided by a 2×2 transmission matrix

the probabilities that the economy transmit from prosperity to recession, and from recession to prosperity are $\pi_1$ and $\pi_2$


$$
\left\{
\begin{split}
log(\tilde{R}_{j,t}) & = \beta_{j,1} + \beta_{j,2}\Delta e_t^{+} + \beta_{j,3}\Delta e_t^{-} + \beta_{j,3}v_{t-1} + \epsilon_{j,t} \\
\log(p_{t})-\log(p_{t-1}) & = \beta_{h,1} + \beta_{h,2}\Delta e_t^{+} + \beta_{h,3}\Delta e_t^{-} + \beta_{h,3}v_{t-1} + \epsilon_{v,t} \\
v_t & = \beta_{v,1} + \beta_{v,2}\Delta e_t^{+} + \beta_{v,3}\Delta e_t^{-} + \beta_{v,3}v_{t-1} + \epsilon_{v,t} \\
\end{split}\right.
$$

where $\Delta e_t^{+}=\max\{0,e_t-e_{t-1}\}$, $\Delta e_t^{-}=\max\{0,e_{t-1}-e_t\}$, $v_t$ is the log dividend yield ratio. $j \in \{\text{bond},\text{stock}\}$



##### 3 labor income

$$
\begin{split}
& \log(\tilde{Y}_t) = f(t,X_t) + \xi^p_t + \xi^q_t \\
& \xi^p_t = \xi^p_{t-1} + \eta_t \\
& \xi^q_t \sim (0,\sigma_q^2) \\
& \eta_t = \left\{
\begin{split}
& \eta_{1,t} \sim N(\mu_{\eta_1,e_t},\sigma_{\eta_1}) \; \text{with prob.} \,\pi_3 \\
& \eta_{2,t} \sim N(\mu_{\eta_2,e_t},\sigma_{\eta_2}) \; \text{with prob.} \,1-\pi_3\\
\end{split}
\right.
\end{split}
$$

where $\xi^p_t$ is permanent income shock and $\xi^q_t$ is transitory income shock

##### 5 liquid savings account

$$
a^l_t = \sum_{j=1}^J (\tilde{R}_{j,t}a^l_{j,t-1}+s^l_{j,t})
$$

##### 6 retirement savings account

$$
a^r_t = \sum_{j=1}^J (\tilde{R}_{j,t}a^r_{j,t-1}+s^r_{j,t})
$$



##### 7 goal-based savings account

savings goal (default): $G = (1-\phi_{lv})p_th_t$
$$
a^g_t = \left\{
\begin{split}
& \sum_{j=1}^J (\tilde{R}_{j,t}a^g_{j,t-1}+s^g_{j,t}) &\; \text{if} \; g_{t-1}<\bar{g}  \\
& 0 &\; \text{if} \; g_{t-1}=\bar{g} 
\end{split}
\right.
$$



##### 8 housing

house price $\tilde{p}_t$

interest rate $i_t$

rent-to-price ratio $\phi_{rp}$

loan-to-value ratio $\phi_{lv}$

duration $L$

transaction cost $\xi_h$



action variable: $o_t$, $b_t$



If the agent is a renter at period $t$, $o_t = 0$;  if she is a homeowner, $o_t = 1$. 

$o_t \in \{0,1\}$  if $D_t=0$; $o_t \in \{1\}$ if $D_t>0$ 

$b_t\{o_t = 0\} = \phi_{rp}p_th_t$


$$
L_t = \left\{
\begin{split}
& L, & \; \text{if} \; o_{t-1} = 0,o_t = 1 \\
& L_{t-1} - 1, & \; \text{if} \;o_{t-1}=o_t=1, D_t>0 \\
& 0, & \; \text{else}
\end{split}\right.
$$

$$
D_t = \left\{
\begin{split}
& p_th_t-b_t, & \; \text{if} \; o_{t-1} = 0,o_t = 1 \\
& D_{t-1} - b_t, & \; \text{if} \;o_{t-1}=o_t=1, D_{t-1}>0 \\
& 0, & \; \text{else}
\end{split}\right.
$$



$b_t\{o_{t-1} = 0,o_t = 1\} \in [(1-\phi_{lv})p_th_t+\xi_h,p_th_t+\xi_h]$


$b_t\{o_{t-1}=o_t=1,d_t>0\} \in [\frac{1}{L_t}\frac{1+i_t}{i_t}((1+i_t)^{L_t}-1) D_t,D_t]$

$b_t\{o_{t-1}=1,o_t=0\} = -p_th_t+\xi_h$





$b_t$ cannot exceed cash-on-hand





10 stock market participation 

11 medical expenditure



the probability that health status is bad $\pi_4 = f(t,X_t,Y_t)$ 


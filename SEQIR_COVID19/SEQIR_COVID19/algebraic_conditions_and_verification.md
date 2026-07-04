# Algebraic Conditions and Verification for the SEQIR COVID-19 Model

This file contains the algebraic conditions and verification for the monomial parametrization of the SEQIR COVID-19 model of Pal et al. (2022).

The weakly reversible PL-NDK realization is transformed into a weakly reversible PL-RDK realization using Procedure 1 of Talabis et al. (2024). After Procedure 1, the SEQIR realization has \(n=10\) complexes, \(l=2\) linkage classes, stoichiometric rank \(s=5\), and kinetic-order subspace dimension \(\widetilde{s}=5\), giving the deficiency \(\delta=n-l-s=10-2-5=3\) and the kinetic deficiency \(\widetilde{\delta}=n-l-\widetilde{s}=10-2-5=3\).

Since \(\widetilde{\delta}=3>0\), the monomial parametrization is valid only when the parameter values satisfy the required algebraic conditions.

## Algebraic Conditions

The required algebraic conditions are

$$
\left(\frac{\lambda}{2}\right)(\gamma_{s_2}+\gamma_{s_1})=(\mu_r)(\beta),
$$

$$
\left(\frac{\lambda}{2}\right)(\gamma_{s_1})(\mu_q)(\mu_e+\gamma_{e_1}+\gamma_{e_2})
=
\left(\frac{\lambda}{2}\right)(\gamma_{e_1})(\gamma_{q_1}+\gamma_{q_2})(\mu_s+\gamma_{s_2}+\gamma_{s_1}),
$$

$$
\left(\frac{\lambda}{2}\right)(\gamma_{s_1})(\gamma_{q_2})(\mu_i)(\mu_e+\gamma_{e_1}+\gamma_{e_2})
=
(\gamma_r)\left(\frac{\lambda}{2}\right)(\gamma_{e_2})(\gamma_{q_1}+\gamma_{q_2})(\mu_s+\gamma_{s_2}+\gamma_{s_1}).
$$

where

$$
\mu_i=\mu_{i_1}+\mu_{i_2}.
$$

## Verification

If at least one algebraic condition is not satisfied, the monomial parametrization is not valid for that parameter set.

For the parameter values from Pal et al. (2022), the algebraic conditions are not satisfied. Therefore, for those parameter values, the code-generated monomial parametrization does not describe a true equilibrium, and ACR and BCR cannot be concluded from it.

However, this does not mean that the monomial parametrization is incorrect. It only means that the chosen parameter values do not satisfy the required algebraic conditions. For parameter values satisfying all algebraic conditions, the monomial parametrization becomes valid.

## Valid Monomial Parametrization

For parameter values satisfying all required algebraic conditions, the valid monomial parametrization is

$$
S^*=\frac{\dfrac{\lambda}{2}}{\beta},
$$

$$
E^*=
\frac{\left(\dfrac{\lambda}{2}\right)\beta}
{\left(\dfrac{\lambda}{2}\right)(\mu_s+\gamma_{s_2}+\gamma_{s_1})},
$$

$$
Q^*=
\frac{\left(\dfrac{\lambda}{2}\right)\gamma_{e_1}}
{\mu_q(\mu_e+\gamma_{e_1}+\gamma_{e_2})},
$$

$$
I^*=
\frac{\left(\dfrac{\lambda}{2}\right)\gamma_{e_2}}
{\mu_i(\mu_e+\gamma_{e_1}+\gamma_{e_2})},
$$

$$
R^*=
\frac{\dfrac{\lambda}{2}}
{\mu_e+\gamma_{e_1}+\gamma_{e_2}}.
$$

## BCR and ACR Interpretation

Under these algebraic conditions, the compartments \(S\), \(E\), \(Q\), \(I\), and \(R\) exhibit balanced concentration robustness (BCR), since their steady-state values contain no free parameters.

However, since \(\delta=3>0\), absolute concentration robustness (ACR) cannot be concluded from the monomial parametrization alone.

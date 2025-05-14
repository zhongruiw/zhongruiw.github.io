---
title: Differences in the Formulations of Kalman Filter and Kalman-Bucy Filter
subtitle: The discrete-time filtering formulation differs from its continuous-time counterpart. To distinguish the difference, the observation error in discrete-time filter is referred to as 'measurement error,' whereas in the continuous-time filter, it is termed 'observation model noise.'
layout: blog_post
date: 2025-05-08
keywords: data assimilation, Kalman Filter
published: true
---

### Discrete-time filtering: Kalman filter

Consider a discrete-time dynamical system of the following form,
{% katexmm %}
$$
\begin{aligned}
\mathbf{x}_{n+1} &= \mathbf{M} \mathbf{x}_n + \bm{\mathsf{\Sigma}}_{\mathbf{x}} \mathbf{\epsilon}_{\mathbf{x},n} \\
\mathbf{y}_{n+1} &= \mathbf{H} \mathbf{x}_{n+1} + \bm{\mathsf{\Sigma}}_{\mathbf{y}} \mathbf{\epsilon}_{\mathbf{y},n+1}
\end{aligned}
$$
{% endkatexmm %}
where $\mathbf{x}_n$ and $\mathbf{y}_n$ are unobserved states and observations at discrete time $t_n$, respectively. 
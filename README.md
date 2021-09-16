# Candidacy-exam
EPFL Computer Science candidacy exam write-up

Title: Langevin Monte-Carlo without log-concavity

Langevin Monte Carlo (LMC) is a Markov Chain Monte Carlo sampling method that generate samples by adding gradient information to Gaussian noise. Since it queries only local information, we might expect it to have all the limitations of local methods like Gradient Descent. The presence of noise, however, makes LMC capable of provably sampling from a large class of distributions for which global information cannot be inferred from local queries. 
This statement was proved by Vempala and Wibisono in [1] under two mild assumptions. This will be the starting point of our report. We will then see that, although their work shows the region of tractability for LMC extends beyond strong log-concavity, there is a potential exponential blow-up of constants in the convergence bound that ensures that the computational hardness of non-convexity is never violated. Tzen et al's trajectory-wise analysis of LMC [2] will shed some light on the causes of this exponential blow-up of convergence time. With this understanding, we will naturally ask whether or not this blow-up occurs when trying to sample from real world distributions. The success of Song and Ermon's work [3] using LMC to generate natural images will help us argue that the real world may well be within the tractable region.

Papers:
 
- Vempala, Santosh, and Andre Wibisono. "Rapid Convergence of the Unadjusted Langevin Algorithm: Log-Sobolev Suffices." Proceedings of the 33rd Annual Conference on Neural Information Processing Systems. 2019. [paper](https://arxiv.org/abs/1903.08568)
- Tzen, Belinda, Tengyuan Liang, and Maxim Raginsky. "Local optimality and generalization guarantees for the langevin algorithm via empirical metastability." Conference on Learning Theory. PMLR, 2018.[paper](http://proceedings.mlr.press/v75/tzen18a.html)
- Song, Yang, and Stefano Ermon. "Generative Modeling by Estimating Gradients of the Data Distribution." Proceedings of the 33rd Annual Conference on Neural Information Processing Systems. 2019. [paper](https://arxiv.org/abs/1907.05600)

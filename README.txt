 Kernel Regularized Least Squares (KRLS) with Gaussian Kernel**

1. **Objective**

   * Learn how to use **Kernel Regularized Least Squares (KRLS)** with a **Gaussian (RBF) kernel**.
   * Explore the role of:

     * The **kernel parameter (σ² or τ)**
     * The **regularization parameter λ**
   * Understand their effect on **fitting** and **stability** .

2. **Mathematical Formulation**

   * Instead of a linear model, KRLS models predictions as:

     $$
     f(x) = \sum_{i=1}^n \alpha_i K(x_i, x)
     $$

     where $K(x_i, x) = \exp\left(-\frac{\|x_i - x\|^2}{\tau}\right)$ is the **Gaussian kernel**.
   * The weight vector **α** is computed as:

     $$
     \alpha = (K + \lambda I)^{-1} y
     $$

3. **Steps to Follow**

   * **Build the kernel matrix** using the Gaussian kernel for your training set.
   * For various values of **λ** and **τ (kernel width)**:

     * Compute **α**
     * Use it to make predictions
     * Evaluate:

       * Training error
       * Test error
   * This is a **non-parametric model**, meaning predictions depend directly on the training data.

4. **Hands-On Instructions**

   * Implement KRLS from scratch using:

     * A matrix-based approach for kernel computation
     * Looping over different λ and τ values
   * Plot:

     * Training and test errors as a function of λ (for fixed τ)
     * Training and test errors as a function of τ (for fixed λ)
   * Highlight the impact of these hyperparameters on:

     * **Model capacity**
     * **Bias-variance behavior**
     * **Overfitting/underfitting**

5. **Evaluation Strategy**

   * Use training data to analyze **fitting**.
   * Use separate test data to analyze **stability** (i.e., generalization).
   * Support findings with **plots** and **observations** .


## 📊 Credit Scoring Business Understanding

### 1. **The Basel II Accord and the Importance of Interpretability**

The **Basel II Accord** emphasizes **risk-sensitive capital requirements**, requiring banks to quantify and justify their credit risk exposure. This pushes financial institutions to use **models that are not only accurate but also interpretable and auditable**. Regulatory bodies must be able to understand the logic behind credit decisions. Hence, models must be transparent, well-documented, and based on **clear statistical and business logic**. This directly influences our need to use techniques such as **Weight of Evidence (WoE)** and **Logistic Regression**, which provide a clear path of reasoning from input features to credit decisions.

---

### 2. **The Need for a Proxy Variable and Associated Business Risks**

In many alternative data scenarios, especially in emerging markets or new digital lending environments, **direct default labels (i.e., whether a customer has failed to repay a loan)** may not be available. This necessitates the creation of a **proxy variable**—such as using **RFM segmentation to flag "disengaged" customers** as high-risk. While this allows model training, it comes with **significant business risks**:
- **Label Noise:** Proxies may not accurately reflect actual default behavior, leading to poor model generalization.
- **Bias Introduction:** Incorrectly labeled customers could cause **misclassification** of creditworthy individuals.
- **Reputational & Regulatory Risk:** Decisions based on weak proxies may not stand up to regulatory scrutiny or may unfairly impact certain groups.

Therefore, while proxies are a practical workaround, they must be designed and validated with extreme care.

---

### 3. **Trade-offs Between Interpretability and Performance**

There is a fundamental trade-off between:
- **Simple, interpretable models** like **Logistic Regression with WoE**:
  - ✅ Highly interpretable and auditable
  - ✅ Easier to explain to regulators and stakeholders
  - ❌ May not capture complex relationships in data
- **Complex models** like **Gradient Boosting Machines (GBM)**:
  - ✅ Higher predictive power
  - ✅ Better performance with non-linear and high-dimensional data
  - ❌ Opaque "black box" logic
  - ❌ Requires model explainability tools (e.g., SHAP) for interpretation

In regulated environments, **interpretability often takes precedence**, especially when models affect customer financial decisions. However, performance gains from complex models may justify their use if combined with robust explainability and monitoring tools.

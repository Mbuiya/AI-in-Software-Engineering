# Assignment: Tools & Resources for AI in Software Engineering

**AI Tools:**  
- **GitHub Copilot**
- **Testim.io**
- **Google Colab**

**Datasets:**  
- Kaggle  
- GitHub Issues

**Libraries:**  
- Scikit-learn  
- Pandas  
- Selenium

---

### Why This Matters

- **Career Relevance:**  
  Mastering AI tools like Copilot and Selenium is highly valued in today’s tech roles.
- **Ethical Awareness:**  
  This assignment prepares you to engineer fair and inclusive AI-driven software.

**Deadline:** 7 days  
Let’s engineer smarter software! 🚀

Need Help?  
- Use documentation: GitHub Copilot, Testim  
- Join the Community: `#AISoftwareAssignment`
- **Pro Tip:** Start early & test incrementally—AI thrives on iteration! 🔄

---

## Part 1: Theoretical Analysis (30%)

### 1. Short Answer Questions

**Q1:** *Explain how AI-driven code generation tools (e.g., GitHub Copilot) reduce development time. What are their limitations?*  
A1:  
AI-driven code generation tools predict and suggest code snippets based on context, reducing boilerplate work, accelerating prototyping, and catching common patterns. However, their limitations are incomplete understanding of business logic, possible generation of insecure or buggy code, and reliance on quality training datasets—sometimes producing generic or outdated solutions.

**Q2:** *Compare supervised and unsupervised learning in the context of automated bug detection.*  
A2:  
Supervised learning uses labeled bug data to train models to identify known defect patterns. It’s effective when bug data is available but may miss new or rare bug types. Unsupervised learning finds anomalies by clustering or detecting outliers in code behavior, uncovering unseen issues, but may result in higher false positives due to lack of explicit labels.

**Q3:** *Why is bias mitigation critical when using AI for user experience personalization?*  
A3:  
Bias mitigation ensures AI-driven personalization treats users fairly, avoids reinforcing stereotypes, and prevents exclusion of minority groups. Unchecked bias can result in unfair recommendations, reduced user trust, and negative social impact.

---

### 2. Case Study Analysis

**Read:** *AI in DevOps: Automating Deployment Pipelines*

**Answer:**  
AIOps improves software deployment efficiency through automation, faster error detection, and predictive failure prevention.  
**Examples:**  
1. Automated rollback triggered by anomaly detection in deployment logs.  
2. Dynamic resource allocation optimizing server usage based on live metrics.

---

## Part 2: Practical Implementation (60%)

### Task 1: AI-Powered Code Completion Tool

- **Tool:** GitHub Copilot or Tabnine

**Task:**  
Write a Python function to sort a list of dictionaries by a specific key.

```python
# AI-suggested code by Copilot
def sort_dicts_by_key(dicts, key):
    return sorted(dicts, key=lambda x: x[key])

# Manual implementation
def manual_sort_dicts_by_key(dicts, key):
    for i in range(len(dicts)):
        for j in range(i+1, len(dicts)):
            if dicts[i][key] > dicts[j][key]:
                dicts[i], dicts[j] = dicts[j], dicts[i]
    return dicts
```

**Analysis (200 words):**  
The AI-suggested function leverages Python’s built-in `sorted` and `lambda`, yielding concise and efficient code, optimizing for readability and performance (O(n log n)). The manual implementation uses a nested loop (bubble sort) with O(n²) complexity, less efficient and more error-prone. AI tools like Copilot propose best practices and standard library usage, reducing implementation time and learning curve. Manual writing, while educational, risks introducing subtle bugs and inefficiencies. AI assistance accelerates routine coding but should be validated for correctness in complex logic.

---

### Task 2: Automated Testing with AI Framework

- **Tool:** Selenium IDE with AI features, Testim.io

**Task:**  
Automate a test case for a login page (valid/invalid credentials).

**Test script sample (Selenium IDE):**
```python
# Pseudocode for Selenium test
def test_login_valid(driver):
    driver.get("https://example.com/login")
    driver.find_element("username").send_keys("validUser")
    driver.find_element("password").send_keys("validPass")
    driver.find_element("loginBtn").click()
    assert "Dashboard" in driver.page_source

def test_login_invalid(driver):
    driver.get("https://example.com/login")
    driver.find_element("username").send_keys("invalidUser")
    driver.find_element("password").send_keys("wrongPass")
    driver.find_element("loginBtn").click()
    assert "error" in driver.page_source
```
*Insert screenshot of results here.*

**Summary (150 words):**  
AI-powered testing tools suggest test flows, auto-generate scripts, and adapt assertions based on page structure, increasing coverage and robustness. Manual testing requires repetition and is prone to omission. AI frameworks expand test scenarios dynamically (e.g., edge cases, UI changes), boosting defect detection and reducing maintenance overhead.

---

### Task 3: Predictive Analytics for Resource Allocation

- **Dataset:** Kaggle Breast Cancer Dataset

**Steps:**  
- Preprocess: Clean, label, split data  
- Train model: Random Forest predicts issue priorities  
- Evaluate: Accuracy & F1-score

*Attach Jupyter Notebook here and highlight performance metrics.*

---

## Part 3: Ethical Reflection (10%)

**Prompt response:**  
Deploying the predictive model may expose bias if the dataset underrepresents certain teams, leading to unfair priority classifications. IBM AI Fairness 360 can audit, visualize, and rectify such biases, ensuring equitable recommendations across user groups by re-weighting attributes and introducing fairness constraints.

---

## Bonus Task (Extra 10%)

**Innovation Challenge Proposal**  
*AI-Powered Automated Documentation Generator*

**Purpose:**  
Automatically generates module and API documentation from source code and code comments using NLP.

**Workflow:**  
- Scans repositories for undocumented code.
- Summarizes functions/classes using AI.
- Integrates with CI/CD for continual updates.

**Impact:**  
Reduces engineering time spent on documentation, increases codebase accessibility, and enhances onboarding for new developers.

---

**End of Assignment**

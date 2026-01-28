<img width="1280" height="640" alt="github" src="https://github.com/user-attachments/assets/d47a6f4a-04fc-4bbc-a8d2-012d74c5ebdb" />

# 👋 Hi, I'm Marco Rosado

**Data Analyst** focused on problem-first analysis, risk-aware metrics, and operational efficiency.  
Working with **Python, Pandas, and SQL**. Fintech-oriented | Medical background applied beyond clinical practice.

---

## 🔍 About me
I approach data analysis starting from the problem, not the tool.  
My background in regulated, high-impact environments shaped the way I work with data:  
prioritizing data quality, understanding risk, and translating insights into actionable decisions.

I’m currently transitioning fully into tech, building projects that reflect real-world constraints, imperfect data, and operational impact — especially in fintech-related use cases.

---

## 🧰 Tech stack
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)&nbsp;
![SQL](https://img.shields.io/badge/sql-003B57?style=for-the-badge&logo=postgresql&logoColor=white)&nbsp;
![Pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)&nbsp;
![NumPy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)&nbsp;
![Matplotlib](https://img.shields.io/badge/matplotlib-11557C?style=for-the-badge&logo=plotly&logoColor=white)&nbsp;
![Seaborn](https://img.shields.io/badge/seaborn-4C72B0?style=for-the-badge&logo=python&logoColor=white)&nbsp;
![Google Sheets](https://img.shields.io/badge/google%20sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)&nbsp;
- **Languages & Tools:** Python, SQL  
- **Libraries:** Pandas, NumPy, Matplotlib  
- **Focus areas:** Data cleaning, exploratory analysis, risk-oriented metrics, operational insights

---

## 🚀 What I’m working on
- Data analysis projects with a **problem-first mindset**
- Simulated fintech use cases (risk, operations, decision metrics)
- Improving data quality and analytical storytelling

---

## 📌 Featured projects
*(Pinned repositories below 👇)*  
Each project includes context, methodology, and conclusions — not just code.

---

## 🤝 Open to collaborate on
- Data analysis projects with real-world constraints  
- Fintech, risk, or operations-focused datasets  
- Exploratory analysis where decision-making matters

---

## 📫 Contact
- ![LinkedIn](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)&nbsp; [linkedin.com/in/dr-marco-rosado](https://www.linkedin.com/in/dr-marco-rosado/)
- ![Gmail](https://img.shields.io/badge/gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)&nbsp; marcorosado1@gmail.com

---

> *“Data is only useful when it helps someone make a better decision.”*

### 🧠 Example of Applied Data Thinking (Health Context)

```python
import pandas as pd

# Load anonymized health dataset
df = pd.read_csv("occupational_health_events.csv")

# Problem-first: identify risk concentration, not averages
risk_by_area = (
    df.groupby("work_area")
      .agg(
          incidents=("event_id", "count"),
          severe_cases=("severity", lambda x: (x >= 4).sum())
      )
      .assign(severity_rate=lambda x: x.severe_cases / x.incidents)
      .sort_values("severity_rate", ascending=False)
)

risk_by_area.head()

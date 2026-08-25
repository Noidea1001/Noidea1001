<div align="center">

# ERROR404

**Systems Architect | Backend Engineering Lead | Full-Stack Developer**

[Phnom Penh, Cambodia](https://github.com/Noidea1001) • [khvysal@gmail.com](mailto:khvysal@gmail.com) • [Explore My Portfolio](https://github.com/Noidea1001/MyPortfolio)

---

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=24&pause=1000&color=2E86AB&center=true&vcenter=true&width=600&lines=High-Availability+System+Architecture;API+Security+%26+Performance;Scalable+Web+Ecosystems" alt="Typing SVG" />

</div>

---

## 👨‍💻 Executive Summary

Software Developer and Systems Architect specialized in designing high-concurrency backend systems and secure API ecosystems. Leveraging expertise in structured database design, authentication protocols (JWT), and optimized request handling to build resilient, scalable software solutions. Based in Phnom Penh.

---

## 📈 Engineering Analytics & Metrics

*This section visualizes core engineering output, including contribution distribution, technology proficiency, and velocity.*

<div align="center">
  <a href="https://github.com/Noidea1001">
    <img src="https://github-readme-stats.vercel.app/api?username=Noidea1001&show_icons=true&theme=dark&hide_border=true&count_private=true&include_all_commits=true" alt="Error404's Engineering Productivity Metrics" width="48%" />
  </a>
  <a href="https://github.com/Noidea1001">
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Noidea1001&layout=compact&theme=dark&hide_border=true&langs_count=8" alt="Technology and Language Distribution" width="48%" />
  </a>
</div>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Noidea1001&theme=dark&hide_border=true&mode=daily" alt="Commit Consistency Streak" width="97%" />
</div>

---

## 🛠️ Technology Stack & Core Competencies

<div align="center">

| Area of Expertise | Verified Technologies & Tools |
| :--- | :--- |
| **Core Languages** | ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white) |
| **Architectures** | RESTful API Design, Microservices, Event-Driven Architecture, JWT/OAuth |
| **Infrastructure/CI** | Git, GitHub Actions, Linux Environments, Docker |

</div>

---

## 🏗️ Featured Project Architecture & Technical Demos

*Detailed architectural overviews and dynamic demonstrations of primary engineering output.*

### 1. Bank Account Management API
> **Key Attributes:** REST Architecture, Python, Transaction Integrity, Security First.  
> **Overview:** An optimized backend service engineered to handle core ledger operations, including transaction validation, balance synchronization, and data encryption.

<div align="center">
  <img src="https://github.com/Noidea1001/Bank_account_api/raw/main/assets/demo_api_validation.gif" alt="Technical Demonstration: API Validation and Transaction Workflow" width="90%" style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.2);" />
</div>

<details>
  <summary><b>View Core Python Implementation (Schema & Logic)</b></summary>
  
  ```python
  # Optimized Ledger Update Logic
  class LedgerEntry(models.Model):
      account = models.ForeignKey(Account, on_delete=models.CASCADE)
      transaction_type = models.CharField(max_length=10, choices=TRANSACTION_TYPES)
      amount = models.DecimalField(max_digits=12, decimal_places=2)
      timestamp = models.DateTimeField(auto_auto_now_add=True)
      
      @transaction.atomic
      def process_transaction(self):
          if self.transaction_type == 'DEBIT' and self.account.balance < self.amount:
              raise InsufficientFundsError()
          
          # Implementation logic
          # ...

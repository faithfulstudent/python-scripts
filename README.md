# python-scripts
Building practical cyber defense capabilities through Python scripting, access control modeling, and foundational security automation.

---

# 🛡️ Access Control Authentication Simulator (Python)

A foundational Python project that simulates a basic access control and authentication mechanism.

This project demonstrates core cybersecurity principles including identity verification, authorization logic, and access decision workflows — foundational concepts in defensive security and SOC environments.

---

## 🎯 Project Objective

This project was developed as part of my cybersecurity learning path with a focus on **defensive security and access control mechanisms**.

The goal is to model:

* Credential intake
* Identity validation
* Authorization checks
* Controlled access decision-making
* Defensive logic flow

Although simple in structure, it reflects the fundamental building blocks used in larger identity and access management (IAM) systems.

---

## 🔐 Cyber Defense Concepts Demonstrated

This project aligns with several key defensive security principles:

### 1️⃣ Authentication vs Authorization

* **Authentication** → Identifying who the user claims to be (name input)
* **Authorization** → Verifying whether the user is allowed access (list comparison)

### 2️⃣ Access Control Logic

* Whitelisting approach (authorized user list)
* Boolean access flag control
* Controlled execution flow

### 3️⃣ Defensive Programming Practices

* Input normalization using `.title()`
* Logical separation via functions
* Controlled access loop
* Clear privilege decision point

---

## 🧠 How the Code Works

### 1. `getname()`

Captures user input and standardizes formatting.

```python
def getname():
    entry = input('Please enter your name: ')
    return entry.title()
```

Security relevance:

* Reduces case-based bypass attempts (e.g., "john" vs "John")
* Basic input normalization practice

---

### 2. `Authorize(name)`

Compares input against an authorized whitelist.

```python
def Authorize(name):
    Access_Granted = False
    AList =  ['John', 'Bill', 'Tom']

    for person in AList:
        if person == name:
            Access_Granted = True
    return Access_Granted
```

Security relevance:

* Implements a whitelist model
* Uses explicit authorization logic
* Returns a controlled Boolean access decision

---

### 3. Main Execution Flow

* Prompts for access request
* Requests credentials
* Evaluates authorization
* Grants or denies access
* Re-prompts if denied

This mimics a simplified access gateway workflow.

---

## 🏗️ System Flow

```
User Requests Access
        ↓
Enter Identity
        ↓
Normalize Input
        ↓
Compare Against Authorized List
        ↓
Access Granted / Access Denied
```

---

## 🚀 How to Run

```bash
git clone https://github.com/yourusername/access-control-simulator.git
cd access-control-simulator
python main.py
```

---

## 🔍 Security Strengths

* Demonstrates core IAM logic
* Clean function separation
* Boolean-based access control
* Whitelist implementation
* Loop-controlled authentication attempts
* Structured logic flow

---

## ⚠️ Security Limitations (Learning Reflection)

As part of building a strong cyber defense profile, recognizing weaknesses is critical.

Current limitations:

* Plain-text identity validation
* No password or multi-factor authentication
* Hardcoded whitelist
* No logging or monitoring
* No rate limiting (brute force protection)
* No hashing or secure credential storage

Identifying these gaps is an essential defensive skill.

---

## 🔮 Planned Enhancements (Blue Team Focused)

To evolve this project toward real-world defensive relevance:

* 🔐 Add password-based authentication
* 🔑 Implement hashed credential storage (e.g., `hashlib`)
* 📁 Store users securely in external file or database
* 🚨 Add logging for failed attempts
* ⏳ Implement lockout after repeated failures
* 📊 Add monitoring metrics
* 🛡 Input validation hardening
* 🔍 Add intrusion detection logic for brute-force patterns

---

## 🛡️ Career Alignment – Cyber Defense Path

This project demonstrates early-stage competencies aligned with:

* SOC Analyst (Tier 1)
* Blue Team Engineer
* Identity & Access Management (IAM) Analyst
* Security Operations Intern
* Junior Cybersecurity Analyst

### Skills Highlighted

* Defensive mindset
* Authentication workflow logic
* Access control modeling
* Python scripting for security
* Structured program design
* Understanding of authorization principles

---

## 📚 Learning Takeaways

Through this project I practiced:

* Translating security concepts into executable logic
* Building structured access control systems
* Recognizing authentication vs authorization distinctions
* Identifying security gaps in simple systems
* Thinking from a defensive architecture perspective

---

## 👤 About Me

I am actively building a cybersecurity portfolio with a focus on:

* Defensive security engineering
* Security automation
* Access control systems
* Monitoring & detection logic
* Python-based security tooling

This project represents foundational work toward developing a strong blue team skill set.

---

## 📄 License

MIT License

---

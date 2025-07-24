# Tricentis-Tosca-AS1-AS2

## Tosca AS1 Topics 

### 1. Introduction 
- [RoadMap](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Automating%20web%20application%20testing_Roadmap.pdf)
- [Additional Material Base - 1 ](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/tree/main/AS1_Additional_Material_Base%20(1))
- [Automation-Specialist-level -1](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/tree/main/Automation_Specialist_Level_1_Base%20(1))

<br>


### Single User Workspace
- A local workspace used by one user only.
- No synchronization or version control with a shared repository.
- Best for individual projects, learning, or PoC (Proof of Concept) work.

<br>

#### 🔹 Key Points:
```
❌ No check-in/check-out mechanism.
✅ Changes are saved directly and locally.
❌ Cannot collaborate with team members simultaneously.
✅ Easier setup; no need to configure Tosca Server or repository.

```

<br>


### 🔹 When to Use:
- For training or learning Tosca.
- For quick prototype test cases.
- When working on isolated tasks.

  
<br>

## Multi User Workspace
```
🔹 What is a Multi User Workspace?
- A collaborative workspace setup where multiple testers work on the same Tosca project.
- Connected to a common central repository (Tosca Server or TDS – Tosca Distributed Server).

```

<br>

#### 🔹 Key Points:
```
- ✅ Supports check-in / check-out functionality.
- ✅ Enables team collaboration and version control.
- ✅ Prevents conflicts by locking objects when edited.
- ❌ Needs setup with Tosca Server (or similar).
```
<br>


### 🔹 Features:
- 🔄 Update All – To get the latest changes from the repository.
- 📤 Check-In – To upload your changes.
- 🔍 Conflict resolution – If two users edit the same object.

<br>

### 🔹 When to Use:
- In team environments.
- For large-scale test automation projects.
- When working in agile/scrum teams needing frequent collaboration.


### [Exercise - 1 (Workspace Setup) ](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_1%20(2).pdf)


### [Exercise - 2 (Navigate to SUT) ](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_2%20(2).pdf)

---
<br>

## Modules

###  Model-Based Test Automation

##🔹 What is Model-Based Test Automation?
- Based Automation means creating test cases by reusing models (modules) instead of writing scripts manually.
- In Tosca, these models are called Modules, which represent the UI/API elements of the system under test.

  <br>

## 🔹 Key Concepts:
- 🧩 Modules: Represent UI/API objects (like buttons, fields).
<br>
  

## 🧪 TestCases: Built using those modules — no need to write code.
- 🔁 Reusable: Once a module is scanned, you can reuse it across many test cases.
- 🖱️ Drag & Drop: TestSteps are created using a visual interface, not code.

<br>

## 🔹 How It Works in Tosca:
```
- Scan the application to create modules.
- Create TestCases by dragging module elements into TestSteps.
- Parameterize with TestData for flexibility.
- Run the TestCase — Tosca handles the execution.
```

<br>


## 🔹 Benefits:
```
✅ Faster automation
✅ Easier maintenance
✅ Low-code / no-code
✅ Highly reusable

```

<br>

## [Exercise - 3 (Module Section)](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_3%20(1).pdf)

##  Standard Modules 



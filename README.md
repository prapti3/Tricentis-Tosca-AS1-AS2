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

### 🔹 What is a Multi User Workspace?
```

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


 [Exercise - 1 (Workspace Setup) ](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_1%20(2).pdf)

 [Exercise - 2 (Navigate to SUT) ](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_2%20(2).pdf)

---
<br>

## Modules

###  Model-Based Test Automation

##🔹 What is Model-Based Test Automation?
```
Based Automation means creating test cases by reusing models (modules) instead of writing scripts manually.
In Tosca, these models are called Modules, which represent the UI/API elements of the system under test.
```
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

### [Exercise - 3 (Module Section)](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_3%20(1).pdf)


##  Standard Modules 

### 🔹 What is a Standard Module in Tosca?
- Standard Modules are predefined modules provided by Tosca for commonly used operations.
- They are built-in and do not require scanning any application.

### 🔹 Key Features:

##### 🛠️ Ready to use — no need to scan

- 🔄 Useful for general actions (e.g., wait, open URL, close browser)
- 📚 Located under Standard folder in the Modules section

##### 🔹 Common Standard Modules:
```
Standard Module	Purpose
TBox Set	Sets a value in an input field
TBox Click	Performs click action
TBox Wait	Waits for a condition or time
TBox Open URL	Opens a given URL in a browser
TBox Verify	Verifies expected value
TBox Loop	Loops through steps or data
TBox FileOperations	File read/write or handling operations
```

#### 🔹 Why Use Standard Modules?
- ✅ Save time — no scanning needed
- ✅ Reliable and optimized by Tricentis
- ✅ Can be used across all projects


---
<br>


## XSCAN 

### 🔹 What is XScan in Tosca?
- XScan (Tosca XModule Scanner) is Tosca’s tool for scanning and identifying elements (like buttons, fields, dropdowns) from an application’s UI or API.
- It helps you create Modules, which are the building blocks for your TestCases.

<br> 


### 🔹 Key Points:
- 🔍 Used to scan desktop, web, mobile, or API applications.
- 🧱 Generates Modules with controls (like Username field, Login button, etc.).
- 🎯 Captures technical information behind the UI (XPath, ID, Name, etc.).

<br>


### 🔹 Types of XScan:
| Type            | Used For                            |
| --------------- | ----------------------------------- |
| **Tosca XScan** | For web/desktop/mobile applications |
| **API Scan**    | For scanning APIs (REST/SOAP)       |


<br>


### 🔹 How to Use XScan:

- Open Tosca Commander.
- Right-click a Module folder → Select Scan.
- Choose the application window.
- Start scanning elements.
- Save → A Module is created with all scanned controls.

<br> 


### 🔹 Why is XScan Important?
- ✅ No need to write locators manually.
- ✅ Ensures accurate identification of elements.
- ✅ Reusability — scanned Modules can be used in multiple test cases.

---
<br>


## Identify Controls by Properties in XScan

### 🔹 Identifying Controls by Properties and Anchor in Tosca
- When Tosca scans elements (controls), it uses technical properties and sometimes anchor elements to reliably locate those controls during execution.


### ✅ 1. Identify by Properties (Attributes):
 - Tosca checks HTML or technical properties like:

| Property Type | Examples                 |
| ------------- | ------------------------ |
| ID            | `id="username"`          |
| Name          | `name="email"`           |
| Type          | `type="text"`            |
| Class         | `class="form-control"`   |
| InnerText     | Button text, labels      |
| XPath/CSS     | Auto-generated if needed |

- 🧠 Best Practice: Use unique and stable properties to avoid flaky tests.

---
<br>


### ✅ 2. Identify by Anchor:
- If a control doesn’t have unique properties, Tosca uses a nearby anchor element (like a label or surrounding text) to find it.

- 🔹 How it works:
    - Anchor is a neighboring element with stable identification.
    - Tosca finds the control relative to this anchor.

<br>

📌 Example:
- If a textbox has no unique ID but is next to a label “Email”, Tosca uses “Email” as the anchor to locate the textbox.

---
<br>

### 🔧 In XScan:
- After scanning a control, you can:
  - ✅ Adjust identification properties
  - ➕ Add or change anchors
  - ⚙️ Set weights to prioritize properties
 
---
<br>

### 🔹 Summary:


| Technique         | When to Use                                                    |
| ----------------- | -------------------------------------------------------------- |
| **By Properties** | Element has unique, stable attributes                          |
| **By Anchor**     | Element has **no stable ID**, but nearby stable element exists |



#### [Exercise - 4 (Identify Control by Prop and Anchor)](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_4%20(1).pdf)


---
<br>


### 💠 Testcase 


#### 🔹 What is a TestCase in Tosca?
- A TestCase in Tosca is a sequence of TestSteps that performs an automated test on your application. It defines what to test, how to test, and what data to use.
- It is the core object used for building your automation logic.

<br>

#### 🔹 Key Components of a TestCase:
| Component           | Purpose                                       |
| ------------------- | --------------------------------------------- |
| **TestSteps**       | Actions to perform (click, set, verify, etc.) |
| **TestStepValues**  | Specific values/data to be used in TestSteps  |
| **TestCase Folder** | Logical grouping for organizing TestCases     |

<br>


#### 🔹 How to Create a TestCase:
1. Go to TestCases section in Tosca Commander.
2. Right-click a folder → Create TestCase.
3. Drag and drop Modules to add TestSteps.
4. Enter input/output values as needed.
5. Link TestData if required.
6. Run in ScratchBook or ExecutionList.


<br>

#### 🔹 Example (Login TestCase):
| Step | Module        | Action | Value     |
| ---- | ------------- | ------ | --------- |
| 1    | `Username`    | Set    | `user123` |
| 2    | `Password`    | Set    | `pass123` |
| 3    | `LoginBtn`    | Click  | —         |
| 4    | `WelcomeText` | Verify | `Welcome` |

<br>


#### 🔹 Features:
- ✅ Reusable across multiple executions
- ✅ Parameterization via TestCaseDesign or TCP
- ✅ Data-driven, modular, and easy to maintain


### [Exericse - 5 (Testcase Section)](https://github.com/prapti3/Tricentis-Tosca-AS1-AS2/blob/main/Exercise/Exercise_5%20(1).pdf)





# Microsoft Certified: Dynamics 365 Business Central Developer Associate (MB-820)

[![Microsoft Certification](https://img.shields.io/badge/Microsoft%20Certified-Business%20Central%20Developer%20Associate-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/credentials/certifications/)
[![Exam Code](https://img.shields.io/badge/Exam%20Code-MB-820-brightgreen?style=for-the-badge&logo=github)](https://learn.microsoft.com/en-us/credentials/certifications/)
[![Passing Score](https://img.shields.io/badge/Passing%20Score-700%2F1000-blue?style=for-the-badge)](https://learn.microsoft.com/en-us/credentials/certifications/)
[![Practice Materials](https://img.shields.io/badge/Practice%20Materials-MB-820-orange?style=for-the-badge)](https://www.certsclub.com/microsoft/)

---

## 📖 Table of Contents
1. [Exam Overview](#-exam-overview)
2. [How to Prepare](#-how-to-prepare)
3. [Exam Blueprint & Skills Measured](#-exam-blueprint--skills-measured)
4. [Practice & Preparation Materials](#-practice--preparation-materials)
5. [10 Realistic Demo Practice Questions & Answers](#-10-realistic-demo-practice-questions--answers)
6. [Community Discussion & Study Group](#-community-discussion--study-group)
7. [Detailed Topic Documentation Index](#-detailed-topic-documentation-index)
8. [Official Microsoft Learning Resources](#-official-microsoft-learning-resources)

---

## 🎯 Exam Overview

Exam MB-820 validates developer expertise in designing, developing, testing, and debugging solutions using the AL programming language, Visual Studio Code, AL Extension architecture, and Azure integrations for Microsoft Dynamics 365 Business Central.

### Quick Facts
| Attribute | Specification |
| :--- | :--- |
| **Exam Code** | **MB-820** |
| **Certification Name** | **Microsoft Certified: Dynamics 365 Business Central Developer Associate (MB-820)** |
| **Passing Score** | 700 / 1000 (Scaled Score) |
| **Official Portal** | [Microsoft Learn Credentials](https://learn.microsoft.com/en-us/credentials/certifications/) |

---

## 🚀 How to Prepare

- 🔗 **Review the Exam MB-820 page for exam registration and other details:**  
  Visit the [Official Microsoft Exam Registration Page](https://learn.microsoft.com/en-us/credentials/certifications/) to review scheduling options via Pearson VUE.
  
- 📚 **Explore the Official Study Guide:**  
  Review the official Microsoft study guide for an itemized breakdown of testable objectives.

- 👥 **Connect with Microsoft Training Services Partners:**  
  Find authorized training partners worldwide at the [Microsoft Training Services Partner Directory](https://learn.microsoft.com/en-us/credentials/support/help#training-services-partners).

---

## 📊 Exam Blueprint & Skills Measured

| Domain / Skill Area | Weighting |
| :--- | :---: |
| **Describe Business Central architecture** | **10–15%** |
| **Develop apps for Business Central by using AL** | **40–45%** |
| **Design user interfaces by using AL** | **15–20%** |
| **Integrate Business Central with other systems** | **15–20%** |
| **Test, manage, and debug solutions** | **10–15%** |

---

## 💡 Practice & Preparation Materials

For comprehensive practice tests, high-yield scenario questions, and full-length exam simulations, explore the dedicated practice resources for [MB-820](https://www.certsclub.com/microsoft/).

---

## 📝 10 Realistic Demo Practice Questions & Answers

### Question 1 (Domain: AL Extensibility)
**Scenario / Question:** In Business Central AL development, which object type is used to add new custom fields or modify properties on an existing standard table (such as the Customer table) without modifying base code?
- A) TableExtension
- B) Table
- C) PageExtension
- D) Codeunit
- **Correct Answer:** **A**
- **Detailed Explanation:** `TableExtension` objects allow developers to extend standard tables by adding new fields, keys, FlowFields, and field triggers non-intrusively.

---
### Question 2 (Domain: Event Architecture)
**Scenario / Question:** You need to execute custom validation logic right before a Sales Header record is deleted. Which attribute is placed above the AL procedure to subscribe to the standard table deletion event?
- A) `[EventSubscriber(ObjectType::Table, Database::\"Sales Header\", 'OnBeforeDeleteEvent', '', false, false)]`
- B) `[BusinessEvent]`
- C) `[Test]`
- D) `[Commit]`
- **Correct Answer:** **A**
- **Detailed Explanation:** The `[EventSubscriber]` attribute hooks an AL procedure to a specific trigger event (e.g., `OnBeforeDeleteEvent`) published by standard Business Central objects.

---
### Question 3 (Domain: API Development)
**Scenario / Question:** You need to create a modern, high-performance REST API in Business Central that can be consumed by Power Automate and external microservices. Which page type should you define in AL?
- A) `PageType = API;` with `APIPublisher`, `APIGroup`, `APIVersion`, `EntityName`, and `EntitySetName` properties set
- B) `PageType = Card;`
- C) `PageType = List;`
- D) `PageType = NavigatePage;`
- **Correct Answer:** **A**
- **Detailed Explanation:** API pages (`PageType = API`) publish lightweight, performant, entity-based OData v4 REST endpoints designed specifically for cloud integrations.

---
### Question 4 (Domain: FlowFields)
**Scenario / Question:** In AL table design, you define a FlowField column that dynamically displays the total outstanding balance from Customer Ledger Entries. Why does a FlowField require calling `Rec.CalcFields(\"Balance (LCY)\")` in AL code before reading its value?
- A) FlowFields are virtual calculated fields not stored physically in the SQL table; `CalcFields` evaluates their CalculationFormula on-demand
- B) It compiles the C# DLL
- C) It restarts the service tier
- D) It locks the database
- **Correct Answer:** **A**
- **Detailed Explanation:** FlowFields do not store static values in the database; calling `CalcFields` executes the underlying calculation formula query to populate the value in memory.

---
### Question 5 (Domain: Data Upgrade)
**Scenario / Question:** When publishing a new version of an AL extension that restructures existing data into a new schema, which special codeunit subtype should you use to migrate and transform existing tenant records?
- A) `Subtype = Upgrade;`
- B) `Subtype = Test;`
- C) `Subtype = Install;`
- D) `Subtype = Normal;`
- **Correct Answer:** **A**
- **Detailed Explanation:** Upgrade codeunits (`Subtype = Upgrade`) contain `OnUpgradePerCompany` and `OnUpgradePerDatabase` triggers to safely migrate data between extension versions.

---
### Question 6 (Domain: AL Language & Record Navigation)
**Scenario / Question:** Which AL record function is recommended for iterating through a filtered set of records in a `repeat...until` loop while optimizing client-to-server data streaming?
- A) `if Customer.FindSet() then repeat ... until Customer.Next() = 0;`
- B) `if Customer.FindFirst() then ...`
- C) `Customer.Get()`
- D) `Customer.Count()`
- **Correct Answer:** **A**
- **Detailed Explanation:** `FindSet()` fetches an optimized dataset chunk for forward looping, which is best practice when iterating through sets of records.

---
### Question 7 (Domain: Telemetry & Diagnostics)
**Scenario / Question:** How should an AL developer log structured diagnostics and custom error metrics from an AL extension directly into an Azure Application Insights instance for cloud monitoring?
- A) `Session.LogMessage('Tag001', 'Custom message', Verbosity::Normal, DataClassification::SystemMetadata, TelemetryScope::ExtensionPublisher, customDimensions);`
- B) `Message('Error')`
- C) `Error('Crash')`
- D) `Dialog.Open()`
- **Correct Answer:** **A**
- **Detailed Explanation:** `Session.LogMessage` sends structured telemetry events with custom dimensions directly to the configured Azure Application Insights instance.

---
### Question 8 (Domain: Generative AI UI)
**Scenario / Question:** Which modern Page Type introduced in recent Business Central versions allows developers to build interactive AI copilot generative modal experiences with user prompt inputs and AI-generated proposals?
- A) `PageType = PromptDialog;`
- B) `PageType = Card;`
- C) `PageType = List;`
- D) `PageType = Worksheet;`
- **Correct Answer:** **A**
- **Detailed Explanation:** `PromptDialog` pages provide the standard user experience for building AI copilot capabilities, allowing prompt inputs and reviewing generated suggestions.

---
### Question 9 (Domain: Page Extensions)
**Scenario / Question:** In an AL `PageExtension` object, which syntax is used to insert a custom field immediately after the `Name` field on a standard card page?
- A) `addafter(Name) { field(\"Custom Field\"; Rec.\"Custom Field\") { ApplicationArea = All; } }`
- B) `insert Name`
- C) `modify(Name)`
- D) `delete(Name)`
- **Correct Answer:** **A**
- **Detailed Explanation:** `addafter(AnchorControl)` adds custom UI elements immediately following the designated target control on extended pages.

---
### Question 10 (Domain: Automated Testing)
**Scenario / Question:** Which codeunit subtype is used by Business Central developers to write automated test suites that can assert expected behavior without committing test transactions to the production database?
- A) `Subtype = Test;`
- B) `Subtype = Install;`
- C) `Subtype = Upgrade;`
- D) `Subtype = Normal;`
- **Correct Answer:** **A**
- **Detailed Explanation:** Test codeunits (`Subtype = Test`) execute isolated test methods using `[Test]` attributes and `Assert` libraries, automatically rolling back changes after test execution.

---

## 💬 Community Discussion & Study Group

Have questions regarding MB-820 concepts, study plans, or exam strategies?
- 💬 **Ask a question or start a topic:** [GitHub Discussions](https://github.com/MicrosoftLearnHub/MB-820---Microsoft-Dynamics-365-Business-Central-Developer/discussions)
- 🐛 **Report corrections or suggest updates:** [GitHub Issues](https://github.com/MicrosoftLearnHub/MB-820---Microsoft-Dynamics-365-Business-Central-Developer/issues)
- 🤝 **Contribute:** Open a Pull Request to share study notes, architecture diagrams, and review materials.

---

## 📂 Detailed Topic Documentation Index

- 📘 [01-architecture-and-extensions.md](./docs/01-architecture-and-extensions.md)
- 📘 [02-al-programming-language.md](./docs/02-al-programming-language.md)
- 📘 [03-tables-and-table-extensions.md](./docs/03-tables-and-table-extensions.md)
- 📘 [04-ui-pages-and-page-extensions.md](./docs/04-ui-pages-and-page-extensions.md)
- 📘 [05-reports-queries-and-xmlports.md](./docs/05-reports-queries-and-xmlports.md)
- 📘 [06-integration-and-webservices.md](./docs/06-integration-and-webservices.md)
- 📘 [07-official-resources-and-links.md](./docs/07-official-resources-and-links.md)

---

## 🌐 Official Microsoft Learning Resources

- 🌐 [Microsoft Learn Certification Directory](https://learn.microsoft.com/en-us/credentials/certifications/)
- 🌐 [Microsoft Learn Free Interactive Modules](https://learn.microsoft.com/en-us/training/)
- 🌐 [Find a Microsoft Training Services Partner](https://learn.microsoft.com/en-us/credentials/support/help#training-services-partners)

---

### 🛡️ Disclaimer
*This repository contains educational study notes, architecture summaries, and reference documentation compiled from publicly available official Microsoft Learn documentation. Microsoft, Azure, and Microsoft Entra are trademarks of the Microsoft group of companies.*

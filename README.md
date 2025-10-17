# Manual Testing Project – Demo E‑Commerce (PracticeSoftwareTesting)

A hands‑on **manual testing** project performed on the public demo site **Practice Software Testing**: <https://practicesoftwaretesting.com/>.  
This repository contains the complete tester workflow: **Test Plan → Test Cases → Execution → Defect Log → RTM → Test Summary**.

---

## 🎯 Objectives
- Practice end‑to‑end **manual testing** on a real web app
- Demonstrate **SDLC/STLC** understanding with complete artifacts
- Showcase **test design, execution, bug reporting, and traceability**

---

## 🧪 Application Under Test (AUT)
- **Site:** https://practicesoftwaretesting.com/
- **Modules covered:** Login, Register, Shop (Search, Product Detail), Cart, Checkout

> ⚠️ *This is a training/dummy site. Only use sample/dummy data.*

---

## 📦 Repository Structure
```
manual-testing-practice-ecommerce/
├─ README.md
├─ /docs
│  ├─ Test_Plan.md
│  └─ RTM.md
├─ /reports
│  └─ Test_Summary.md
├─ /evidence
│  └─ (screenshots: TC-*, BUG-*.png)
├─ Manual_Testing_Project_Template.xlsx   # Test Cases, Execution Log, Defect Log, RTM, Summary
└─ .gitignore
```

> The **Excel workbook** is the single source of truth for: **Test Cases**, **Execution Log**, **Defect Log**, **RTM**, and **Test Summary**.  
> Download it from this repo and update during your testing.

---

## 🔧 Test Environment & Tools
- **OS & Browsers:** Windows 10/11, Chrome, Firefox (latest)
- **Documentation:** MS Word/Google Docs (reports), **MS Excel** (provided)
- **Bug Tracking (optional):** JIRA/Bugzilla (replicated in Excel Defect Log)
- **Utilities:** Screenshot tool, basic **CLI/ADB** (optional, for device logs)

---

## 🧭 Scope
**In-Scope**
- Functional flows: Login, Search, Product Detail, Add to Cart, Cart, Checkout
- UI validations (text, labels, error messages, basic layout)
- Smoke, Functional, Regression, Sanity checks

**Out-of-Scope**
- Payment gateway integrations
- Performance/Security/Load testing
- Backend/database changes on live server

---

## 🧱 Process (STLC mapping)
1. **Requirement Analysis** → Identify flows in AUT
2. **Test Planning** → Define scope, risks, environments (see `/docs/Test_Plan.md` and Excel **Test Plan** sheet)
3. **Test Case Design** → Add Test Cases in Excel (**Test Cases** sheet)
4. **Test Execution** → Mark Pass/Fail, attach evidence (screenshots in `/evidence`)
5. **Defect Reporting** → Log bugs in Excel (**Defect Log** sheet) or JIRA
6. **Traceability** → Map REQs to TCs in Excel (**RTM** sheet)
7. **Closure** → Metrics in Excel (**Test Summary** sheet) + `/reports/Test_Summary.md`

---

## ✅ Smoke Test (quick health check)
Before deep testing, verify:
- Home page loads
- Login page opens
- Login works with valid user
- Search returns results
- Add 1 item to cart

If any fails → stop and log a **Smoke Failure** defect.

---

## 🔎 Test Scenarios (high level)
- **Login:** valid login, invalid email, wrong password, blank fields, logout
- **Search:** exact/partial name, no results, special chars
- **PDP:** image/price/name visible, add-to-cart works, quantity change
- **Cart:** add/remove item, price total updates, empty-cart message
- **Checkout:** address validation, payment option (COD/placeholder), order confirmation

---

## 📝 Sample Test Cases (from Excel)
| TC ID | Module | Title | Steps (summary) | Expected Result | Type | Priority |
|------|--------|-------|------------------|-----------------|------|----------|
| TC-LOGIN-001 | Login | Login with valid credentials | Enter valid email + password → Login | Redirect to dashboard/home | Functional | High |
| TC-LOGIN-005 | Login | Invalid password shows error | Enter valid email + wrong password → Login | Inline error “Invalid credentials” | Negative/Functional | High |
| TC-CART-003 | Cart | Add product to cart from PDP | Open PDP → Click **Add to Cart** | Cart count increments, success toast | Functional/Regression | High |

> Full list available in **Manual_Testing_Project_Template.xlsx → Test Cases**.

---

## 🐞 Defect Lifecycle (used in Excel / JIRA)
**New → Assigned → In‑Progress → Fixed → Retest → Closed (or Reopened)**

**Defect template (Excel/JIRA fields):**
- *Title, Severity, Priority, Environment, Build, Steps to Reproduce, Expected vs Actual, Attachments, Status*

---

## 🔁 Testing Types Used
- **Smoke**: quick readiness check
- **Functional**: feature‑level validations
- **Sanity**: targeted recheck after a small fix
- **Regression**: re‑execute impacted areas after fixes/updates

---

## 📊 Metrics (from Excel “Test Summary”)
- Total/Executed/Passed/Failed/Blocked test cases
- Pass % and Fail %
- Defects by Severity (Critical/High/Medium/Low)

> Update values by executing test cases and logging defects in the Excel workbook.

---

## ▶️ How to Run This Project (as a learner)
1. Open the site **https://practicesoftwaretesting.com/**
2. Download and open **Manual_Testing_Project_Template.xlsx**
3. In **Test Cases**, start with Login (TC-LOGIN-001 to 005)
4. Execute in Chrome/Firefox → mark **Pass/Fail**, add **Actual Result**
5. Take screenshots for failures → save into `/evidence`
6. Log defects in **Defect Log** (use severity/priority)
7. Maintain **RTM** mapping and **Test Summary** metrics
8. Export `/reports/Test_Summary.md` with your final numbers

---

## 🧾 Resume Bullets (you can reuse)
- Performed end‑to‑end **manual testing** on a demo e‑commerce app covering Login, Search, Cart, and Checkout.
- Designed **25+ test cases**, executed them across Chrome/Firefox, and documented results with evidence.
- Logged defects with **severity/priority** and maintained **RTM** for complete coverage.
- Prepared a **Test Summary report** with execution metrics and defect analysis.

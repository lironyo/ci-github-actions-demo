#  **ci-github-actions-demo**

This repository contains **4 separate GitHub Actions workflows**, explicitly designed to address each task of the assignment with a unique, dedicated file.

---

## 💻 **Workflow Files Implemented**

### 1️⃣ **Basic CI Check** (`ci.yml`)

This workflow confirms the most fundamental CI trigger and logging capability.

* **Goal:** Execute the simplest CI step.
* **Trigger:** Code **Push** to the `main` branch.
* **Action:** Runs a shell command that prints: **`Hello, CI with GitHub Actions!`**

---

### 2️⃣ **Single-Version Testing** (`pytest.yml`)

This workflow is dedicated to the core requirement of **running tests on a single, specified Python version**.

* **Goal:** Verify basic test functionality.
* **Trigger:** Code **Push** to the `main` branch.
* **Actions:** Sets up **Python 3.9** and runs the **Unit Tests** (`test_main.py`).

---

### 3️⃣ **Cron Scheduling** (`cron.yml`)

This workflow demonstrates time-based automation, separate from code events.

* **Goal:** Set up a routine, time-based job.
* **Trigger:** **Cron Schedule** (`0 0 * * *`).
* **Schedule:** Runs daily at **midnight UTC** 🌃.
* **Action:** Prints the message: **`Scheduled build completed successfully!`**

---

### 4️⃣ **Dedicated Matrix Builds with separated version and OS** (`matrix_python_v.yml`)

This workflow focuses on the advanced aspect of running tests across multiple versions.

* **Goal:** Demonstrate the advanced matrix strategy.
* **Trigger:** Code **Push** to the `main` branch.
* **Key Feature:** Uses a **Matrix Build** 🧩 to execute the unit tests (`test_main.py`) simultaneously against **Python versions 3.7 3.8, 3.9, 3.10**.
* 3.7 run and test separately on Windows

---
### 4️⃣ **Dedicated Matrix Builds** (`matrix_python_version.yml`)

This workflow focuses on the advanced aspect of running tests across multiple versions.

* **Goal:** Demonstrate the advanced matrix strategy.
* **Trigger:** Code **Push** to the `main` branch.
* **Key Feature:** Uses a **Matrix Build** 🧩 to execute the unit tests (`test_main.py`) simultaneously against **Python versions 3.8, 3.9, 3.10**.
---

## 📁 **Project Structure**

* **`main.py`** 🐍: Contains the simple Python function for testing.
* **`test_main.py`** ✅: Unit tests using the `unittest` framework.
* **`.github/workflows/`** ⚙️: Contains the four separate workflow files.

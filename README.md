# Quantum-Lumberjack-Quantum-Graph-Surgery
Automated quantum circuit optimizer and T-gate reducer for the Google Verifiable Quantum Circuit Compilation challenge on Kaggle. Uses Qiskit DAG and N-gram commutation logic
# 🪶 Quantum Graph Surgery: Compiling with N-Grams

An automated quantum circuit optimizer and T-gate reducer designed for the **Google Quantum AI - Verifiable Quantum Circuit Compilation** challenge on Kaggle.

[English Version](#english) | [Русская версия](#russian)

---

<a name="english"></a>
## 🇬🇧 English Version

### 💡 Core Idea
The main goal of this tool is to optimize complex quantum circuits by treating the sequence of gates as a multi-dimensional text. Instead of using standard string searching, this optimizer converts flat OpenQASM code into a **Directed Acyclic Graph (DAG)** using Qiskit. 

By analyzing the DAG, the tool performs **"Graph Surgery"** by identifying specific \(n\)-gram patterns (such as \([T][T]\) or \([T][T^\dagger]\)) along independent qubit wires, bypassing parallel execution noise.

### 🚀 Key Features
* **Phase Barrier Breaking:** Automatically commutes (pushes) expensive \(T\)-gates forward through `CX` (CNOT) control lines.
* **\(N\)-Gram Phase-Folding:** Fuses adjacent \(T\)-gates into cheaper \(S\)-gates or completely annihilates \(T\)/\(T^\dagger\) pairs.
* **Qiskit 1.x Compatible:** Fully updated to support the latest Qiskit 1.0+ internal graph structures (`DAGOpNode`).

### 🛠️ Installation & Usage
Ensure you have the required libraries installed:
```bash
pip install qiskit matplotlib pydot graphviz
```

Run the pipeline python script to see the automated optimization in action:
```python
# Run your full_pipeline_optimizer script here
```

---

<a name="russian"></a>
## 🇷🇺 Русская версия

### 💡 Главная идея
Основная цель этого инструмента — автоматическая оптимизация сложных квантовых схем. Мы относимся к последовательности квантовых вентилей как к многомерному тексту. Вместо поверхностного поиска по строкам, оптимизатор переводит плоский код OpenQASM в **Направленный ациклический граф (DAG)** с помощью Qiskit.

Анализируя граф, инструмент проводит **«хирургию графов»**: выявляет избыточные $$n$$-граммы (такие как цепочки SS[T][T]$$ или $$T][T^\dagger])$$ вдоль изолированных линий кубитов, полностью игнорируя текстовый «шум» параллельно выполняющихся операций.

### 🚀 Ключевые возможности
* **Разрушение фазовых барьеров:** Автоматически протаскивает (коммутирует) дорогие $$T$$-гейты вперед через ведущие (Control) линии вентилей `CX` (CNOT).
* **Схлопывание фаз через N-граммы:** Объединяет два идущих подряд T-гейта в один дешевый S-гейт или полностью аннулирует пары взаимообратных гейтов T/$$T^\dagger$$.
* **Поддержка Qiskit 1.x:** Код полностью адаптирован под новые внутренние структуры графов Qiskit 1.0+ (`DAGOpNode`).

### 🛠️ Установка и запуск
Убедитесь, что у вас установлены необходимые библиотеки:
```bash
pip install qiskit matplotlib pydot graphviz
```

Запустите готовый скрипт оптимизатора, чтобы увидеть сквозной цикл перестановки и сжатия цепи:
```python
# Запустите ваш скрипт full_pipeline_optimizer здесь
```

---

### 🏷️ GitHub Topics
`kaggle` | `google-quantum-ai` | `quantum-computing` | `quantum-compiler` | `kickmix` | `openqasm` | `qiskit` | `circuit-optimization`

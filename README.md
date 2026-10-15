# LLM Layer 1-3: Guardrails Implementation

This repository demonstrates the three fundamental layers of LLM security (Input, Runtime, and Output validation) using DeepSeek V4 and Yandex Cloud API. Each layer is implemented as a separate, isolated code block.

## 🛡️ The Three Layers of Defense

### Layer 1: Pre-processing (Input Validation)
*   **Goal:** Filter malicious data before it reaches the LLM.
*   **Tools:** Delimiters (XML tags), ML Classifiers (Naive Bayes), PII Detectors (RegEx).
*   **Status:** Blocks direct Prompt Injection and data leakage at the entry point.

### Layer 2: Intra-processing (Runtime Guardrails)
*   **Goal:** Control the model's actions during generation.
*   **Tools:** Tool Call Interception (Middleware), Argument Validation (Price/Logic checks).
*   **Status:** Prevents unauthorized `tool_calls` (e.g., blocking expensive or restricted operations).

### Layer 3: Post-processing (Output Validation)
*   **Goal:** Sanitize the model's response before showing it to the user.
*   **Tools:** Toxicity Checkers, PII Detectors (Output), Factuality Check (NLI).
*   **Status:** Prevents reputational damage and accidental data leaks in the final text.

## 💻 Tech Stack
*   **API:** Yandex Cloud (OpenAI-compatible)
*   **Model:** DeepSeek V4 Flash
*   **Env:** Google Colab
*   **Libs:** `openai`, `re`, `json`, `sklearn`

## 📜 License
MIT

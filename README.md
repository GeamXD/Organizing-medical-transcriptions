# Medical Information Extraction with Gemini

This guide outlines how to use the Gemini model for Named Entity Recognition (NER) and data extraction from medical texts.

## Overview

Leverage Gemini's capabilities to identify and extract key entities (e.g., diseases, treatments, medications) and structured information from unstructured medical notes, research papers, or clinical reports.

## Getting Started

1.  **Obtain a Gemini API Key:**
    * Sign up for Google AI Studio or Google Cloud (if using Vertex AI).
    * Generate your API key from the respective platform.

2.  **Save Your API Key Securely:**
    Create a `.env` file in your project's root directory and add your API key:

    ```
    GEMINI_API_KEY="your_api_key_here"
    ```

## Usage

Utilize the Gemini API to send prompts that guide the model to perform NER and extract specific data.

**Example Prompting Strategy:**

```
"Extract the patient's age, medical specialty, primary treatment, and ICD-10 code from the following medical note: [Your Medical Text Here].
Format the output as a JSON object with keys: 'age', 'medical_speciality', 'treatment', 'icd_code'."
```

**Key Considerations for Prompting:**

* **Clear Instructions:** Explicitly state what you want to extract.
* **Desired Format:** Specify the output format (e.g., JSON, list, table).
* **Context:** Provide sufficient context from the medical text.
* **Few-shot Examples (Optional but Recommended):** For complex or domain-specific extractions, include 1-2 examples of input text and desired output to guide the model.

---

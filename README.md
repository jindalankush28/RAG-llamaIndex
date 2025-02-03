# Parsing EMRO Hypertension Guidelines with LlamaIndex

## Overview
This project utilizes LlamaIndex to extract and structure data from the **EMRO Technical Publications Series 29: Clinical Guidelines for the Management of Hypertension**, published by the **World Health Organization**. The extracted information includes textual content, structured tables, and key medical guidelines, making it easier for researchers and healthcare professionals to analyze hypertension management strategies.

## Methodology
### 1. **Data Ingestion**
- The source document is loaded and parsed using **LlamaIndex**, which enables efficient indexing of large unstructured medical texts.
- The text extraction process ensures that key sections such as **clinical guidelines, pathophysiology, and treatment protocols** are captured.
- Original data: `dsa234.pdf`

### 2. **Text Processing & Parsing**
- The LlamaIndex pipeline extracts sections from the document while preserving structure and meaning.
- **Markdown formatting** is used to enhance readability, maintaining headings, bullet points, and key insights.
- **Tables** are identified and extracted separately to retain their structured information.

### 3. **Table Parsing**
LlamaIndex API effectively captures and structures tabular data, ensuring readability and accessibility. An example is the extracted **Table 7**, which presents details of antihypertensive drug preparations, their mechanisms of action, and dosage information:

#### **Table 7: Preparations, Mechanism of Action, and Main Features of Antihypertensive Drugs**

| Drug         | Doses (mg/day) | Mechanism of Action                                      |
|-------------|--------------|------------------------------------------------------|
| Acebutolol  | 200–1200     | β-adrenergic receptor antagonists                    |
| Labetalol   | 200–800      | Non-cardioselective                                 |
| Propranolol | 20–240       | Cardioselective                                    |
| Metoprolol  | 50–200       | Direct vasodilators                                |
| Carvedilol  | 3.75–25      | Nondihydropyridines                               |
| Hydralazine | 1–2          | Calcium antagonists                               |
| Diltiazem   | 90–360       | Combined                                          |
| Nifedipine  | 30–120       | Direct relaxation of smooth muscle cells         |
| Amlodipine  | 2.5–10       | Block entry of calcium into smooth muscle cells  |
| Felodipine  | 5–20         | Fall in BP results mainly from a decrease in vascular resistance. |

### 4. **Indexing & Retrieval**
- The processed data is stored in an **LlamaIndex vector database** for efficient retrieval.
- Users can query the indexed data for **specific drug details, treatment recommendations, and pathophysiology insights**.

### 5. **Load Llama 2 7b model**
- Llama 2 is loaded from HuggingFace for generating responses of user queries.
- GPU T4 is leveraged. Given compute restrictions model is loaded in 4 bit Quantization

Final Parsed Outputs: `outputs.md`

## Key Features
- **Automated Parsing**: Extracts and structures large-scale medical text efficiently.
- **Table Retention**: Maintains structured tabular information in a user-friendly format.
- **Efficient Search & Retrieval**: Allows querying of extracted content for rapid access to relevant information.
- **Markdown Formatting**: Enhances readability and preserves document structure.


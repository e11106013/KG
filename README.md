# 系統模組與套件說明


## 📥 資料收集與清洗模組

### `1_html2json_v2.ipynb`

- **BeautifulSoup（bs4）**：負責解析 HTML 結構，提供節點搜尋與屬性操作等功能。
- **re**：使用正則表達式清理不必要的空白與特殊符號。
- **json**：將轉換後的資料儲存為標準 JSON 格式。
- **os**：處理路徑與檔案讀取操作。

### `1_pdf2json_v2.ipynb`

- **pdfplumber**：從 PDF 抽取文字內容、位置與版面資訊，適合處理結構化或表格型 PDF。
- **re**：同上。
- **json**：同上。
- **os**：同上。

### `2_get_metadata_v4.ipynb`

- **json**：處理 JSON 檔案的讀取與解析。
- **pandas**：將處理後的資料轉為 DataFrame，並可儲存為 CSV。
- **os**：處理檔案與目錄操作。
- **re**：透過正則表達式處理與格式化欄位內容。

---

## 🧠 文本語意分析模組

### `3_cot_NER_llama_v3.ipynb`

- **langchain_openai**：支援 OpenAI 模型（如 llama-3.3-70b-versatile）。
- **langchain**：用於建立 PromptTemplate 與 LLMChain。
- 提供命名實體辨識（NER）與關係識別功能。
- **re**：清理 JSON 輸出中的 Markdown 標記。
- **json**：處理 JSON 資料解析與序列化。
- **os**：處理環境變數與檔案操作。
- **shutil**：檔案搬移用途。

### `3_resolution_NER_llama_v8.ipynb`

- 同上，並額外提供 **廣義指稱解決（GCR）** 功能。

---

## ✅ 審閱與修訂模組

### `4_1_human_review_v7.ipynb`

- **os**：列出資料夾中的檔案與組合路徑。
- **json**：讀取 JSON 檔案並處理字典轉換。
- **csv**：將資料寫入 CSV。
- **shutil**：移動已處理檔案至 done/ 資料夾。

### `4_3_review_report_v3.ipynb`

- **pandas**：處理與分析 CSV 結構化資料。
- **tabulate**：格式化並輸出表格數據至終端機。

---

## 🔗 實體連結模組

### `5_wiki1_v5.ipynb`

- **wikipedia / requests**：查詢實體描述與可能對應條目。
- **sparqlwrapper**：執行 SPARQL 查詢並與 RDF 平台互動。

---

## 📄 知識圖譜管理模組

### `6_RDF_event_v6.ipynb`

- **os**：處理檔案與目錄操作。
- **json**：解析 JSON 格式資料。
- **requests**：從 Wikidata 或 DBpedia 擷取資料。
- **rdflib**：
  - `Graph`, `URIRef`, `Literal`, `RDF`, `Namespace`, `BNode`
  - 命名空間：`XSD`, `RDFS`, `OWL`

### `6_RDF_meta_v1.ipynb`

- 同上。

---

## 💬 KG 應用程式

### `7_SPARQL_QA_JSON.ipynb`
### `7_sparql_nli_v2.ipynb`

- [![影片標題](https://img.youtube.com/vi/JOf4mG4b7aY/0.jpg)](https://www.youtube.com/watch?v=JOf4mG4b7aY)

- **requests**：支援 HTTP 請求（GET / POST）。
- **string.Template**：建立模板字串並以變數格式化內容。

<div align="center">
  <img src="./icon.svg" width="84" height="84" alt="XJY Editor Logo" />
  <h1>XJY Editor</h1>
  <p><strong>100% Local-First Browser &amp; Offline Editor for XML, JSON, YAML, CSV, SQLite &amp; Excel</strong></p>
  <p><strong>在浏览器与离线单文件中编辑 XML、JSON、YAML、CSV、SQLite 与 Excel（零上传 · 保编码 · 分色表格）</strong></p>
  <p>
    <a href="https://xjyeditor.com/zh/">🇨🇳 中文官网</a> ·
    <a href="https://xjyeditor.com/en/">🌐 English Website</a> ·
    <a href="https://xjyeditor.com/app/">🚀 Launch Web App (在线使用)</a> ·
    <a href="https://xjyeditor.com/app/cleaner">✦ Data Cleaner (数据清洗)</a> ·
    <a href="https://xjyeditor.com/en/pricing/">⚡ Pro &amp; REST API</a> ·
    <a href="https://www.youtube.com/watch?v=7H1ex_RlGgA">▶ 60s Demo Video</a> ·
    <a href="https://xjyeditor.com/zh/windows/">🪟 Windows Right-Click Helper (右键助手)</a> ·
    <a href="https://findchanged.com">🔍 FindChanged Diff</a>
  </p>
</div>

<p align="center">
  <img src="./og-card.png" width="860" alt="XJY Editor Preview" />
</p>

<div align="center">
  <h3>▶ 60-Second Video Demo: Visual Data Cleaner &amp; Pro REST API</h3>
  <a href="https://www.youtube.com/watch?v=7H1ex_RlGgA">
    <img src="https://img.youtube.com/vi/7H1ex_RlGgA/hqdefault.jpg" width="600" alt="Watch XJY Editor Data Cleaner 60s Demo on YouTube" />
  </a>
  <p><em>Click to watch on YouTube: clean messy CSV/Excel/JSON locally, compare diffs in FindChanged.com, detect statistical outliers (Z-score/IQR/MAD) &amp; export cURL API calls.</em></p>
</div>

---

## 🇨🇳 中文介绍 (Chinese)

**XJY Editor**（[https://xjyeditor.com](https://xjyeditor.com)）是一套完全在本地浏览器中运行的结构化文档与数据表格编辑器。无任何后端文件上传、无账号注册、无追踪脚本；同时提供**双击即用的单文件离线 HTML 版**（可直接拷入隔离内网使用）和 **Windows 资源管理器右键菜单助手**（支持 `Ctrl+S` 直接写回原文件并保留 GBK / UTF-16 编码与 CRLF 换行符）。

### ✨ 五大工作台与核心亮点

| 工作台 | 支持格式 | 在线入口 | 离线单文件（本仓库直接下载） | 核心解决痛点 |
| :--- | :--- | :--- | :--- | :--- |
| **1. 结构化文档编辑器** | `.xml` / `.kml` / `.json` / `.yaml` / `.yml` | [打开编辑器 ↗](https://xjyeditor.com/app/) | [`XJYEditor.html`](./XJYEditor.html) | 左侧目录树 + 中间**数据类型分色表格** + 源码双向实时定位；保留 JSON 64 位大整数精度与 YAML 1.2 注释/锚点；支持 XML 同级重复节点检查、坏文件源码修复与 36 条批量辅助编辑规则 |
| **2. CSV / TSV 编辑器** | `.csv` / `.tsv` / `.txt` | [打开 CSV ↗](https://xjyeditor.com/app/csv) | [`CSVEditor.html`](./CSVEditor.html) | 所有字段按原文本保护，**绝不吞掉 `00123` 前导零、不把 18 位长编号转成科学计数法**；同时按语义分色显示文本、数值、日期与布尔值；未改动行按原始字节写回 |
| **3. SQLite 编辑器** | `.sqlite` / `.sqlite3` / `.db` / `.db3` | [打开 SQLite ↗](https://xjyeditor.com/app/sqlite) | [`SQLiteEditor.html`](./SQLiteEditor.html) | 内置 WebAssembly SQLite 引擎，免装客户端直接按类型读写 `INTEGER`（64 位安全）、`REAL`、`TEXT`、`NULL`、`BLOB`；支持**多条件筛选排序、SQL 查询与执行、导入 CSV 建表/追加、新建/修改/删除表结构与索引**，全库原子事务与一步撤销 |
| **4. Excel 编辑器** | `.xlsx`（在位编辑）/ `.xls`（只读预览） | [打开 Excel ↗](https://xjyeditor.com/app/excel) | [`ExcelEditor.html`](./ExcelEditor.html) | **外科手术式在位修改**：只更新你改动过的单元格，原工作簿中的样式、图表、公式与其他工作表原封不动 |
| **5. 数据清洗工作台** | `.csv` / `.xlsx` / `.json` | [打开数据清洗 ↗](https://xjyeditor.com/app/cleaner) | [`DataCleaner.html`](./DataCleaner.html) | 可视化串联去重、空值填充、Excel 合并单元格向下填充（Fill Down）、清除不可见字符、全角转半角、JSON 嵌套拍平；清洗后一键跳转 [FindChanged.com](https://findchanged.com/zh/) 对比前后差异；支持导出可复用 Pipeline JSON 并接入 [Pro 云端 REST API](https://xjyeditor.com/zh/pricing/)（统计异常值、类型不符检测、值范围校验、PII 脱敏） |

### 🎨 为什么选择 XJY Editor？

1. **数据类型自动分色 + 琥珀金自动索引列（`#`）**
   - 四个编辑器统一采用「显式语法/存储类型优先 + 文本语义推断」双层着色方案：
   - 自动索引列（`#`）采用暖琥珀金标出；**文本**（淡蓝，含前导零编码 `00108`）、**数值**（薄荷绿）、**布尔**（暖橙）、**ISO 日期**（青碧）、**空值 `null`**（淡紫斜体）与**复合节点/公式**（淡靛紫）一目了然，一眼排查出“数字被误存为字符串”等配置问题。
2. **保存绝不改动你没动过的东西**
   - 自动识别并保留原文件的字符编码（**UTF-8、UTF-8 BOM、UTF-16LE/BE、GBK / GB18030**）与换行符（**CRLF / LF**）。
3. **36 条批量辅助编辑规则**
   - 在同一列连续对 3 个单元格做相似修改（如加前缀、改后缀、按规律编号），自动推断规则并预览整列剩余记录的修改结果，一次确认即可完成，支持单步撤销。
4. **跨格式转换与子树对比**
   - **转换并导出**：XML / JSON / YAML 互转；CSV / Excel / SQLite 当前表导出为 CSV、TSV 或文本型 XLSX（不丢前导零）。
   - **子树差异比对**：勾选两个同级节点一键发送至 [FindChanged](https://findchanged.com/zh/) 比较差异，点击差异直接跳回原节点。

### 🪟 Windows 资源管理器右键菜单助手（`XJYEditorHelper.exe`）

安装轻量级助手后，在 Windows 资源管理器中右键任意支持的文件选择 **「用 XJY Editor 打开」**，即可在浏览器中直接编辑，按 `Ctrl+S` 直接写回原磁盘文件（无需管理员权限，不篡改系统默认文件关联）。

- **下载页面**：[https://xjyeditor.com/zh/windows/](https://xjyeditor.com/zh/windows/)（或直接下载本仓库中的 [`XJYEditorHelper.exe`](./XJYEditorHelper.exe)）
- **当前版本**：`0.4.1`（大小：`6.7 MB`）
- **SHA-256**：`13fa1dfebeb5e04c08c706a7c7b92a070841dff2932ab2abccf48c5ff4aae296`

---

## 🌐 English Overview

**XJY Editor** ([https://xjyeditor.com/en/](https://xjyeditor.com/en/)) is a local-first browser and offline toolkit for editing **XML (including KML), JSON, YAML 1.2, CSV/TSV, SQLite (`.sqlite / .db`) and Excel (`.xlsx / .xls`)** files. Every operation runs 100% locally in your browser — files are never uploaded to any server.

### Key Highlights

- **Tree + Color-Coded Smart Table + Bidirectional Source Sync**: Browse nested XML, JSON and YAML with a left structure tree and a middle smart table where cells are automatically tinted by data type (**String**, **Number**, **Boolean**, **ISO Date**, **Null/Empty**, **Complex**) alongside a warm amber-gold automatic index column (`#`).
- **Zero Silent Data Corruption**:
  - **JSON**: Keeps exact lexical number literals (64-bit integers and exponents are never rounded by JavaScript floats).
  - **YAML 1.2**: AST-based editing preserves inline comments, block scalars and anchors/aliases.
  - **CSV / TSV**: Every field is preserved as exact text — leading zeros like `00123` and 18-digit IDs are never stripped or converted to `1.23E+17`. Unchanged rows are written back byte for byte.
  - **SQLite**: In-browser WebAssembly SQLite engine with 64-bit integer safety, multi-condition filtering & sorting, SQL query/execution tab, CSV import, visual table/index schema editing, atomic transactions, foreign keys and triggers.
  - **Excel (`.xlsx`)**: Surgical in-place cell updates that leave existing styles, charts, formulas and untouched sheets intact.
- **Preserves Original Encoding & Line Endings**: Supports UTF-8, UTF-8 with BOM, UTF-16LE/BE and GBK/GB18030 with CRLF/LF preservation.
- **Visual Data Cleaner & REST API**: Build reusable cleaning pipelines for CSV, Excel (`.xlsx`) and JSON (deduplication, Fill Down for merged cells, invisible character cleanup, JSON flattening) locally in [`DataCleaner.html`](./DataCleaner.html) or [online](https://xjyeditor.com/app/cleaner), inspect before/after diffs in [FindChanged.com](https://findchanged.com/en/), or upgrade to [Pro & REST API](https://xjyeditor.com/en/pricing/) for statistical outlier detection (Z-score / IQR / MAD), data type mismatch quarantine, value range validation, PII masking and large-file programmatic execution.
- **Single-File Offline HTML Builds**: Download [`XJYEditor.html`](./XJYEditor.html), [`CSVEditor.html`](./CSVEditor.html), [`SQLiteEditor.html`](./SQLiteEditor.html), [`ExcelEditor.html`](./ExcelEditor.html), [`DataCleaner.html`](./DataCleaner.html) and [`XJYHelp.html`](./XJYHelp.html) directly from this repository to use on air-gapped or intranet machines without internet access.
- **Windows Right-Click Helper**: Right-click any supported file in Windows File Explorer to open it and press `Ctrl+S` to save straight back to disk ([Download details](https://xjyeditor.com/en/windows/)).

---

## 💬 Feedback & Issues (问题反馈与建议)

If you encounter a file edge case, bug, or have a feature request, feel free to open an [Issue](../../issues) or email `contact@xjyeditor.com`.

# VBA to Python Prompt Templates

💡 ChatGPTを使って、Excel VBA マクロを Python に変換するためのプロンプトテンプレート集です。

このリポジトリでは、よくあるVBAマクロ処理（セル操作、ループ、条件分岐、シート操作など）を  
Python（openpyxl / pandas）で実現するための ChatGPT 向けプロンプトを収録しています。

---

## 📌 What is this?
This repository provides prompt templates for converting Excel VBA macros to Python using ChatGPT.  
It helps automate spreadsheet tasks with openpyxl or pandas, and is ideal for both engineers and business users.

---

## 🚀 Features

- 🔁 VBAマクロ → Python変換の実用テンプレート
- 🧠 ChatGPTに貼るだけでOKなフォーマット
- 📄 業務フローを意識したサンプル集
- 💬 今後の自動変換ツール・SaaS展開を見据えた基礎素材

### 🔸 VBAマクロコード（例）
```vba
# "Sheet1" を選択して名前を変更
# Select "Sheet1" and rename it
Sheets("Sheet1").Select
ActiveSheet.Name = "処理済"
Sheets.Add.Name = "新規シート"
Sheets("Sheet2").Delete
```
### 🔸 Pythonコード（ChatGPT変換後）
```python
from openpyxl import load_workbook

wb = load_workbook("sample.xlsx")

# 「Sheet1」を選択して名前を変更
# Select "Sheet1" and rename it
ws = wb["Sheet1"]
ws.title = "処理済"

# 新しいシートを追加（最後尾に追加される）
new_sheet = wb.create_sheet(title="新規シート")

# 指定シートを削除
del wb["Sheet2"]

wb.save("sample.xlsx")
```

---

## 🛠 Use Case / 使い方

1. 変換したいVBAコードをコピー  
2. 本リポジトリのテンプレートに貼り付ける  
3. ChatGPTでプロンプトを実行 → Pythonコードが生成される！

---

## 📚 テンプレート例（例として一部抜粋）

- [セルに値を代入する](./01_セル操作の変換.md)
- [ForループとIf条件](./02_ループと条件分岐.md)
- [シートを操作する](./03_シート操作の変換.md)

---

## 🙌 ご意見・コラボ歓迎！

テンプレート追加提案や改善リクエストはお気軽に [Issue](https://github.com/mnrj-vv-w/vba-to-python-prompts/issues) へどうぞ。  
「自動変換Webツール版」の開発にも興味がある方は、ぜひご連絡ください！

---

## 🏷 推奨 GitHub Topics


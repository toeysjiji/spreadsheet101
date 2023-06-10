# Spreadsheet101
This is a brief instruction on how to utilize a basic spreadsheet.


- HyperLink - Crtl+K

## Data Entry

- Drag and Drop - กรอกเองแล้วลากที่ขอบ cell ขวาล่าง
- ={input1, input2, input3, input4, input5} → input จะถูกใส่ใน cell ตามแนวนอน (row)
- ={input1; input2; input3; input4; input5} → input จะถูกใส่ใน cell ตามแนวตั้ง (column)
- Matrix → ใช้ , และ ; ค่อยๆใส่ข้อมูลไปทีละ cell
- =SEQUENCE(row, [columns], [start], [step])

## ArrayFormula

- Ctrl + Shift + Enter
- เลือก cell ต้องเลือกหลายๆ row → E4:E28, F3:F39, G1:G31
- ex.=ArrayFormula(TO_DOLLARS(E4:E28)) , =ArrayFormula(F4:F28*120%)
- ไม่ต้อง lock cell (F4)
- =UPPER() → ให้เป็นตัวใหญ่ทั้งหมด
- =LOWER() → ให้เป็นตัวเล็กทั้งหมด
- ใช้ & ในการเชื่อมข้อมูลใน cell =Tony & “ “ & Patt
- =LEFT(string, [number of characters]) → เลือกตัวหนังสือตัวซ้ายสุดตามจำนวนที่ระบุ

## Import Data

- CSV → =importdata()
- HTML → =importhtml()
- XML → =importxml(url, xpath_query)
- FEED → =importfeed()

## Explore

- ALT + Shift + X

## Filter & Sorting

- =FILTER(range, condition1, [condition2],…) → range เลือกเฉพาะข้อมูลไม่ต้องเลือก header
- =FILTER(EMPLOYEE, (SALARY>100000) * (GENDER="M"))
- `*` = AND
- =FILTER(EMPLOYEE, (SALARY>100000) + (GENDER="M"))
- `+` = OR
- =SORT(range, sort_column, is_ascending)

## Conditions

- =IF(logical_expression, value_if_true, value_if_false)
- =IFS(condition1, value1, [condition2, …], [value2, …])
- =AND(logical_expression1, [logical_expression2, …]) → ใส่กี่เงื่อนไขก็ได้
- =OR(logical_expression1, [logical_expression2, …]) → ใส่กี่เงื่อนไขก็ได้
- =NOT(logical_expression)

## Conditional Formatting

- เลือก range cell ที่สนใจ → Format → conditional formatting
- single color → ใส่เงื่อนไขทีละเงื่อนไข
- single color สามารถ เขียนสูตรข้าม column → Custom formula is
- scale color → ไล่ลำดับ

## Vlookup

- =VLOOKUP(search_key, range, index, [is_sorted])
- [is_sorted] → FALSE = exact match

## TrimWhiteSpace

- ครอบ cell ที่สนใจ → Data → Data Cleanup → Trim whitespace
- =TRIM(string)

## Working with Text

- =LEN()
- =LOWER()
- =UPPER()
- =LEFT()
- =RIGHT()
- =MID()
- =TEXTJOIN()
- =SPLIT(text, delimiter, [split_by_each], [remove_empty_text])
- =PROPER()

## Regular Expression

- `^A` → อะไรก็ได้เริ่มต้นด้วย A
- `s$` → อะไรก็ได้จบด้วย s
- `c.t` → อะไรก็ได้ที่ขึ้นด้วย c จบด้วย t
- `[ABC]` → match A B or C
- `[A-Z]` → match all capital letters
- `[A-z]` → match all letters
- `[a-z]` → match all lowercase letters
- `[0-9]` or \d → match digits

## Regular Expression Quantifiers

- `*` → match zero or more
- `+` → match one or more
- `?` → match zero or one
- `{5}` → match exactly 5 characters
- `{3, 5}` → match min 3, max 5 characters

## Sparkline / Google finance

- =SPARKLINE(data, [options])
- =GOOGLEFINANCE(ticker, [attribute], [start_date], [end_date|num_days], [interval])

## Google Translate

- =GOOGLETRANSLATE(text, [source_language], [target_language])

## Image

- =IMAGE(url, [mode], [height], [width])

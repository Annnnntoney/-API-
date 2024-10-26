# -API-
口罩實名制在疫情期間開始實施，為了避免像之前那樣出現排隊搶購的情況，健保署規劃提供即時的口罩庫存資訊給民眾參考，此口罩地圖 API 網址合併了多種開放資料，
包含著特約藥局、診所相關資訊，以及健保署提供的口罩剩餘數量明細，讓我們利用前面所學的程式串接該API，來試著完成下列的實作。

➟ 口罩地圖 API 網址：https://raw.githubusercontent.com/kiang/pharmacies/master/json/points.json

1. 首先試著直接用瀏覽器打開網址，請解釋這個 API 中有哪些資料？這樣資料會想到什麼樣的應用呢？

（Hint：瀏覽器預設打開會是純文字格式，若你使用 Google Chrome 可以安裝 JSONView 擴充工具美化內容）


(在這裡回答)

2. 請建立一個 Github Repo 與 Colab 綁定（名稱自訂），並且根據以下範例完成第一步驟的資料收集後 Commit 第一個版本：

import requests
import json


# 利用 requests 對 API 來源發送一個請求
'''
Your Code
'''

# 將請求回應的內容存成一個字串格式
'''
Your Code
'''

# 將長得像 json 格式的字串解析成字典或列表
'''
Your Code
'''

print(data)
3. 接下來，請你將取回來的資料利用 Python 語法計算各地區的藥局數量，完成後 Commit 成第二個版本：

med_count = {}

# 填入欄位名稱
for d in data['_____']:
    conunty = d['_____']['_____']
    if conunty not in med_count:
         med_count[conunty] = 0
    '''
    Your Code
    '''

print(med_count)
# {'台北市': 123, '新北市': 456 ...}
4. 接下來請你計算出每個地區的成人剩餘口罩數量，並且將結果從大到小排列，完成後 Commit 第三個版本：

mask_count = {}

# 填入欄位名稱
for d in data['_____']:
    conunty = d['_____']['_____']
    '''
    Your Code
    '''

# 將結果從大到小排列
med_count = dict(sorted('''Your Code''', key=lambda item: item[1]))

print(mask_count)
# {'台北市': 12345, '新北市': 45678 ...}
---

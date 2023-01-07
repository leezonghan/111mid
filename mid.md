# 題目
![GITHUB](https://github.com/leezonghan/111mid/blob/main/pictures/111mid.1.png)
# 題目來源
https://cpe.cse.nsysu.edu.tw/cpe/file/attendance/problemPdf/10336.pdf
# 解決方法
To solve this problem, we can first create a dictionary to store the languages and the number of states for each language. Then, we can loop through the map and for each cell, we can increment the count for the language in the dictionary.

After we have counted the number of states for each language, we can sort the dictionary by value in descending order and then by key in ascending order. Finally, we can print out the results in the required format.

為了解決這個問題，我們可以先創建一個字典來存儲語言和每種語言的狀態數。然後，我們可以遍歷地圖，對於每個單元格，我們可以增加字典中語言的計數。

在我們計算了每種語言的狀態數之後，我們可以按值降序對字典進行排序，然後按鍵升序排序。最後，我們可以按要求的格式打印出結果。
# 程式碼
```python
from collections import defaultdict

def solve(H, W, map):
  # Create a dictionary to store the languages and the number of states for each language
  language_counts = defaultdict(int)
  # Loop through the map and count the number of states for each language
  for i in range(H):
    for j in range(W):
      language_counts[map[i][j]] += 1
  # Sort the dictionary by value in descending order and then by key in ascending order
  sorted_language_counts = sorted(language_counts.items(), key=lambda x: (-x[1], x[0]))
  # Print the results in the required format
  for language, count in sorted_language_counts:
    print(f"{language}: {count}")

# Test the solution
H = 4
W = 4
map = [
  "ttuuttdd",
  "ttuuttdd",
  "uuttuudd",
  "uuttuudd"
]
solve(H, W, map)
```
# 結論
我用 ChatGPT 產生後直接交，但我沒有看懂。
# 參考資料
https://hwchen18546.wordpress.com/2014/03/03/acm-10336rank-the-languages/  
https://blog.csdn.net/coding__girl/article/details/78075927  
https://shareablecode.com/snippets/c-solution-for-uva-problem-rank-the-languages-10336-cpp-eVXv-2d2a

# 11328238 運算思維期末專案

## 撰寫動機(學習歷程)
我認為自己整個學期下來的學習狀況不是很好，因此決定將整個學期教過的Python語法做一次性地複習和整理，也趁著此次機會將沒有學習到的內容補上。

## 1. 分支與迴圈

### 1.1 條件分支

使用 `if`、`elif` 和 `else` 進行條件判斷。

```python
x = 10
if x > 5:
    print("x 大於 5")
elif x == 5:
    print("x 等於 5")
else:
    print("x 小於 5")

###1.2 迴圈

####1.2.1 
for 迴圈
遍歷序列（如列表、字串）。

for i in range(5):  # 0 到 4
    print(i)

fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
#### 1.2.2 while 迴圈
根據條件重複執行。

x = 0
while x < 5:
    print(x)
    x += 1

####1.2.3 跳出與控制迴圈
break: 提前結束迴圈。
continue: 跳過本次迴圈，進入下一次迴圈。
pass: 保持空白，佔位用。
for i in range(5):
    if i == 3:
        break
    elif i == 1:
        continue
    print(i)
##2. 函式與遞迴

###2.1 函式
使用 def 定義函式。
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))

####2.1.1 函式參數
預設值參數
可變長度參數（*args、**kwargs）
def add(a, b=10):  # 預設值
    return a + b

def total_sum(*args):  # 可變長度
    return sum(args)

def print_info(**kwargs):  # 關鍵字參數
    for key, value in kwargs.items():
        print(f"{key}: {value}")

###2.2 遞迴
函式呼叫自身，通常需要終止條件。
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # 120

##3. 輸入與輸出

###3.1 輸入
使用 input() 接收使用者輸入（結果為字串）。
name = input("請輸入你的名字: ")
print(f"你好, {name}!")
###3.2 輸出
使用 print() 顯示內容。支援格式化輸出。
age = 20
print(f"我今年 {age} 歲")  # f-string
print("我今年 {} 歲".format(age))  # format

###3.3 檔案操作
讀取與寫入檔案：
# 寫入檔案
with open("example.txt", "w") as file:
    file.write("Hello, world!")

# 讀取檔案
with open("example.txt", "r") as file:
    content = file.read()
    print(content)

##4. 變數型態與基本運算

###4.1 變數型態
基本資料型態：int、float、bool、str
x = 10       # 整數
y = 3.14     # 浮點數
is_valid = True  # 布林值
name = "Alice"   # 字串

###4.2 資料結構
列表（list）、元組（tuple）、集合（set）、字典（dict）
# 列表
nums = [1, 2, 3]

# 元組
coords = (10, 20)

# 集合
unique_items = {1, 2, 3}

# 字典
person = {"name": "Alice", "age": 25}

###4.3 基本運算

####4.3.1 算術運算
+、-、*、/、//（整除）、%（取餘）、**（次方）

####4.3.2 比較運算
==、!=、>、<、>=、<=
x = 10
print(x == 10)  # True

####4.3.3 邏輯運算
and、or、not
a, b = True, False
print(a and b)  # False
print(a or b)   # True
print(not a)    # False

##心得:
雖然Python不會是系上主要學習的程式語言，但我相信把這個部分重新補上不僅不會有壞處，更是對學業的負責。此外，如此次期末專案所見，後面的標題都呈現不出來，希望在之後的課程裡，我能更完整的學習Github的使用方式，我相信這對於往後系上資料或報告的整理有更好的功效。
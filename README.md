Python期末報告 11124147 陳秉綜
# 二分法求平方根

設計一個用二分法計算一個大於或等於0的實數n的平方根的函數sqrt_binary(n), 實數 n和計算精度控制由用戶在同一行內輸入，用逗號進行分隔，輸出結果保留八位小數。當(abs(x*x-n))小於或等於設定的精度時，近似認為x * x == n。

程式碼
```python
import math

def sqrt_binary(num , accuracy):
	low,high = 0, num + 0.25
	while True:
		x = (high + low ) / 2
		if abs(x * x -num ) <= accuracy:
			return x
		elif x*x-num<0:
			low = x
		else:
			high = x


n ,error = map(float, input().split(','))
print('{:.8f}'.format(sqrt_binary(n,error)))
print('{:.8f}'.format(math.sqrt(n)))

```
#實作
![image](https://github.com/heart1beat/python_final/blob/main/python_final_png.png)

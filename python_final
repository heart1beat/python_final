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

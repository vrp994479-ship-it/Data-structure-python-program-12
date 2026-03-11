# Data-structure-python-program-12
arr = [1, 2, 3, 7, 5]
target = 12

start = 0
sum = 0
found = False

for end in range(len(arr)):
    sum += arr[end]

    while sum > target:
        sum -= arr[start]
        start += 1

    if sum == target:
        print(start+1, end+1)
        found = True
        break

if not found:
    print([-1])

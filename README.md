# Number-of-Subarrays-of-0-s
You are given an array arr  of length N of 0's and 1's. Find the total number of subarrays of 0's.

def count_subarrays_of_zeros(n, arr):
    count = 0
    result = 0

    for i in range(n):
        if arr[i] == 0:
            count += 1
        else:
            result += (count * (count + 1)) // 2
            count = 0

    
    result += (count * (count + 1)) // 2

    return result

try:

    n = int(input())

  
    arr = list(map(int, input().split()))

   
    print(count_subarrays_of_zeros(n, arr))

except EOFError:

    print("Input error: End of file reached.")
except Exception as e:

    print(f"Error: {e}")

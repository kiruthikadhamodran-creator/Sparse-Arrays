📊 Algorithm
Step 1: Initialize array

Create an array of size n+1 filled with zeros.

arr = [0,0,0,0,...]
Step 2: Process each query

For each query:

[a, b, k]

Perform:

arr[a] += k
arr[b+1] -= k

This marks the start and end boundaries.

Step 3: Compute Prefix Sum

Traverse the array from left to right:

arr[i] = arr[i] + arr[i-1]

This applies all range updates.

Step 4: Find Maximum Value

While computing prefix sum:

Track the maximum element:

max_value = max(max_value, arr[i])
Step 5: Return Result

Output:

max_value
⏱ Time Complexity
O(n + q)

Where:

n = size of array
q = number of queries
💾 Space Complexity
O(n)
✅ Optimization Done

Instead of updating each element inside the range:

O(n × q)

We update only:

start index
end index + 1

Then apply prefix sum once.

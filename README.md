# Self-Crossing
The "Self Crossing" problem on LeetCode asks you to determine whether a given list of integers represents a self-crossing pattern or not. This problem can be solved with a careful analysis of different cases and conditions.
Understanding the Problem:
•	A self-crossing pattern occurs if the current line crosses the previous lines at any point.
•	The list of integers represents the distance from the starting point at each step.

One way is to iterate over the list and make the path step by step, and at each step of the path check that the new position has visited before or not (v1). But this method faces time and memory issues for very large lists.
There is a better method to solve this problem without running into time or memory issues:

Define Conditions for Self-Crossing (fast method):
A self-crossing can occur in different cases, and you need to define conditions for each:


![Self Crossing](https://github.com/ParvinBayati/Self-Crossing/assets/91033182/6bef7f9c-2475-4e2f-b5c6-ddd17278bda9)


•	Case 1: If the current line crosses the line three steps back. It means that there is a crossing at i and i-3 lines.

•	Case 2: If the current line crosses the line four steps back and the current line is greater than or equal to the line two steps back.



•	Case 3: If the current line crosses the line five steps back and the current line is less than or equal to the sum of the line two steps back and the line four steps back.

# question-no-1931
Solution to the question no 1931 on leet code 

1931. Painting a Grid With Three Different Colors
You are given two integers m and n. Consider an m x n grid where each cell is initially white. You can paint each cell red, green, or blue. All cells must be painted.

Return the number of ways to color the grid with no two adjacent cells having the same color. Since the answer can be very large, return it modulo 109 + 7.

Problem:
You are given a grid with m rows and n columns. Each cell can be painted with 3 colors (say 0, 1, 2).
Constraints:

No two adjacent cells in the same row can have the same color.

No two cells in the same column of adjacent rows can have the same color.

Solution Overview:
Generate Valid Row Patterns:
Use base-3 numbers to generate all color combinations for a row of m cells, ensuring no two adjacent cells have the same color.

Find Compatible Rows:
For every valid row pattern, precompute which other row patterns can follow it (i.e., have different colors in the same columns).

Dynamic Programming:
Use DP to count the number of ways to color the grid column by column, ensuring that adjacent rows are compatible.

Final Answer:
Sum up all valid ways to color the last column.

Time Complexity Insight:
Efficient due to fixed m (max 5), making 3^m a small, manageable number of row states.

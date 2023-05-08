Download Link: https://assignmentchef.com/product/solved-qbio401-assignment4-python-function-that-takes-inputs
<br>
<ol>

 <li>Write a Python function that takes five inputs:</li>

 <li>A DNA sequence string X,</li>

 <li>A DNA sequence string Y,</li>

 <li>A score <em>S<sub>match</sub></em> occurs for matching the characters of X and Y,</li>

 <li>A penalty <em>P<sub>mismatch</sub></em> occurs for mismatching the characters of X and Y, and</li>

 <li>A penalty <em>P<sub>gap</sub></em> occurs if a gap is inserted into the string.</li>

</ol>

This function returns a Dynamic Programming scoring matrix for the global pairwise alignment.

For example, with the inputs (‘ACGA’, ’CACT’, 3, -1, -2)

First, the function initializes a scoring matrix. The first row and column of the matrix are filled with gap scores.

Second, the function fills the matrix from the upper-left-hand corner of the matrix. To find the maximum score of each cell, it is required to know the neighboring scores (diagonal, left and up) of the current position. Compare three values: the value adding the match or mismatch score to the diagonal neighboring score, the value adding the gap score to the left neighboring score, and the value adding the gap score to the up neighboring score. Take the maximum among these three values and fill it into the i<sub>th</sub> and j<sub>th</sub> position. For instance, -1 (marked in red below) is the maximum among three values: 0-1=-1 (the diagonal neighboring score plus a mismatch score), -2-2=-4 (the up neighboring score plus a gap penalty), -2-2=-4 (the left neighboring score plus a gap penalty). With this rule, fill up the scoring matrix completely.

<ol start="2">

 <li>[Bonus] Modify Function #1 to be able to store the back pointer to the cell from where the maximum score is obtained in each step. One way is that the function creates an extra matrix with the same size as the scoring matrix to store these pointers. This function traces back step from the bottom-right-hand corner of the matrix. Finally, this function returns the optimal alignment (return one of the optimal alignments if there are many) [Bonus 2pt].</li>

</ol>






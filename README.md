# Computational Practice: Align two sequences with dynamic programming
##  Lab Overview
Pairwise sequence alignment means the alignment of two nucleic acid or two protein sequences. 
(Note: multiple sequence alignment (MSA) = 3+ sequences)
There are many ways to align two sequences. The optimal alignment is the one with most similar/identical residues. 	
	--> Optimal alignment has the highest ‘score’
	--> Scores come from scoring matrices
	--> Best alignment may or may not be biologically meaningful
Alignment score provides evidence that for the hypothesis that two sequences share a common ancestral sequence (aka Evidence that two sequences are homologs).
If two sequences are homologs, it is evidence that they could have the same molecular function (so you can map known function between them).
##  Lab Objectives:
In this lab, you will perform pairwise sequence alignment by hand.
•	Align two DNA sequences using the Needleman-Wunsch dynamic programming global alignment algorithm.
•	Align two protein sequences using the Smith-Waterman dynamic programming local alignment algorithm.
Follow these lab instructions:
###  Task A: 
Using the dynamic programming algorithm, globally align these two DNA sequences:

```
GGCAACTTCACAT (sequence i) 

GGCAACTTCAGCAT (sequence j) 
```

The scoring system is: (match= +2; mismatch = -1; gap = -3)*. Please do the following: 

a.	On a piece of paper, complete the scoring matrix. Note trace-back arrows.
b.	Outline the trace-back route(s).
c.	Write down the resulting optimal GLOBAL (Needleman-Wunsch) alignment. 
d.	Record the final score of the optimal alignment.


*These numbers reflect a substitution (scoring) matrix like PAM/BLOSUM.  It’s simpler to state scores since it doesn’t matter which nucleotides are substituted.  The matrix, however, would look like this…

||A|T|G|C|
|A|2|-1|-1|-1|
|T|-1|2|-1|-1|
|G|-1|-1|2|-1|
|C|-1|-1|-1|2|


###  Task B: 
Using the dynamic programming algorithm, locally align these two PEPTIDE sequences:
 
	QSTFAQEWDS (sequence i)
	WSTFAQETS (sequence j)

The scoring system is: (BLOSUM80 with gap penalty = -6; Here is the BLOSUM80 matrix: https://www.cbcb.umd.edu/confcour/CMSC423-materials/BLOSUM80.txt). 

Please do the following: 

a.	On a piece of paper, complete the scoring matrix. Note trace-back arrows.
b.	Outline the trace-back route(s).
c.	Write down the resulting optimal LOCAL (Smith-Waterman) alignment. 
d.	Record the final score of the optimal alignment.


// Relational Algebra

What is Relational Algebra?
Relational Algebra is procedural query language, which takes Relation as input and generate relation as output. It uses operators to perform queries. An operator can be either unary or binary.

Fundamental Operations of Relational algebra

1. Select: It is denoted by (σ). Select is used to select required tuples(a single row in a table represents a set of related data) of the relations.
Notation:  σ p(r)
* σ is used for selection prediction
* r is used for relation
* p is used as a propositional logic formula which may use connectors like: AND OR and NOT. These relational can use as relational operators like =, ≠, ≥, <, >, ≤.

For Example: 

BRANCH_NAME	       LOAN_NO	    AMOUNT
Downtown	       L-17	         1000
Redwood	           L-23       	 2000
Perryride	       L-15	         1500
Downtown	       L-14	         1500
Mianus	           L-13       	  500
Roundhill	       L-11	          900
Perryride	       L-16	         1300

Input: σ BRANCH_NAME="Downtown" (LOAN)

Output:

BRANCH_NAME	      LOAN_NO	AMOUNT
Downtown	      L-17	     1000
Downtown	      L-14	     1500

2. Project: It is denoted by (π). Projection is used to project required column data from a relation. This operation shows the list of those attributes that we wish to appear in the result. Rest of the attributes are eliminated from the table.

For Example: 

      R 
  (A  B  C)    
  ----------
   1  2  4
   2  2  3
   3  2  3
   4  3  4

Input:  π (BC) 

Output: 

B  C
-----
2  4
2  3
3  4

In this case, we took list of attribute BC only. As it is shown 2 3 is repeated twice we took only once

3. Union: It is denoted by (∪). Suppose there are two tuples A and S. The union operation contains all the tuples that are either in A or S or both in A & S. It eliminates the duplicate tuples

Notation: A ∪ S 

Tuple A:

CUSTOMER_NAME	ACCOUNT_NO
Johnson	           A-101
Smith	           A-121
Mayes	           A-321
Turner	           A-176
Johnson	           A-273
Jones	           A-472
Lindsay	           A-284

Tuple S:

CUSTOMER_NAME	ACCOUNT_NO
Jones	         A-472
Smith	         A-121
Hayes	         A-151
Jackson	         A-141
Curry	         A-192
Williams	     A-174

Input: A ∪ S 

Output: 

CUSTOMER_NAME	ACCOUNT_NO
Johnson	           A-101
Smith	           A-121
Mayes	           A-321
Turner	           A-176
Johnson	           A-273
Jones	           A-472
Lindsay	           A-284
Hayes	           A-151
Jackson	           A-141
Curry	           A-192
Williams	       A-174

4. Set difference: It is denoted by (∩). Suppose there are two tuples A and S. The set difference operation contains all the tuples that are in both A & S. 

Notation: A ∩ S 

Tuple A:

CUSTOMER_NAME	ACCOUNT_NO
Johnson	           A-101
Smith	           A-121
Mayes	           A-321
Turner	           A-176
Johnson	           A-273
Jones	           A-472
Lindsay	           A-284

Tuple S:

CUSTOMER_NAME	ACCOUNT_NO
Jones	         A-472
Smith	         A-121
Hayes	         A-151
Jackson	         A-141
Curry	         A-192
Williams	     A-174

Input: A ∩ S 

Output: 

CUSTOMER_NAME	ACCOUNT_NO
Smith	           A-121
Jones	           A-472
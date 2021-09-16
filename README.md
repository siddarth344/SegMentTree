# SegMentTree
that can be used for almost any type of range queries like range sum, range minimum, range product queries or any other user defined queries.
General purpose segment tree library.

include SegmentTree.h

to construct a segment tree you need to specify the following:
a. The datatype of array for which the tree is being constructed.
b. an array or vector for which the tree is to be constructed.
c. a value that can be used to fill the extra nodes of the tree.
d. a function combine that specifies how the result of left and right child of a node should be used to generate the value of current node.

Example usage:
int small(int x,int y){return min(x,y);}
SegmentTree < int > rangeMinQueries(dataVector,INT_MAX,small);

int sum(int x,int y){return x+y;}
SegmentTree < int > rangeSumQueries(dataVector,0,sum);

long long product(long long x,long long y){return x*y;}
SegmentTree < long long > rangeProductQueries(dataVector,1,product);

I am demonstrating that how one can use this library in his code-
ex.1 problem link of GSS1 problem spoj: https://www.spoj.com/problems/GSS1/
      solution to SPOJ GSS1 using segTree library : https://ideone.com/QkVcKA

# interview-bit---array---kth-row-of-pascal-s-triangle

------> Question:

Given an index k, return the kth row of the Pascal's triangle.
Pascal's triangle: To generate A[C] in row R, sum up A'[C] and A'[C-1] from previous row R - 1.

Example:

Input : k = 3


Return : [1,3,3,1]

Note: k is 0 based. k = 0, corresponds to the row [1]. 

Note: Could you optimize your algorithm to use only O(k) extra space?



------> short Code:

vector<int> Solution::getRow(int n) {
  
    vector<int>v;
    int res=1;
    v.push_back(1); 
    for(int i=1;i<=n;i++){
        res = (res*(n-i+1))/i; 
        v.push_back(res);
    }
    return v;
}

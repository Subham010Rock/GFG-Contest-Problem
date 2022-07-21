# GFG-Contest-Problem

## [Assign Tasks](https://practice.geeksforgeeks.org/contest/gfg-hiring-mts-internship/problems/#)

Solution--
```
class Solution
{
    public:
    long long solve(int n,long long A[], long long B[])
    {
        // add your code here
        
        sort(A,A+n,greater<long long>());
        sort(B,B+n,greater<long long>());
        int res=0;
        for(int i=0;i<n;i++ ){
                int d=ceil((double)A[i]/B[i]);
                res=max(res,d);
                
        }
        return res;
       
    }
};
```

## [Remove and Reverse](https://practice.geeksforgeeks.org/contest/gfg-hiring-mts-internship/problems/#)

Solution--
```
class Solution:
    def removeReverse(self, S): 
        #code here
        d={}
        t=len(S)
        for i in S:
            d[i]=d.get(i,0)+1
        i=0
        while i<t:
            if(d[S[i]]>1):
                d[S[i]]-=1
                S=S.replace(S[i],"",1)
                S=S[::-1]
                i=0
                t-=1
            else:
                i+=1
        return S
```
## [Maximum Frequency](https://practice.geeksforgeeks.org/contest/job-a-thon-10-hiring-challenge/problems/)

Solution--
```
class Solution():
    def solve(self, n, y, A):
        #your code goes here
        d={}
        m=0;
        for i in A:
            d[i]=d.get(i,0)+1
            m=max(m,d[i])
        return m
```
## [Minimum Swaps](https://practice.geeksforgeeks.org/contest/job-a-thon-10-hiring-challenge/problems/)

Solution--
```
class Solution {
  public:
    int count(int N,vector<vector<int>> A,vector<vector<int>> B) {
        // code here
        int different=0;
        int sum_A=0;
        int sum_B=0;
        for( int i=0;i<N;i++){
            for( int j=0;j<N;j++){
                sum_A+=A[i][j];
                sum_B+=B[i][j];
                if(A[i][j]!=B[i][j]){
                   different+=1;
                }
            }
        }
        if(sum_A!=sum_B)
        return -1;
        else
        return different/2;
    }   
 ```
## [Even subaaray sum](https://practice.geeksforgeeks.org/contest/job-a-thon-11-hiring-challenge/problems/)

Solution--
```
class Solution {
    public:
    string solve(int N, vector<int> &A){
        // code here
        for(int i=0;i<N-1;i++){
            if(A[i]+A[i+1]!=0)
            return "NO";
        }
        return "YES";
        
    }
};
```
## [Rectangles and Squares](https://practice.geeksforgeeks.org/contest/job-a-thon-11-hiring-challenge/problems/)

Solution--
```
class Solution{
  public:
     int minimumMoves(int A, int B){

        if(A==B)
           return 1;
        int res=0;
        while(A!=0 and B!=0){
            if(A>B){
                res+=A/B;
                A=A%B;
            }
            else{
                res+=B/A;
                B=B%A;
            }
        }
        return res;
    }
 };

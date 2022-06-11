# GFG-Contest-Problem

## Problem No. 1-[Assign Tasks](https://practice.geeksforgeeks.org/contest/gfg-hiring-mts-internship/problems/#)

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

## Problem No. 2-[Remove and Reverse](https://practice.geeksforgeeks.org/contest/gfg-hiring-mts-internship/problems/#)

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

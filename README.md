# Reduce-Array-Size-to-the-Half
class Solution:
    def minSetSize(self, arr: list[int]) -> int:
        n=len(arr)
        count=Counter(arr)
        r=[]
        c1=0
        for c in sorted(count.values(),reverse=True):
            c1+=c
            r.append(c)
            if c1>=n//2:
                return len(r)

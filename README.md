class Solution:
    def maxWidthOfVerticalArea(self, points: List[List[int]]) -> int:
        x = [i[0] for i in points]
        x.sort()
        y = 0
        for j in range(1,len(x)):
            y = max(y,x[j]-x[j-1])
        return y

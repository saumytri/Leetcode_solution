# Leetcode_solution


Pascal's triangle leetcode 118:
class Solution {
    public List<List<Integer>> generate(int numRows) {
        if(numRows==0)return new ArrayList();
        List<List<Integer>> a=new ArrayList();
         for(int i=1;i<=numRows;i++)
         {
             List<Integer> curr=new ArrayList();
             for(int j=0;j<i;j++)
             {
                 if(j==0||j==i-1)
                 curr.add(1);
                 else
                 {
                     curr.add(a.get(i-2).get(j)+a.get(i-2).get(j-1));
                 }

             }
             a.add(curr);
         }
         return a;
    }
}

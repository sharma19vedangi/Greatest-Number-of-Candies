# Greatest-Number-of-Candies
#Array Leetcode Problem Solution
class Solution {
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
   
        ArrayList<Boolean> result = new ArrayList<Boolean>();
        int check;
        int max=candies[0];
        for(int i=1;i<candies.length;i++)
        {
            if(max<candies[i])
            {
                max=candies[i];
            }
        }
        for(int i=0;i<candies.length;i++)
        {
            check=0;
            check=candies[i]+extraCandies;
            if(check>=max)
            {
                result.add(true);
            }
            else
            {
                result.add(false);
            }
        }
        return result;
    }
}

    1. https://leetcode.com/problems/longest-common-subsequence/
    
    def longestCommonSubsequence(text1: String, text2: String): Int = {
        val cache = Array.tabulate(text1.length,text2.length)((r,c) => -1)
        //start with index 0 for both string
        //helperZero(text1,0,text2,0,cache)
        val res = helper(text1,0,text2,0,0,cache)
        for(i<- 0 until text1.length){
            for(j <- 0 until text2.length){
                println(i +" "+j +" "+cache(i)(j))
            }
        }
        res
        
    }
    
    def helper(text1:String,i:Int,text2:String,j:Int,soFar:Int,cache:Array[Array[Int]]): Int = {
        if(i == text1.length || j == text2.length){
            soFar
        }  else if(cache(i)(j) != -1) cache(i)(j)
        else {
            var max = 0
            if(text1(i) == text2(j)) {
                max = max.max(helper(text1,i+1,text2,j+1,soFar+1,cache))    
            } else {
                max = max.max(helper(text1,i+1,text2,j,soFar,cache))
                max = max.max(helper(text1,i,text2,j+1,soFar,cache))
            }
            cache(i)(j) = max
            max
        }
    }
}

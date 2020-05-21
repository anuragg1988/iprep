# iprep
iprep with Anurag

1. https://www.hackerrank.com/challenges/special-palindrome-again/problem?h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=strings

Nice question, i was not able to optimise it and had to see the solution to understand
https://www.geeksforgeeks.org/count-special-palindromes-in-a-string/
1. For non repeating case - keeps an extra array with continuous repeating freq of char at each index ex
str =   "a a b a c c c"
arr[]= { 2 2 1 1 3 3 3 }
check at each index for str.charAt(curr - 1) == str.charAt(curr +1) => count += min(arr[curr-1],arr[curr+1])


2. https://www.hackerrank.com/challenges/common-child/problem?h_l=interview&playlist_slugs%5B%5D=interview-preparation-kit&playlist_slugs%5B%5D=strings

This i am still doing

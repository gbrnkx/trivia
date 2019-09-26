Write the pseudocode of a function, which takes as input a String, and returns True if it is palindrome, or False otherwise.

> A palindrome is a word, phrase, or sequence that reads the same backwards as forwards

Example:
*  "savvas" => true
*  "pambos" => false

checkPalindrome(input){
SET left = 0
SET right = input.length - 1
SET isPalindrome = true

WHILE LOOP
Break when left > right OR isPalindrome = false
	
	IF input[left] = input[right] THEN
		Increment left by 1
		Decrement right by 1
	ELSE
		isPalindrome = false
    break;

RETURN isPalindrome
}

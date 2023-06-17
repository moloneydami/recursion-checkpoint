# recursion-checkpoint
This is a Recursion project.

ALGORITHM

1. If the length of the word is 0 or 1, return True (base case).
2. If the first and last characters of the word are different, return False (base case).
3. Extract the middle substring of the word (excluding the first and last characters).
4. Recursively call the isPalindrome function with the remaining substring.
5. Repeat steps 1-4 until a base case is reached or a difference is found.


CODE

FUNCTION isPalindrome(word: STRING) RETURNS BOOLEAN
    IF length(word) ≤ 1 THEN
        RETURN True
    END IF
    
    IF word[0] ≠ word[length(word) - 1] THEN
        RETURN False
    END IF
    
    RETURN isPalindrome(substring(word, 1, length(word) - 2))
END FUNCTION


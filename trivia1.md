Write, in pseudo-code, an efficient way of doing the following conversions and explain the complexity of the solution in big O notation

  1. Words only
  "Reverse this sentence" => "sentence this Reverse"

  SET sentence = "Reverse this sentence"
  SET words = []
  SET word = ""
  SET r_sentence = ""

  FOR LOOP
  SET char = 0 
  Break when char > sentence.length - 1
  Increment char by 1
	  IF sentence[char] = " " OR char = sentence.length - 1  THEN
		  PUSH word to words
		  word = ""
	  ELSE
		  word = word + char

  WHILE LOOP
  Break when words.length = 0 DO
	  r_sentence = r_sentence + words.POP + " "

  PRINT r_sentence

This algorithm is O(n) because although it has 2 LOOP inside, these LOOPs are not nested. The execution speed is directly proportional to the length of the input sentence.

  2. Logical case
  "Reverse this sentence" => "Sentence this reverse"

  SET sentence = "Reverse this sentence"
  SET words = []
  SET word = ""
  SET r_sentence = ""

  FOR LOOP
  SET char = 0 
  Break when char > sentence.length - 1
  Increment char by 1
	  IF sentence[char] = " " OR char = sentence.length - 1  THEN
		  PUSH word to words
		  word = ""
	  ELSE
		  word = word + char

  SET first = false

  WHILE LOOP
  Break when words.length = 0 DO
	  IF first = false THEN
		  r_sentence = r_sentence + words.POP.CAPITALIZE + " "
		  first = true
	  ELSE IF words.length = 1 THEN
		  r_sentence = r_sentence + words.POP.DOWNCASE
	  ELSE 
		  r_sentence = r_sentence + words.POP + " "

  PRINT r_sentence

This algorithm is also O(n) because although it has 2 LOOP inside, these LOOPs are not nested. The execution speed is directly proportional to the length of the input sentence.
  
  3. Logical dot anotation
  "Reverse this sentence." => "Sentence this reverse."

  SET sentence = "Reverse this sentence"
  SET words = []
  SET word = ""
  SET r_sentence = ""

  FOR LOOP
  SET char = 0 
  Break when char > sentence.length - 1
  Increment char by 1
	  IF sentence[char] = " " OR char = sentence.length - 1  THEN
		  PUSH word to words
		  word = ""
	  ELSE
		  word = word + char

  SET first = false

  WHILE LOOP
  Break when words.length = 0 DO
	  IF first = false THEN
		  r_sentence = r_sentence + words.POP.CAPITALIZE + " "
		  first = true
	  ELSE IF words.length = 1 THEN
		  r_sentence = r_sentence + words.POP.DOWNCASE + "."
	  ELSE 
		  r_sentence = r_sentence + words.POP + " "

  PRINT r_sentence

This algorithm is also O(n) because although it has 2 LOOP inside, these LOOPs are not nested. The execution speed is directly proportional to the length of the input sentence.
  
  4. Something more tricky
  "aaagggaaaiinnnnn" => "3a3g3a2i5n"

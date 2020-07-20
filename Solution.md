# Basic-JavaScript-Questions 

# Practice Questions

## Tracing Code

### Logical Operators 

Question: What is the output?

    alert( true && true );    //   true
    alert( false && true );   //   false
    alert( true && false );   //   false 
    alert( false && false );  //   false 



Question: What is the output?

    alert( true || true );    //  true
    alert( false || true );   //  true
    alert( true || false );   //  true
    alert( false || false );  //  false

Question: What is the output?

    alert( !true );     //  false
    alert( !0 );        //  true

### While Loops 

Question: What is the output?

    var i = 0;
    while (i < 3) {
        console.log("hi");
        i++;    
    }
    
Output:

    hi
    hi
    hi
___


## Writing Code


### Basic (Arithmetics)

1. Write a code to give the sum of x and y where x = 10 and y = 2 

        var x = 10;
        var y = 2;
        console.log( x + y );

1. Write a code to get the remainder of x divided by y where x = 10 and y = 2

        var x = 10;
        var y = 2;
        console.log( x % y );   

1. Write a code to get the quotient of x divided by y where x = 10 and y = 2

        var x = 10;
        var y = 2;
        console.log( x / y ); 

1. Write a code to determine if the number x is odd or even

        x = 10      // some value of x 
        if ( x % 2 == 0 ) {
            console.log('even');
        } else {
            console.log('odd');
        }

1. Write a code to determine if the number y is a multiple of 11 where y >= 11

        y = 11     // some value of y where y >= 11
        if ( y % 11 == 0) {
            console.log('y is a multiple of 11');
        } else {
            console.log('y is not a multiple of 11');
        }


### Basic (Logical Operators)

1. Write a code to determine if x is equal to y where *x = a + 2b* and *y = c + 2d* for the following permutations

    a = 1, b = 1, c = 1, d = 1     
    a = 1, b = 2, c = 2, d = 2  
    a = 1, b = 2, c = 1, d = 2

        var a = 1, b = 2, c = 1, d = 2 // where a,b,c,d are the respective values as given above

        console.log((a + 2 * b) === (c + 2 * d))


1. Logical operators are used when we want to check the truth value of certain statements. Logical operators help us in checking multiple statements together for their truthness.

    Here we will learn logical operators like AND(&&), OR(||), NOT(!). These operators produce either a true or a false as an output.

    Input Format:
    First line of input conatins number of testcases T. For each testcase, there will be one line of input containing a and b separated by a space.

    Output Format:
    For each testcase, print the required output.

    Your Task:
    Your task is to complete the provided function.

    Constraints:
    1 <= T <= 10
    1 <= a, b,<= 100

    Input:
    1
    6 7

    Output:
    1 1 0

    Taken from: https://practice.geeksforgeeks.org/problems/logical-operators/1

        var num_of_test_cases = 1, a = 6, b = 7

        for (var i = 0; i < num_of_test_cases; i++) {
            if(a&&b)
            {
                console.log(1)
            }
            else
            {
                console.log(0)
            }
            if(a||b)
            {
                console.log(1)
            }
            else
            {
                console.log(0)
            }
            if(((!a)&&(!b)))
            {
                console.log(1)
            }
            else
            {
                console.log(0)
            }
        }


### Basic (String)

1. Write a code to determine the length of the string

        var word = 'string'
        console.log(word.length)

1. Write a code to determine if a character 'e' is present in the words 'hi' and 'bye'

        var word1 = 'hi'
        var word2 = 'bye'

        // Check 'hi' for 'e'
        if (word1.indexOf('e') == -1) {
            console.log(word1 + ' does not contain e')
        } else {
            console.log(word1 + ' contain e')
        }

        // Check 'bye' for 'e'
        if (word2.indexOf('e') == -1) {
            console.log(word2 + ' does not contain e')
        } else {
            console.log(word2 + ' contain e')
        }

1. Write a code to reduce the word 'meet' to 'met'

        var word = 'meet'
        var new_word = ''

        for (var i = 0; i < word.length; i++) {
            if (word[i] != word[i+1] ) {
                new_word += word[i]
            }
        }

        console.log(new_word)

1. Write a code to determine if the length of the password provided is between 6 to 10 characters

        var password = 'abcdefghijk'

        if (password.length >= 6 && password.length <= 10) {
            console.log('Valid Password')
        } else {
            console.log('Invalid Password')
        }

1. Given a string, reverse each letter in the word

    Input:
    ram

    Output:
    mar

        var word = 'ram'
        word.split('')
        var new_word = ''
        for (var i = word.length - 1; i >= 0; i--) {
            new_word += word[i]
        }

        console.log(new_word)

1. Write code to check a String is palindrome or not?

    A palindrome is a word, number, phrase, or other sequence of characters which reads the same backward as forward, such as madam, racecar.

    Input:  
    madam   
    
    Output:
    True    

        var word = 'madam'
        word.split('')
        var new_word = ''
        for (var i = word.length - 1; i >= 0; i--) {
        new_word += word[i]
        }

        console.log(new_word == word)

    Input:  
    ram

    Output:
    False 

        var word = 'ram'
        word.split('')
        var new_word = ''
        for (var i = word.length - 1; i >= 0; i--) {
        new_word += word[i]
        }

        console.log(new_word == word)

1. Write code to check two String are Anagram
    
    An anagram is a word or phrase formed by rearranging the letters of a different word or phrase, typically using all the original letters exactly once

        // Elbow = Below
        var word1 = 'Elbow'
        var word2 = 'Below'
        word1 = word1.toLowerCase().split('').sort()
        console.log(word1)
        word2 = word2.toLowerCase().split('').sort()
        console.log(word2)

        var flag = true 

        for (var i = 0; i < word1.length; i++) {
            if (word1[i] != word2[i]) {
                flag = false
            }
        }

        if (flag) {
            console.log('anagram')
        } else {
            console.log('not anagram')
        }


1. Given a non-empty sequence of characters, return true if sequence is Binary, else return false

        var sequence = '0100110111'

        var isBinary = true

        for (var i = 0; i < sequence.length; i++) {

            if (! (sequence[i] == '0' || sequence[i] == '1') ) {
                isBinary = false
            }
        }

        if (isBinary) {
            console.log('binary')
        } else {
            console.log('not binary')
        }


### Advance (IF ELSE, SWITCH)
1. The taxi fare structure in Singapore must be one of the most complex in the world! Check out: http://www.taxisingapore.com/taxi-fare/.

    For the purpose of this exercise, we will just use the following simpliﬁed fare structure:

    Basic Fare	    
    The first 1 km or less (Flag Down)	$3.40   
    Every 400 m thereafter or less, up to 10.2 km	$0.22   
    Every 350 m thereafter or less, after 10.2 km	$0.22   

    Write a code to calculate how much a person must pray if he were to travel 24km.

        var distance = 24, sum = 0, distance_calculated = 0

        distance -= 1 // first km
        distance_calculated += 1
        sum += 3.4

        while (distance > 0) {
        
        if (distance_calculated < 10.2) { // Every 400 m thereafter or less, up to 10.2 km
            distance -= 0.400 
            distance_calculated += 0.400
        } else { // Every 350 m thereafter or less, after 10.2 km
            distance -= 0.350
            distance_calculated += 0.350
        }

        sum += 0.22
        }

        console.log(sum)




### Advance (Maths)
1. Write a code that reads three positive integers representing the length, width, and height of a box, and output  
    (i) its surface area, and 
    (ii) the length of the diagonal between two vertices of the box that are furthest apart.


    Input:  
    10 20 30

    Output:     
    2200 37.4166    

        var length = 10, width = 20, height = 30
        var surfaceArea = ( length * width + length * height + width * height ) * 2
        var diagonal_base = Math.sqrt(length*length+width*width)
        var diagonal_vertices = Math.sqrt(diagonal_base*diagonal_base+height*height)

        console.log('surface area', surfaceArea)
        console.log('diagonal vertice', diagonal_vertices)

### Advance (Loop)

1. Write a code that reads in a non-negative integer, and prints the sum of the individual digits in this integer.

    For instance, if the input is 1933091, then the sum is 1 + 9 + 3 + 3 + 0 + 9 + 1 = 26.

    You should not use a loop to solve this, but rather, you should write a function sum_of_digits that takes in an integer and return the sum of the digits of that integer, that calls itself:

    if the input to sum_of_digits has only one digit, return this digit.
    Otherwise, use the modulo operator % and integer division / to extract the last digit (e.g., 1) and the rest of the digits (e.g., 193309) respectively, and call sum_of_digits on the rest of the digits to find its sum (e.g., 1+9+3+3+0+9 = 25). Finally we add the last digit to this sum to get the total we seek (e.g., 1 + 25 = 26).

    Taken from: https://nus-cs1010.github.io/1819-s1/as01.html#question-3-digits-5-marks

    Input:  
    1933091

    Output:     
    26

    
        var num = 1933091, sum = 0

        while (num > 0) {
        
        sum += num % 10
        num = num / 10
        num = Math.floor(num)
        // console.log(num)  

        }

        console.log(sum)



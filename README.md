Download Link: https://assignmentchef.com/product/solved-cse222-505-data-structures-and-algorithms-homework-3
<br>
GTU Computer Science and EngineeringCSE 222/505 –Homework #03Version 31) Counting components.A binary digital image is represented through a matrix of integers, each element of which is either 1(white) or 0 (black) (40 points). Example of an image (6 rows, 11 columns) (left) and thecorresponding binary image (right):0 0 0 0 0 0 0 0 0 0 00 0 1 0 0 0 1 0 0 0 00 1 1 1 1 0 0 1 0 1 00 1 1 0 1 0 0 0 0 1 10 0 0 1 1 0 0 0 1 1 00 0 0 0 0 0 0 0 0 0 0

<img decoding="async" data-recalc-dims="1" data-src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/04/809.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

 <noscript>

  <img decoding="async" src="https://i0.wp.com/www.ankitcodinghub.com/wp-content/uploads/2020/04/809.png?w=980&amp;ssl=1" data-recalc-dims="1">

 </noscript>InputYou are to write a program that admits as a commandline argument the path to a ASCII text filecontaining a binary digital image represented through a matrix of space separated integers such asthe one above.OutputYour program will calculate the number of “white components” and print that number on screen.ExplanationA white component is a set of white matrix locations, such that, between any two of them, there is apath of white matrix locations, where every consecutive pair are adjacent (through their top, left,right or bottom neighbor). Hence the above example contains four components, shown here withletters A, B, C and D:0 0 0 0 0 0 0 0 0 0 00 0 A 0 0 0 B 0 0 0 00 A A A A 0 0 C 0 D 00 A A 0 A 0 0 0 0 D D0 0 0 A A 0 0 0 D D 00 0 0 0 0 0 0 0 0 0 0Assume location (0,0) corresponds to the top left element.B contains the locations (in column,row format): (6,1)C contains the locations (in column,row format): (7,2)D contains the locations (in column,row format): (9,2)(9,3)(9,4)(10,3)(8,4)etce.g. locations (10,3) and (8,4) (in pink) belong to the same white component since there is a path(i.e. a sequence) of white locations starting from (10,3) and ending at (8,4): (10,3),(9,3),(9,4),(8,4)such that every consecutive location pair z=(x1,y1) and w=(x2,y2) are neighbors (i.e. z is either ontop, bottom, left or right of w; e.g.(8,4) is at the left of (9,4)).You need to visit every matrix element at least once in order to accomplish this goal. So yourcomplexity will be at least O(n) where n is the number of matrix elements. Solutions with lowercomplexities will be rewarded.Rules– Don’t use recursive functions.– Your program will be tested with an arbitrary matrix– Don’t use any Java class implementing the Collection interface; (implement your own datastructures).– Hint 1: you can represent your matrix as a 2 dimensional array of integers.– Hint 2: you might want to use a stack in your algorithm for white component counting.2) A calculatorWrite a program that evaluates an infix expression (40 points). You already know that you mustfirst convert it to postfix and then evaluate the postfix expression with a stack based algorithm.The trick is that the infix expression can contain:– variables– functions (only sin, cos, abs)– parenthesisInputThe input will be provided through the commandline as a path to file containing a single infixexpression (an example is provided at the moodle page: infix_test_file_1.txt). The expression’stokens will be space separated.OutputThe infix expression’s value.Rules– Don’t use any Java classes implementing Java’s Collection interface; (implement your own datastructures).– Do not call any method from the Math class of java, implement your own sin, cos, abs methods.
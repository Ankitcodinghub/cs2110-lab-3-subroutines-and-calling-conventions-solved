# cs2110-lab-3-subroutines-and-calling-conventions-solved
**TO GET THIS SOLUTION VISIT:** [CS2110 Lab 3-Subroutines and Calling Conventions Solved](https://www.ankitcodinghub.com/product/cs2110-lab-3-subroutines-and-calling-conventions-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92796&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS2110 Lab 3-Subroutines and Calling Conventions Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column"></div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Purpose

The purpose of this timed lab is to test your understanding of implementing subroutines in the LC-3 assembly language using the calling convention, from both the callee and caller side.

2.2 Task

You will implement the subroutines listed below in LC-3 assembly language. Please see the detailed instruc- tions for the subroutines on the following pages. We have provided pseudocode for the subroutines—you should follow these algorithms when writing your assembly code. Your subroutines must adhere to the LC-3 calling conventions.

2.3 Criteria

Your assignment will be graded based on your ability to correctly translate the given pseudocode for a subroutine (function) into LC-3 assembly code, following the LC-3 calling convention. Please use the LC-3 instruction set when writing these programs. Check the Deliverables section for what you must submit to Gradescope.

You must produce the correct return values for each function. In addition, registers R0-R5 and R7 must be restored from the perspective of the caller, so they contain the same values after the caller’s JSR subroutine call. Your subroutine must return to the correct point in the caller’s code, and the caller must find the return value on the stack where it is expected to be. If you follow the LC-3 calling conventions correctly, all of these things will happen automatically. Additionally, we will check that you made the correct subroutine calls, so you should not try to implement a recursively subroutine iteratively.

Your code must assemble with no warnings or errors (Complx and the autograder will tell you if there are any). If your code does not assemble, we will not be able to grade that file and you will not receive any points.

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
3 Detailed Instructions

For this Timed Lab, you will be implementing three subroutines: ABS, POW3 and MAP. ABS is a non-recursive subroutine that will calculate the absolute value of its argument. POW3 is a recursive subroutine that will compute 3 to the power of its argument. MAP will iterate through an array and apply one of the two subroutines above to each of the elements.

3.1 ABS subroutines

ABS will take one argument that should be loaded from the stack. You should implement the subroutine as

shown in the pseudocode below:

<pre>    // checkpoint 1
    int ABS(int x) {
        if (x &lt; 0) {
</pre>
<pre>            return -x;
        } else {
</pre>
return x; }

}

Examples:

• ABS(5) returns 5 • ABS(0) returns 0 • ABS(-3) returns 3

Implementing ABS will be the first checkpoint. Please refer to Checkpoints for details on how ABS will be graded.

3.2 POW3 subroutine

POW3 will take one non-negative integer argument n and compute 3n; that is, 3 raised to the power of

the argument. You should implement the subroutine as shown in the pseudocode below:

<pre>    int POW3(int n) {
        if (n == 0) {
</pre>
<pre>            return 1;               // (checkpoint 2) base case: 3ˆ0 = 1
        } else {
</pre>
<pre>            return 3 * POW3(n - 1); // (checkpoint 3) recursive case
        }
</pre>
}

Examples:

• POW3(0) returns 1 • POW3(1) returns 3 • POW3(3) returns 27

POW3 contains two checkpoints. Checkpoint 2 is the base case: returning 1 when n == 0. Checkpoint 3 is the recursive case: POW3 should return the correct value for all non-negative integers. Please refer to Checkpoints for details on how POW3 will be graded.

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
3.3 MAP subroutine MAP takes two arguments:

• array: The address of the first element in the array to be modified • length: The length of the array to be modified

MAP should iterate through the array. For every element at an even index, it should apply ABS to it and replace the element with the result. For every element at an odd index, it should apply POW3 to it and replace the element with the result.

Hint: remember Homework 1. What’s a simple way using bitwise operations to check that a number is even or odd without doing a full mod operation?

You should implement the subroutine as shown in the pseudocode below:

<pre>    // checkpoint 4
    void MAP(array, length) {
</pre>
<pre>        i = 0;
        while (i &lt; length) {
</pre>
<pre>            element = arr[i];
            if (i % 2 == 0) {
</pre>
<pre>                result = ABS(element);
            } else {
</pre>
<pre>                result = POW3(element);
            }
</pre>
<pre>            arr[i] = result;
</pre>
i = i + 1; }

}

You do not need to return a value from MAP. While you will still leave a spot for a return value on the stack,

it will be ignored.

Correctly implementing MAP is checkpoint 4. Please refer to Checkpoints for details on how MAP will be graded.

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
4 Checkpoints

4.1 Checkpoints (70 points)

In order to get all of the points for this timed lab, your code must meet these checkpoints:

<ul>
<li>Checkpoint 1 (15 points): In ABS, load the parameters x and compute the absolute value to return
|x|.
</li>
<li>Checkpoint 2 (15 points): Implement the base case for POW3 to return 1 when n == 0.</li>
<li>Checkpoint 3 (20 points): Implement the recursive case of POW3 to successfully compute and return 3n for any non-negative integer n.</li>
<li>Checkpoint 4 (20 points): Implement MAP. You should iterate through the array, and apply the ABS subroutine to elements at all even indices and the POW3 subroutine to elements at all odd indices. The results of each subroutine call must be properly stored back into the array at every index.</li>
</ul>
4.2 Other Requirements (30 points)

Your subroutine must follow the LC-3 calling convention. Specifically, it must fulfill the following conditions:

<ul>
<li>Your subroutine must be recursive and call itself according to the pseudocode’s description.</li>
<li>When your subroutine returns, every register must have its original value preserved (except R6).</li>
<li>When your subroutine returns, the stack pointer (R6) must be decreased by 1 from its original value so that it now points to the return value.</li>
<li>During the execution of your subroutine, you must make the correct number of calls to ABS and POW3, corresponding to the pseudocode.
– If the autograder claims that you are making an unknown subroutine call to some label in your code, it may be that your code has two labels without an instruction between them. Removing one of the labels should appease the autograder.

5 Deliverables

Turn in the following files on Gradescope during your assigned timed lab slot: 1. tl03.asm
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
6 Local Autograder

To run the autograder locally, follow the steps below depending upon your operating system: • Mac/Linux Users:

<ol>
<li>Navigate to the directory your homework is in (in your terminal on your host machine, not in the Docker container via your browser)</li>
<li>Run the command sudo chmod +x grade.sh</li>
<li>Now run ./grade.sh</li>
</ol>
• Windows Users:

<ol>
<li>In Git Bash (or Docker Quickstart Terminal for legacy Docker installations), navigate to the
directory your homework is in
</li>
<li>Run chmod +x grade.sh</li>
<li>Run ./grade.sh</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
Your code must assemble with NO WARNINGS OR ERRORS. To assemble your program, open the file with Complx. It will complain if there are any issues. If your code does not assemble, you WILL get a zero for that file.

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
<ol>
<li>Comment your code! This is especially important in assembly, because it’s much harder to interpret what is happening later, and you’ll be glad you left yourself notes on what certain instructions are contributing to the code. Comment things like what registers are being used for and what less intuitive lines of code are actually doing. To comment code in LC-3 assembly just type a semicolon (;), and the rest of that line will be a comment.</li>
<li>Avoid stating the obvious in your comments, it doesn’t help in understanding what the code is doing.</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
Good Comment

<pre>ADD R3, R3, -1
BRp LOOP
</pre>
Bad Comment

<pre>ADD R3, R3, -1
BRp LOOP
</pre>
</div>
<div class="column">
<pre>; counter--
; if counter == 0 don’t loop again
</pre>
<pre>; Decrement R3
; Branch to LOOP if positive
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<ol start="4">
<li>DO NOT assume that ANYTHING in the LC-3 is already zero. Treat the machine as if your program was loaded into a machine with random values stored in the memory and register file.</li>
<li>Following from 4., you can randomize the memory and load your program by going to File ¿ Advanced Load and selecting RANDOMIZE for registers and memory.</li>
<li>Use the LC-3 calling convention. This means that all local variables, frame pointer, etc., must be pushed onto the stack. Our autograder will be checking for correct stack setup.</li>
<li>The stack will start at xF000. The stack pointer always points to the last used stack location. This means you will allocate space first, then store onto the stack pointer.</li>
<li>Do NOT execute any data as if it were an instruction (meaning you should put HALT or RET instructions before any .fills).</li>
<li>Do not add any comments beginning with @plugin or change any comments of this kind.</li>
<li>You should not use a compiler that outputs LC3 to do this assignment.</li>
<li>Test your assembly. Don’t just assume it works and turn it in.</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column"></div>
</div>
</div>
<div class="page" title="Page 9">
<div class="layoutArea"></div>
</div>

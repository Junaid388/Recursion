# Recursion

recursion  /rɪˈkəːʃ(ə)n/

The repeated application of a recursive procedure or definition.

According to wikipedia "Recursion in computer science is a method of solving a problem where the solution depends on solutions 
to smaller instances of the same problem (as opposed to iteration). The approach can be applied to many types of problems, and 
recursion is one of the central ideas of computer science."

In general it is a process in which a function calls itself directly or indirectly. The corresponding function is called as 
recursive function. Using recursive algorithm, many of the problems can be solved quite easily. 
Examples of such problems are finding factorial of a number, Towers of Hanoi (TOH), Inorder/Preorder/Postorder Tree Traversals, DFS of Graph, etc.

Example: Towers of Hanoi (TOH) 

The Tower of Hanoi is a mathematical puzzle. It consists of three rods and a number of disks of different sizes, which can slide 
onto any rod. The puzzle starts with the disks in a neat stack in ascending order of size on one rod, the smallest at the top, 
thus making a conical shape.

The objective of the puzzle is to move the entire stack to another rod, obeying the following simple rules:

1. Only one disk can be moved at a time.
2. Each move consists of taking the upper disk from one of the stacks and placing it on top of another stack or on an empty rod.
3. No larger disk may be placed on top of a smaller disk.

With 3 disks, the puzzle can be solved in 7 moves. The minimal number of moves required to solve a Tower of Hanoi puzzle is 2^n− 1,
where n is the number of disks.

Source:wikipedia

In the program we are trying to solve the TOH problem using recursion. 

In the method we are assuming there are 3 rods for moving the disks and 1 rod is the base position(f) where all the disks are placed
at initial positon in asccending order. Next, We want to take a rod as the helper rod(h) which will help us to move the disks from 
initial positon (f) to final postion (t) via the helper rod. n is the number of disks We want to move.

Assume ther are  3 rods and we want to move 3 disks from(f) rod A to(t) rod C using the helper(h) rod C.

1. first we move the smaller disk from rod A to C.
2. move the medium disk from A to B.
3. move the smaller disk from C to B. (this is the smallest problem where you are moving only two disks from A to B moves taken 3)
4. move the larger disk from A to C.
5. move the smaller disk from B to A.
6. move the medium disk from B to C.
7. move the smaller disk from A to C.

The minimul number of moves required to move this disks form a rod to another rod is 2^n-1= 2^3-1= 8-1=7.

Using recurison we have solved the problem in minimum no. of steps and very effectively. Like this if there are N number of disks 
we can move them from one rod to another in a simple way.

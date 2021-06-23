# Intermediate-Code-Generation-Quadruple-Triple-Indirect-triple

Aim - 

To implement Intermediate code generation – Quadruple, Triple, Indirect triple

Algorithm –

The algorithm takes a sequence of three-address statements as input. For each three address statements of the form a:= b op c perform the various actions. These are as follows: 

Step 1 – Invoke a function getreg to find out the location L where the result of computation b op c should be stored. 
Step 2 – Consult the address description for y to determine y'. If the value of y currently in memory and register both then prefer the register y' . If the value of y is not already in L then 
generate the instruction MOV y' , L to place a copy of y in L. 
Step 3 – Generate the instruction OP z' , L where z' is used to show the current location of z. if z is in both then prefer a register to a memory location. Update the address descriptor of x to 
indicate that x is in location L. If x is in L then update its descriptor and remove x from all other descriptors. 
Step 4 – If the current value of y or z have no next uses or not live on exit from the block or in register then alter the register descriptor to indicate that after execution of x : = y op z those 
register will no longer contain y or z.

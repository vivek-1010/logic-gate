# logic-gate
VERILOG CODE
 BASIC LOGIC GATES AND: - AND, OR, NOT
module logic_gate(a,b,c ,d,e);
Input a,b;
Output c,d,e; // this statement is used only behiverol model
Reg c,d,e;
// we can direct write in a single statement output and reg
//Output reg c;
Always @ (a,b)
Begin
c=a&b;
d=a|b;
d=~a;  // d=!a  we can use it also in place of ~a.
end
endmodule



TESTBENCH




module tb();
reg a,b;
wire c,d,e;
integer i;
//uut is used for to connection of design part 
// uut means unit under test
Logic_gates uut(a,b,c,d,e);
Initial
Begin
{a,b}=0;
$display(“ A B  = AND , OR, NOT(A)”);
$monitor($time,”a=%b b=%b c=%b d=%b e=%b”,a,b,c,d,e);
for(i=0;i<=4;i=i+1)
Begin
{a,b}=i;
#5;
End
$finish;
End
endmodule








# MEALY_1101
# AIM
To stimulate and synthesis MEALY Sequence Detecor for 1101 using Vivado.

# SOFTWARE REQUIRED
vivado 2023.2 software.

# PROCEDURE
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table.
# STATE DIAGRAM
![image](https://github.com/RESMIRNAIR/MEALY_1101/assets/154305926/fce7c9dc-e0df-4528-843b-559bf24f018a)
# PROGRAM
module mealy1101 (x,z,clk,rst);

input x,clk,rst;

output reg z;

parameter s0=2'b00,s1=2'b01,s2=2'b10,s3=2'b11;

reg[1:0] PS,NS;

always@(posedge clk or posedge rst)

begin

if (rst)

PS<=s0;

else

PS<=NS;

end

always@(PS or x)

begin

case(PS)

s0: begin

z=0;

NS=x?s1:s0;

end

s1: begin

z=0;

NS=x?s2:s0;

end

s2: begin

z=0;

NS=x?s2:s3;

end

s3: begin

z=x?1:0;

NS=x?s1:s0;

end

endcase

end

endmodule
# OUTPUT:
![image](https://github.com/trishasailendran/MEALY_1101/assets/87655678/032b255b-1d63-4236-8249-267f9a7b3dff)

# RESULT:
Thus the verilog program for MEALY Sequence Detecor for 1101 has been simulated and verified successfully.


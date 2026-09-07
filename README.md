# smart-elevator-controller
A smart elevator control system for a multi-story building. The system prioritizes requests, handles multiple elevators, and optimizes waiting times based on the number of passengers and floors requested. The project is implemented in Verilog HDL and is verified using a testbench.
The elevator controller operates like an FSM where the system transitions between different states based on elevator availability, current positions, and incoming requests.
The system uses an always block triggered by the clock signal (posedge clk) to manage the request queue and update elevator positions.
A synchronous reset is used to initialize system variables such as elevator positions, queue pointers, and busy flags. 
A circular buffer is implemented to store up to 8 pending requests.
The elevator selection logic employs case statements to determine which elevator should serve the request, based on proximity and passenger count.


# Lecture 3 Exercises

### Simulation
- Write and run (fixing eventual bugs) the simulation for the example block design

## Fixed_timer_master
- Create a new module to interact with the one written as exercise 2, [Timer](../lec_2/exercises.md#Lecture%202%20exercises#Timer),  that will drive the latter.
	- It has a parameter: `TIMER_WIDTH`
	- It has the following ports
		- Sequential ports (clock and reset)
		- The ports to interact with Timer
		- Two channels (handshakes only) to interact with an external module
			- One to be activated
			- One to notify the completion
	- Skeleton:
```verilog
module fixed_timer_master # (
// TIMER_WIDTH parameter
) (
// Seqential ports
input wire activate_valid,
output wire activate_ready,
output wire done_valid,
output wire done_ready,
// Timer's interaction ports
);
// Logic
endmodule
```

- It will work with a fixed and hard-coded value for timer's `starting_value`
### Simulation
- Test the module in the previous section and verify in simulation it works as expected
	- Add as many internal wires and registers to the waveform as you please

## New module (parametric_timer_master)
- Create a new module cloning the one in the previous section, [fixed_timer_master](../lec_3/exercises.md#Lecture 3 Exercises#Fixed_timer_master)
- Add a new parameter that will be used instead of the fixed hard-coded value for timer's `starting_value`, called `TIMER_VALUE`
### Simulation
- Test the module in the previous section and verify in simulation it works as expected
	- Add as many internal wires and registers to the waveform as you please
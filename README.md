# Phased Array simulator

This is a code that can simulate phased arrays, written in Julia.
I wrote it in order to simulate an array of ultrasonic sensors, which I am building using a microcontroller.
The simulation works by simply adding waves (exp(ikr)) that travel radially outward from a source, in a 3D grid.
It used CUDA to accelerate the calculations using the GPU, and has an object-oriented structure.

To run a simulation, you first initialize it by creating an object of type 'SimulationWorld',
for example: sim = SimulationWorld(Ncells, ....).
Then, one can run the simulation using run(sim). The GPU makes these calculations lightning fast.

# Analog-PI-Cruise-Control
A fully analog closed-loop PI controller for DC motor speed regulation, designed and simulated in LTSpice. Achieves zero steady-state error with stable transient response.
The project aims to develop a cruise control system prototype using IC 741 op-amp, which 
maintains a constant DC motor speed through a closed-loop feedback mechanism. The set 
speed is given using a potentiometer, while the actual speed is sensed and compared with the 
reference to generate an error signal. Based on this error, the motor drive is automatically 
adjusted to keep the speed nearly constant even under varying load conditions. 

# What It Does
- Regulates DC motor speed using a PI (Proportional-Integral) controller.
- Implemented entirely with analog components - op-amps, resistors, capacitors.
- Closed-loop feedback eliminates steady-state error.
- Simulated transient response analysed for overshoot, settling time, and stability.

# Technical Highlights
- Controller IC: IC 741 Op-Amp (used as error amplifier/comparator). 
- Controlled Unit: 12V DC motor (acts as vehicle engine). 
- Set Speed Input: Potentiometer (manual speed setting). 
- Speed Feedback: Tachogenerator / IR sensor (speed-to-voltage conversion). 
- Driver Stage: Power transistor or MOSFET to supply motor current. 
- Control Type: Closed-loop negative feedback system. 
- Power Supply: ±12V for IC 741 and 12V for motor.
- Tool: LTSpice

# Controller Design
- Proportional stage:
Sets the gain of the error signal.
Faster response, but alone causes steady-state error.

- Integral stage:
Integrates accumulated error over time.
Eliminates steady-state error entirely.
RC time constant tuned for stability: `τ = R × C`

- Combined PI response- 
  Proportional: immediate correction;
  Integral: long-term accuracy

Result: smooth speed regulation with zero steady-state error



# Quad Motor Driver

The Quad Motor Driver board contains four DRV10970 BLDC motor driver ICs and is intended for driving the Faulhaber 1509 motors that spin HuskySat-2's reaction wheels. The motors are connected with eight-pin Molex Pico-Lock connectors.

### Use

The board contains two headers. The first contains labeled pins for ground and a 5V power input. The second contains PWM and direction control (FR) pins for each of the four motors. Each of the four motor driver subsystems has two solder jumpers. The lower-numbered jumper may be soldered closed to enable motor braking when the PWM signal is zero. If left unsoldered, the motor will coast. The higher-numbered jumper may be soldered closed to operate the motor with a sinusoidal signal. Otherwise, the motor will be driven with a trapezoidal signal. In our design, we plan to bridge both of these jumpers. Each motor driver subsystem also has two testpoints: the lower-numbered testpoint connects to the frequency indication (FG) signal and the higher-numbered testpoint connects to the lock indication (RD) signal.

### Notes

- The motor connector pinouts may or may not be backwards.

- R1 and R2 (and their equivalents on the other motor driver subsystems) may not be required if TP1 and TP2 are not used.

- R4, R5, and R6 (and their equivalents on the other motor driver subsystems) may not be required.

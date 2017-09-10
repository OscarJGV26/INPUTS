# INPUTS
This library has a class called INPUT which handles PWM signals going for servos and motors/ESCs in the system.

The begin function allows you to:/
  1. Specify a desired frequency for all the PWM signals. 
  2. Calibrate your ESCs at start with 1/0. (Careful with this... Do not test with propellers on!)

In the h file you can:/
  1.Define a number of servos/ESCs and their respective channel mapping. 
  The begin function will check that there are no repeated channels for servos/motors 
  and that the number of servos+motors doesn't exceed 8.
  2. Specify a desired range in us for both servos/ESCs (independently) and
  a range of angles that the write function accepts.
  3. Reverse a servo signal by changing the reverse_servo_angle variable.
  4. Offset servo angles. E.g. 90 degrees is actually 92-93. It is intended for fine tunning.

The write function receives 2 arrays with the motor signals (microseconds) and servo angles (degrees). 

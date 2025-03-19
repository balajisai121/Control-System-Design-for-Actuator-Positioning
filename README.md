Control System Design for Actuator Positioning
Introduction
This project focuses on designing and tuning control systems for actuator positioning in a medical device. The objective is to apply industrial control system simulations using MATLAB and SIMULINK to analyze system responses.

System Parameters
The actuator is modeled as a second-order mass-spring-damper system with the transfer function:

𝐺
(
𝑠
)
=
1
𝑚
𝑠
2
+
𝑏
𝑠
+
𝑘
G(s)= 
ms 
2
 +bs+k
1
​
 
where:

m = 10 kg (actuator mass)
b = 20 N/m/s (damping coefficient)
k = 100 N/m (stiffness)
Controller Design
Different controllers were designed and analyzed for system performance:

1. Proportional (P) Controller
Tuned Gain (Kp): Improves response speed but introduces steady-state error.
2. Proportional-Integral (PI) Controller
Gains (Kp, Ki): Reduces steady-state error but increases settling time.
3. Proportional-Derivative (PD) Controller
Gains (Kp, Kd): Enhances system stability and reduces overshoot.
4. Proportional-Integral-Derivative (PID) Controller
Gains (Kp, Ki, Kd): Achieves optimal performance by balancing speed and stability.
System Response Analysis
Each controller’s performance was evaluated based on:

Overshoot
Settling Time
Damping Classification (Underdamped, Overdamped, Critically Damped)
Tuning Strategy
A systematic approach was taken to optimize Kp, Ki, and Kd values by:

Iterating through different gain combinations
Analyzing response metrics
Selecting parameters with the best performance
MATLAB Results
Controller Performance Summary:
P Controller → 42.77% overshoot, 3.66s settling time (Underdamped)
PI Controller → 0% overshoot, 49.62s settling time (Overdamped)
PD Controller → 37.09% overshoot, 2.78s settling time (Underdamped)
PID Controller → 0% overshoot, 51.95s settling time (Overdamped)
Best Tuning Parameters Found:
Kp = 0.00, Ki = 20.00, Kd = 20.00
Best Performance: 0% overshoot, 18.57s settling time
SIMULINK Analysis
The system was simulated in Simulink with different controllers. Step response data was extracted to analyze performance.

Controller Design and Results
For each P, PI, PD, and PID controller, simulations were conducted to record:

Rise Time
Settling Time
Maximum Acceleration
Discussion and Conclusion
Results showed different trade-offs:
✅ Underdamped Controllers → Faster response, but higher overshoot and oscillations
✅ Overdamped Controllers → Minimal overshoot, but longer settling times
✅ Optimized PID Controller → Best balance between stability and speed

This project successfully demonstrated the importance of controller tuning in system performance optimization. Future work includes adaptive control strategies for enhanced precision. 

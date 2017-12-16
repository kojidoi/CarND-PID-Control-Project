# PID Controller Project

---

## Reflection

### Describe the effect each of the P, I, D components had in your implementation.

**P (proportional):**
performs control proportional to the error between the current position and the target position called cross track error (CTE).
If P is high, CTE can be decreased more quickly, but it causes big overshoot and vibration.

**D (Derivative):**
performs control proportional to the differential of CTE.
D has a role of suppressing the amount of change in steering angle.

**I (Integral):**
reduces steady CTE which PD control can not solve.


### Describe how the final hyperparameters were chosen.

I did manual parameter tuning.
My final parameter values are below:

|Parameter|Value|
|:---:|:---:|
|Kp|0.1|
|Ki|0.0001|
|Kd|3.0|

First, I tried several Kp parameters and found a value (0.1) that the car did not run off the track and did not overshoot.

Next, I adjusted Kd parameter. It seemed that there was no problem with the value (3.0) indicated in the lecture.

Finally I adjusted Ki. In this issue, the necessity of this component seemed not to be high, so I chose it a small value (0.0001).

With the above parameter settings, the car was able to run within the lane of the course.

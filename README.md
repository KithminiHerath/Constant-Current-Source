# Constant-Current-Source

The proposed project was to design a constant current source to charge a typical 12V lead acid battery by a constant current of 1A. All the typical lead acid battery chargers have the common issue of the high thermal energy dissipation and in this project our intention was to minimize this common issue as much as possible. To address this issue, a Pulse Width Modulated (PWM) signal was generated, which was used to switch a MOSFET and thus provide the required current and a feedback signal was sent to the PWM generator circuit to ensure a 1A constant current output to the load.

This project consists of 4 stages and they are:
* **Ramp generator circuit** - this will generate a ramp signal of 5KHz frequency, which will be fed into the next stage to generate a PWM signal.
* **Comparator Circuit** - this will compare the ramp signal generated in the first stage with a feedback signal (feedback voltage from the charging load) and create a PWM signal to drive the next atage.
* **Buck convertor** - the PWM signal generated in the previous stage was directed to a MOSFET which was used as a switch to supply the constant 1A current to the charging load.
* **Feedback signal amplification stage** - the voltage of a constant resistor in series with the charging load was used as a shunt resistor for an instrumentation amplifier to amplify the feedback signal. This signal was directed to stage 2 to generate the required PWM signal to ensure a constant current across the load until it has been completely charged.

At the end of the constant current charging of the load, the supply will be switched off.

The full circuit is shown below:

![image](https://github.com/KithminiHerath/Constant-Current-Source/blob/master/Images/Final-Circuit.png)

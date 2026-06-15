I intended to create this DC-DC-Boost-Converter as a hands-on opportunity to dive into power electronics, train my component selection skills, and sharpen my technical skills. 
It regulates a 10.5V input voltage to a 19V output through a 40% duty cycle operation.
It consists of two phases: MOSFET ON and MOSFET OFF


// 
When the MOSFET is ON, it acts as a closed switch, which provides the path from the inductor to ground, which stores energy. 
The selection of an appropriate diode is crucial to prevent the capacitor from discharging. 

///
When the MOSFET is OFF, it acts as an open switch, so no current passes through it;
The inductor will try to resist a change in current ( L = di/dt ), creating a back electromotive voltage which is received by the output capacitor.
The output capacitor receives both INPUT voltage + Inductor boost voltage


MOSFETs are excellent for DC-DC Converters, due to their customizable and fast on/off switching and precise power transfer. Its efficiency depends on switching, capacitor, and conduction losses.

To increase duty cycle, we can:

Increase the inductor value, reducing ripple - small AC variation that rides on top of the DC output ; ripple = Vin x Duty Cycle  / Frequency x Inductance

Increase the duty cycle;
Increase the switching frequency, as more energy will be transferred per cycle.

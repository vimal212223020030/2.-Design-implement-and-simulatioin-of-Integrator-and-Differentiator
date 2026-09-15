# 2.-Design-implement-and-simulatioin-of-Integrator-and-Differentiator
**AIM:**
To design , implement and simulate  an integrator and differentiator circuits

**APPARATUS  and SOFTWARE REQUIRED:**
S.No	Name of the Apparatus	Range	Quantity
1.	Signal Generator	3 MHz	1
2.	DSO	30 MHz	1
3.	Dual RPS	(0 – 30) V	1
4.	Op-Amp	µA741	1
5.	Bread Board		1
6.	Resistors	1K,10K,100K,	2
7.	Capacitors	0.1µF,0.01µF	1
8.	Connecting wires and probes	As required	
9.  LT SPICE software

**THEORY:**

**INTEGRATOR**
A circuit in which the output voltage waveform is the integral of the input voltage waveform is the integrator. Such a circuit is obtained by using a basic inverting amplifier configuration if the feedback resistor Rf is replaced by a capacitor Cf . The expression for the output voltage is given as,
Vo = - (1/Rf C1 ) ∫ Vi dt

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. Normally between fa and fb the circuit acts as an integrator. Generally, the value of fa < fb . The input signal will be integrated properly if the Time period T of the signal is larger than or equal to Rf Cf . That is,
T ≥ Rf Cf

The integrator is most commonly used in analog computers and ADC and signal-wave shaping circuits.

**DESIGN:**
 
To obtain the output of an Integrator circuit with component values R1Cf = 0.1ms , Rf = 10 R1 and Cf = 0.01 µF and also if 1 V peak square wave at 1000Hz is applied as input.
We know the frequency at which the gain is 0 dB, fb = 1 / (2π R1 Cf) Therefore fb = 	 Since fb = 10 fa , and also the gain limiting frequency fa = 1 / (2π Rf Cf)
We get , R1 =	and hence Rf = 	

**DIFFEERENTIATOR:**

The differentiator circuit performs the mathematical operation of differentiation; that is, the output waveform is the derivative of the input waveform. The differentiator may be constructed from a basic inverting amplifier if an input resistor R1 is replaced by a capacitor C1 . The expression for the output voltage is given as,
Vo = - Rf C1 ( dVi /dt )

Here the negative sign indicates that the output voltage is 180 0 out of phase with the input signal. A resistor Rcomp = Rf is normally connected to the non-inverting input terminal of the op-amp to compensate for the input bias current. A workable differentiator can be designed by implementing the following steps:
1.	Select fa equal to the highest frequency of the input signal to be differentiated. Then, assuming a value of C1 < 1 µF, calculate the value of Rf.
2.	Choose fb = 20 fa and calculate the values of R1 and Cf so that R1C1 = Rf Cf.

The differentiator is most commonly used in wave shaping circuits to detect high frequency components in an input signal and also as a rate–of–change detector in FM modulators.
 
**DESIGN (DIFFERENTIATOR):**

Design an op-amp differentiator that will differentiate an input signal with fmax = 100HZ Select fa = fmax = 100 HZ = 1 / 2πRFC1
Let C1 = 0.1μF
Then RF = 1 / 2π(102)(10-7)
= 15.9KΩ
Now choose fb = 10fa = 1 / 2πR1C1 Therefore, R1 = 1 / 2π(103)(10-7)
= 1.59KΩ Since RFCF = R1C1
We get, CF = (1.59*103*10-7) / 15.9*103
= 0.01μF


**PROCEDURE:**
1.	Connections are given as per the circuit diagram
2. + Vcc and - Vcc supply is given to the power supply terminal of the Op-Amp IC.
3.	By adjusting the amplitude and frequency knobs of the function generator, appropriate input voltage is applied to the inverting input terminal of the Op- Amp.
4.	The output voltage is obtained in the CRO and the input and output voltage waveforms are plotted in a graph sheet.

 
**INTEGRATOR:**
  **CIRCUIT DIAGRAM**
<img width="1152" height="864" alt="WhatsApp Image 2026-09-14 at 7 31 12 PM" src="https://github.com/user-attachments/assets/804362b1-e67d-4e5e-8534-1e3bb115586a" />


  **MODEL GRAPH:**
<img width="1280" height="1087" alt="WhatsApp Image 2026-09-14 at 7 31 37 PM" src="https://github.com/user-attachments/assets/16c12242-ef76-4dbb-b9e3-a9370ad8207a" />
<img width="1152" height="864" alt="WhatsApp Image 2026-09-14 at 7 31 19 PM" src="https://github.com/user-attachments/assets/50a51ee1-61a7-4466-b2e2-5f7863a0bfe8" />


  **TABULATION:**
 <img width="1040" height="780" alt="WhatsApp Image 2026-09-14 at 7 35 06 PM" src="https://github.com/user-attachments/assets/7b46820b-2dcf-4fc3-a2e9-61967f183ab0" />


**GRAPH:**  

<img width="864" height="1152" alt="WhatsApp Image 2026-09-14 at 7 37 15 PM" src="https://github.com/user-attachments/assets/65acadd0-ce7b-46bc-8a21-692f89f3608a" />

**DIFFERENTIATOR:**
  **CIRCUIT DIAGRAM**
  
<img width="1040" height="716" alt="image" src="https://github.com/user-attachments/assets/a18ecc84-7126-47d3-a1f4-9d2dfa6037c6" />


  **MODEL GRAPH:**
<img width="1280" height="631" alt="image" src="https://github.com/user-attachments/assets/d21a6c69-9bd8-4af4-b1de-d7cf240e8862" />
<img width="1280" height="1064" alt="image" src="https://github.com/user-attachments/assets/e448b6d7-2563-4fae-bebb-a5bf8d2ffda6" />



  **TABULATION:**

 <img width="1280" height="878" alt="image" src="https://github.com/user-attachments/assets/ecb7c52f-5e52-4635-9866-e49c7efbc409" />
  **GRAPH:** 
  

  <img width="780" height="1040" alt="image" src="https://github.com/user-attachments/assets/75cf1469-1ade-4320-a0b8-0080db51e932" />


**LT-SPICE Tool:PROCEDURE:**
•	Double click on LT-Spice icon.
•	New schematic window open.
•	Pick and paste the required component from the library and draw the circuit diagram .
•	Complete the connection.
•	Save the file by giving file name.
•	Click on the run option ->click advanced open ->select Ac analysis->enter the amplitude time delay stop time value.
•	Click on the run option ->simulation window opens->place the probe ->output graph is obtained.
 
  **LT SPICE**
  **INTEGRATOR CIRCUIT and Waveform**
  **SINE WAVE:**
  <img width="1280" height="680" alt="WhatsApp Image 2026-09-14 at 7 46 33 PM" src="https://github.com/user-attachments/assets/09057b18-7b53-4a08-accb-73234b985b2b" />
  **SQUARE WAVE:**
  <img width="1280" height="680" alt="WhatsApp Image 2026-09-14 at 7 46 49 PM" src="https://github.com/user-attachments/assets/2e2bda04-757a-4bb7-94a1-cd05bfbbdfe3" />
  **DIFFERENTIATOR CIRCUIT and Waveform**
  **SINE WAVE:**
  <img width="1280" height="680" alt="WhatsApp Image 2026-09-14 at 7 50 17 PM" src="https://github.com/user-attachments/assets/3258c007-56f3-4ab6-9975-6dc72e9613d5" />

  **SQUARE WAVE:**
  <img width="1280" height="680" alt="WhatsApp Image 2026-09-14 at 7 50 02 PM" src="https://github.com/user-attachments/assets/9134c104-5cfd-4537-9875-e305b396a321" />


**RESULT:**
Thus the Integrator and Differentiator are designed and simulated performance was successfully tested using op-amp IC 741 and LT SPICE.

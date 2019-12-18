# Fuel Trim as Engine Insight and Diagnostic Tool 
The main thing an engine acomplishes is mixing air and fuel, then at the right moment igniting that mixture in order to turn the crankshaft. In order to ignite, the correct [stoichiometric ratio](https://en.wikipedia.org/wiki/Air%E2%80%93fuel_ratio) is the goal. For gasoline that ratio is 14.7 parts air to 1 part fuel. The vehicle's computer is going to be very obsessed with achieving this ratio. Since the engine does not have a lot of control over how much air is entering the combustion chamber, the strategy in general is to measure the incoming air, the exiting exhaust, and adjust the miliseconds of time it activates the fuel injectors depending on those measurements.


## Understanding Fuel Trim
A vehicle’s computer system uses Fuel Trim to maintain the ideal air/fuel ratio for complete combustion. Reading the fuel trim can provide an overall picture of engine health or what might be causing the a problem such as an intake manifold vacuum leak (positive fuel trim – lean) or a stuck open fuel injector (negative fuel trim – rich).


## Short Term Fuel Trim
Short Term Fuel Trim (bank one: STFT1 and bank two: STFT2) is the computer’s immediate response to adjust the air/fuel ratio. The #1 thing short term fuel trim is used to accomplish is to reach stoichiometry.
In positive corrections, fuel is added to adjust for a lean condition, while negative corrections respond to a rich condition. STFT corrections represent the current engine run cycle and react very quickly to Oxygen Sensors (O2 sensors) sensor input. If you were to create a large vacuum leak at idle by disconnecting the Positive Crankcase Ventilation (PCV) hose, the computer would immediately add positive fuel trim to balance the mixture because more unmeasured air is entering the system and causing the O2 sensors to read unburnt air. Short Term Fuel Trim is not stored in Keep Alive Memory (KAM) after shut down and automatically resets to 0 for the next start/run cycle.


## Long Term Fuel Trim
Unlike STFT, Long Term Fuel Trim (bank one: LTFT1 and bank two: LTFT2) is learned over time while in closed loop operation. It is stored in the KAM and used for open loop fuel calculations (like start up and wide-open throttle). LTFT is a coarser adjustment and also works to keep STFT within specification. A vehicles LTFT may be different at idle than at eighty-eight miles per hour; the computer will remember and use different LTFTs for different situations in what is called a [Fuel Map](/fuelmap).


## Catalytic Converters and Emmisions
A Catalytic Converter (Cat) can clear some pollutiants in a rich condition, and other polutiants in a rich condition. Modern three-way catalytic converters need the air-to-fuel ratio to be constantly driven rich/lean in order to work at maximum efficiency. For this reason, the computer ocilates between slightly rich and slightly lean. O2 sensors in the exhaust are used to detect and confirm these normal rich/lean fluctuations.


## Oxygen sensors
Oxygen sensors (O2) are the primary feedback sensor to the fuel system. They report to the computer about how much oxygen is passing through the exhaust. The assumption is that if there is too much oxygen, there must not be enough fuel being burnt to achieve a perfect air/fuel ratio.


### Air/Fuel Ratio Sensors
Some modern cars have are fuel ratio sensors (AFR) which work similiar to O2 sensors but have many differences. Often these are called "Wide Band O2 Sensors" because they detect a much broader range. Another major difference is that they output their measurements in microamps which can be difficult to measure with standard multimeters.


# Diagnosis with Fuel Trims
Fuel trims can give you direction and help zero in on a problem, especially when there are no trouble codes present or multiple common causes for a trouble code. Knowing whether a vehicle is running too rich or too lean will help narrow down your diagnosis. Fuel trims that differ greatly from one-cylinder bank to the other right direction. It is recomended to evaluate fuel trims at idle and at 2500 RPM. A useful test is to "snap the thottle" meaning to apply open throttle quickly for a short period and return to idle, the resulting STFT and LTFT pattern can then be inspected for normality.


### Lean condition:
When you see a negative LTFT, the engine is calling for less fuel.
At around -20% the computer will throw a lean code (bank one: P0171 | bank two: P0174)

Could be caused by any of the following: this is a list of things to check, not replace

- Fuel pressure, too high or out of specifications
- Dirty Mass Air Flow sensor (MAF)
- Inaccurate Mass Air Flow sensor (MAF)
- Inaccurate Intake Air Temperature Sensor Testing (IAT)
- Vacuum leak
- Clogged or dirty Air Filter
- Inaccurate Oxygen Sensor readings (O2)
- Power-train Control Module (PCM)
- Throttle Position Sensor (TPS)
- Air injection system
- Exhaust leak
- Exhaust Gas Recirculation open (EGR)
- Manifold Absolute Pressure sensor (MAP)
- Misfire
- Injectors and seals
- Evaporative Emission Control (EVAP)
- Idle Air Control Valve (IAC)
- Air intake turbulence / Aftermarket air intake


### Rich condition:
When you see a positive LTFT, the engine is calling for more fuel.
At around 20% the computer will throw a lean code (bank one: P0170 | bank two: P0173)

Could be caused by any of the following: this is a list of things to check, not replace

- Injectors stuck open or leaking
- Fuel pressure, Not enough to meet demand of injectors
- 
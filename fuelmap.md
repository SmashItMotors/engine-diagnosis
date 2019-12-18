As you know, the vehicles computer remebers to use different fuel trims for different situtations. We can think of a fuel map as matrix of cells. On one axis the Rotations Per Minute (RPM) and on the other engine load.

{{image}}

Like the LTFT, the map is updated over time, so there is also a time axis but we can safely ignore this except in the most extreme diagnosic cases. It is worth noting however that many vehicles may have never experienced some parts of the fuel map that we may be exploring while diagnosing. For example not many people reach 3000 RPM with 0 load but that's something that may occuring while testing prolonged Wide Open Throttle durring data collection. After a change, the vehicle may exhibit surges or hesitations as it moves through the fuel map and reconciles it's old learned trims with the new (hopefully fixed) reality. During Wide Open Throttle there is no feedback from the O2 sensors and the ECU will be more reliant on the fuel map.

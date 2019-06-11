# EZ-127k
Reverse engineering of Audi Ignition system


# Pinout
- Pin 1 - Connected to 18, 19  - Contact/Conector in dash - Coding plug
- Pin 2 - Altitude sensor power
- Pin 3 - Diagnostic K-line               
- Pin 4 - 10V Feed to Hallsender (Distributor)
- Pin 5 - KE-jetronic pin 1   (Knock, Load)? LOAD   (Low voltage)
- Pin 6 - 12V Main supply           
- Pin 7 - Idle throttle switch
- Pin 8 - KE-jetronic  pin 21 (Knock, Load)? KNOCK 
- Pin 9 - Full throttle switch
- Pin 10 - GND (Hall sender)
- Pin 11 - N/A
- Pin 12 - GND / Shield Knock
- Pin 13 - Knock sender signal
- Pin 14 - Fuelpump Relay    
- Pin 15 - N/A         
- Pin 16 - Ignition stage
- Pin 17 - RPM signal to KE-jetronic pin 30 och Speedometer         
- Pin 18 - Connected to 19, 1 -  Coding plug
- Pin 19 - Connected to 18, 1 -  Coding plug
- Pin 20 - Signal GND
- Pin 21 - Highside Airflow meter   (Power check Signal flowmeter?)
- Pin 22 - Power GND
- Pin 23 - N/A
- Pin 24 - Hall sender signal
- Pin 25 - Coolant temp sensor

# Map

Maps on adress
- 0x1E80
- 0x3E80
- 0x5E80
- 0x7E80

Maps lite peculiar, wrapped between col 4 and 5, so 1-3 is low rpm. 5 is max rpm. 
Therefore maps looks odd when put in in a 3D graph.
Col 9 is around 3k rpm

Code repeated 2 times in bin, only second is used.

0x4000 Program start
0x552E Program end

0x5B00 Parametrar
0x5FF0 Parametrar ends

0x6000 Repeated program here
0x752E Program end

0x7B00 Parametrar
0x7FF0 Parametrar ends

Mappar @
0x7D70 - 0x7DEF 8x16
0x7DF0 - 0x7E5F 7x16
0x7E70 - 0x7EEF 8x16
0x7EF0 - 0x7F5F 7x16

16bits value @
0x7B00 - 0x7B1E  15bytes

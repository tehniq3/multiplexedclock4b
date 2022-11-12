# multiplexedclock4b
based on https://github.com/tehniq3/multiplexedclock4

actual schematic: https://github.com/tehniq3/multiplexedclock4b/blob/main/schema_ceas_multiplexat_reglaj_dioda_LDR_2022.png

<img src="https://github.com/tehniq3/multiplexedclock4b/blob/main/schema_ceas_multiplexat_reglaj_dioda_LDR_2022.png" width=50% height=50%>

<img src="https://github.com/tehniq3/multiplexedclock4b/blob/main/12h_format.png" width=50% height=50%>



ver.4.7 - change DHT sensor with 1N4148 diode

ver.4.7.x - variable for no sensor or diode / LDR (photodiode) + n changes in menus if buton for MENU remain pushed

ver.4.8 - if is night, show just clock

ver.4.8a - date and year display less than the others

ver.4.9 - set 12 or 24 hour format

ver.4.9a - increase time for display the time, in the night i just clock and temperature not date


int digit1 =  3; //PWM pin for control digit 1 (left side)

int digit2 =  5; //PWM pin for control digit 2

int digit3 = 10; //PWM pin for control digit 3

int digit4 = 11; //PWM pin for control digit 4 (right side)

int segA =   9; // pin for control "a" segment

int segB =  12; // pin for control "b" segment

int segC =  A0; // pin for control "c" segment

int segD =   4; // pin for control "d" segment

int segE =  A1; // pin for control "e" segment

int segF =   8; // pin for control "f" segment

int segG =   7; // pin for control "g" segment

int segDP = 13; // pin for control decimal point

#define DIODA A7  // pin for conect 1N4148 diode and GND
                  // (+5V---10k---A7--|>|--GND)      
                  
#define BTN1 A2   // pin for MENU/change  (A2---BTN1---GND)

#define BTN2 A3   // pin for increase value + (A3---BTN2--GND)

#define sound 6 // pin for control alarma (BUZZER---GND)

#define LDR A6  // pin for photoresistor (+5V---LDR---A6--10k---GND)                 

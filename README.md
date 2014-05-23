SitStandData
============

A microcontroller-based data logger for my sit-stand desk

Check out:
https://learn.adafruit.com/trinket-fake-usb-serial/install-for-linux-slash-mac
https://learn.adafruit.com/trinket-ultrasonic-rangefinder
http://arduino.cc/en/Tutorial/Ping
http://www.robot-electronics.co.uk/htm/arduino_examples.htm#SRF02,%20SRF08,%20SRF10,%20SRF235




  // establish variables for duration of the ping, and the distance 
  // result in inches and centimeters.
  duration = 0;
  inches = 0;
  cm = 0;
 
  // The PING))) is triggered by a HIGH pulse of 2 or more microseconds.
  // Give a short LOW pulse beforehand to ensure a clean HIGH pulse:
  pinMode(sonar, OUTPUT);
  digitalWrite(sonar, LOW);
  delayMicroseconds(2);
  digitalWrite(sonar, HIGH);
  delayMicroseconds(5);
  digitalWrite(sonar, LOW);
 
  // The same pin is used to read the signal from the PING))): a HIGH
  // pulse whose duration is the time (in microseconds) from the sending
  // of the ping to the reception of its echo off of an object.
  pinMode(sonar, INPUT);
  duration = pulseIn(sonar, HIGH);
 

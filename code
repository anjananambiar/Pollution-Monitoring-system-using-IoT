#include <dht.h> 
#include <LiquidCrystal_I2C.h>
#include "MQ135.h"
#define ANALOGPIN A2   
#define RZERO 206.85    //  RZERO Calibration Value
MQ135 gasSensor = MQ135(ANALOGPIN);
LiquidCrystal_I2C lcd(0x27, 16,2);
dht DHT; //Declaring the DHT as a dht type to use it later
#define DHT22_PIN 7 //pin defined

void setup()
{
lcd.begin (16,2);
 	lcd.backlight();
lcd.setBacklight(HIGH);
 	lcd.home ();
 	lcd.init(); 
Serial.begin(9600);
 	float rzero = gasSensor.getRZero();
  	delay(3000);
 	Serial.print("MQ135 RZERO Calibration Value : ");
  	Serial.println(rzero);
}
 
void loop()
{
 	 int sensorValue = analogRead(A0);     // print out the value you read:
 	 Serial.print("carbon monoxide:");
  	Serial.println(sensorValue);
  	delay(1000);   
  	lcd.clear();
  	lcd.setCursor(0,0);
  	int chk = DHT.read22(DHT22_PIN);      //Reading data from the module
  	float t= DHT.temperature*(9/5) + 32;  //Converting Celsius to Farenheit
 	lcd.print("Temp: ");
  	lcd.print(t); //Showing temperature value in Farenheit
  	lcd.print(" F");
  	lcd.setCursor(0,1);
  	lcd.print("Humidity: ");
 	lcd.println(DHT.humidity); //Showing humidity percentage
  	lcd.print(" %");
  	Serial.print("temp:");
  	Serial.println(t);
  	Serial.print("humidity:");
  	Serial.println(DHT.humidity);
  	delay(2000); 
  	float ppm = gasSensor.getPPM();
  	delay(1000);
  	Serial.print("pollution in ppm : ");
  	Serial.println(ppm);
  	lcd.setCursor(0,0);
  	lcd.print("POLL.IN.PPM");
  	lcd.setCursor(0,1);
  	lcd.print("AIR QUA: ");
  	lcd.print(ppm);
  	lcd.print("PPM");
  	delay(2000); 
}

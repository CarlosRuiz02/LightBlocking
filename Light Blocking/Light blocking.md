## Light blocking

Este módulo fotointerruptor para Arduino (compatible con otros microcontroladores), activará una señal cuando se bloquee la luz entre la brecha del sensor. Consta de un emisor/detector óptico en la parte frontal y dos resistencias (1kΩ y 33Ω) en la parte posterior. El sensor utiliza un haz de luz entre el emisor y el detector para verificar si la ruta entre ambos está bloqueada por un objeto opaco. Útil en aplicaciones como interruptor de final de carrera entre otras.

Hardware utilizado en este tutorial:

*1 x ESP-WROOM-32 Dev Module
*1 x Micro USB Cable
*1 x Protoboard
*4 x Cables hembra
*2 x Cables macho

## Diagrama

## Código
```
int LedOutput = 5;// Define as LED Output Pin 12 you can change this to 13 if you dont use pin 12 as output indicator
int SensorPin = 15; // Define as Sensor Pin Input
int Value;// Define as variable 
void setup()
{
pinMode(LedOutput,OUTPUT);//Set as LedOutput
pinMode(SensorPin,INPUT);//Set as photo interrupter sensor output interface
}
void loop()
{
Value=digitalRead(SensorPin);// Set as sensor read SensorPin 
if(Value==HIGH) //If value is equal to HIGH estate then turn LED output = high
{
digitalWrite(LedOutput,HIGH); // Set LedOutPut to HIGH or ON
}
else
{
digitalWrite(LedOutput,LOW); // Set LedOutPut to LOW or OFF
}
}```
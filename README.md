# servo-motor-using-Arduino
 We are going to run a servo motor using Arduino

the connection should be something like this
![image](https://user-images.githubusercontent.com/108229185/181568347-05e0eafd-d54c-429b-af13-d64b901262e2.png)
## the black wire on the ground.

## red wire 5v.

## the third wire you can connect it with any pin, in my example it was pin 11

# to create a servo object to control a servo and variable to store the servo position
``` 
#include <Servo.h>


Servo myservo;  
int pos = 0;    
```
now attach the servo on pin 11 to the servo object
```

void setup() {

  myservo.attach(11);  

}
```
we are going to use for loop to goes from 0 degrees to 180 degrees, by using "Write" we tell servo to go to position in variable 'pos'. using "delay" to waits 10ms for the servo to reach the position.
```
void loop() {

  for (pos = 0; pos <= 180; pos += 1) { 

    myservo.write(pos);              
    delay(10);                      
  }
  ```
  using for loop to move from 180 degrees to 0 degrees, tell servo to go to position in variable 'pos'. waits 10ms for the servo to reach the position
  ```
  for (pos = 180; pos >= 0; pos -= 1) { 
  myservo.write(pos);              
  delay(10);                       // waits 15ms for the servo to reach the position

}

}
```
## Brushless-motor-using-Arduino
connection should be like this
![image](https://user-images.githubusercontent.com/108229185/181569879-dc813dd4-20a4-4d84-aaa3-c658492b1417.png)
the code
```
void setup()
{
   pinMode(13, OUTPUT);
   pinMode(12, OUTPUT);
  
}
void loop()
{
  digitalWrite(13, HIGH);
  digitalWrite(12, LOW);
}
```

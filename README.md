# Conditionals2
Lesson 4/11
#make the RGB LED be able to cycle through 7 colors based upon the potentionmeter.


int wiperPin = A0;
int knobValue= 0;
int redPin=-9;
int greenPin=-10;
int bluePin=-11;

void setup() {
  pinMode(wiperPin, INPUT);
  pinMode(redPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
  pinMode(bluePin, OUTPUT);
}

void loop() {
 knobValue= analogRead(wiperPin);

 if(knobValue<148) {
  digitalWrite(redPin, HIGH);
  digitalWrite(greenPin,HIGH);
  digitalWrite(bluePin, LOW);
 }
 else if(knobValue>296) {
  digitalWrite(redPin, HIGH);
  digitalWrite(greenPin,LOW);
  digitalWrite(bluePin, HIGH);
 }
 else if(knobValue>444) {
  digitalWrite(redPin, LOW);
  digitalWrite(greenPin,HIGH);
  digitalWrite(bluePin, HIGH);
 }
 else if(knobValue>592) {
  digitalWrite(redPin, HIGH);
  digitalWrite(greenPin,LOW);
  digitalWrite(bluePin, LOW);
 }
 else if(knobValue>740) {
  digitalWrite(redPin, LOW);
  digitalWrite(greenPin,LOW);
  digitalWrite(bluePin, HIGH);
 }
 else if(knobValue>888) {
  digitalWrite(redPin, LOW);
  digitalWrite(greenPin,HIGH);
  digitalWrite(bluePin, LOW);
 }
 else {
  digitalWrite(redPin, LOW);
  digitalWrite(greenPin,HIGH);
  digitalWrite(bluePin, LOW);
 }
}

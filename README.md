# EECIT-P1
// Define pin numbers
const int buttonPin = 2; // Push button connected to digital pin 2
const int ledPin = 3; // LED connected to digital pin 3
void setup() {
 pinMode(buttonPin, INPUT); // Set pin 2 as INPUT to read button state
 pinMode(ledPin, OUTPUT); // Set pin 3 as OUTPUT to control the LED
 Serial.begin(9600); // Start Serial Monitor communication at 9600 baud
}
void loop() {
 int buttonState = digitalRead(buttonPin); // Read the current state of the button
 if (buttonState == HIGH) { // If button is pressed (input is HIGH)
 digitalWrite(ledPin, HIGH); // Turn the LED ON
 Serial.println("Button Pressed - LED ON"); // Print message to Serial Monitor
 } else {
 digitalWrite(ledPin, LOW); // Turn the LED OFF if button is not pressed
 Serial.print
 }
 delay(100); // Wait for 100 milliseconds to reduce noise (debounce effect)
}

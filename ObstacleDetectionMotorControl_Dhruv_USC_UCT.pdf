#define TRIG 9
#define ECHO 10
#define MOTOR 7

long duration;
int distance;

void setup() {
  pinMode(TRIG, OUTPUT);
  pinMode(ECHO, INPUT);
  pinMode(MOTOR, OUTPUT);

  digitalWrite(MOTOR, LOW);

  Serial.begin(9600);
}

void loop() {

  digitalWrite(TRIG, LOW);
  delayMicroseconds(2);

  digitalWrite(TRIG, HIGH);
  delayMicroseconds(10);

  digitalWrite(TRIG, LOW);

  duration = pulseIn(ECHO, HIGH);

  distance = duration * 0.034 / 2;

  Serial.print("Distance: ");
  Serial.print(distance);
  Serial.println(" cm");

  if (distance > 0 && distance < 20) {
    digitalWrite(MOTOR, LOW);
    Serial.println("Obstacle Detected -> Motor OFF");
  }
  else {
    digitalWrite(MOTOR, HIGH);
    Serial.println("Path Clear -> Motor ON");
  }

  delay(500);
}
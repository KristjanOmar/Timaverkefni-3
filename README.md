# Tímaverkefni 3

## 1.

### Myndband

https://user-images.githubusercontent.com/117899282/227205381-618dc073-901a-4411-843a-7ce3e4be99f5.mp4

### Kóði

```cpp
int raudur = 6;
int graenn = 5;
int blar = 3;

void setup() {
  pinMode(raudur, OUTPUT);
  pinMode(graenn, OUTPUT);
  pinMode(blar, OUTPUT);
}

void loop() {
  int sensorValue = analogRead(A0);
  int birta = map(sensorValue, 0, 1023, 255, 0);

  analogWrite(raudur, birta);
  analogWrite(graenn, birta);
  analogWrite(blar, birta);
}
```

## 2.

### Myndband



### Kóði

```cpp
int led1 = 11;
int led2 = 10;
int led3 = 9;
int led4 = 6;
int led5 = 5;
int led6 = 3;

int styrkur = 0;
int bid = 0;

void setup() {
  randomSeed(0);

  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(led5, OUTPUT);
  pinMode(led6, OUTPUT);
}

void loop() {
  styrkur = random(100,255);

  analogWrite(led1, styrkur);
  analogWrite(led2, styrkur);
  analogWrite(led3, styrkur);
  analogWrite(led4, styrkur);
  analogWrite(led5, styrkur);
  analogWrite(led6, styrkur);

  bid = random(50,150);
  delay(bid);
}
```

## 3.

### Myndband



### Kóði

```cpp
const int raudur = 11;
const int graenn = 10;

int styrkur = 0;
int bid = 0;

void setup() {
  randomSeed(9);
  pinMode(raudur, OUTPUT);
  pinMode(graenn, OUTPUT);
  pinMode(blar, OUTPUT);
}

void loop() {
  styrkur = random(200, 255);
  analogWrite(raudur, styrkur);
  bid = random(150, 250);
  delay(bid);
  styrkur = random(60, 90);
  analogWrite(graenn, styrkur);
  bid = random(150, 250);
  delay(bid);
}
```
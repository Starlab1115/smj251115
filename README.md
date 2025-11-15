# 으아아아아아아아아아아아아아아아아아아아아아아두이노(선민재)
**버튼을 누르면 *LED*색깔이 무작위로 바뀝니다.**
![image](./image.jpeg)
*코드* 
```
void setup() {
  pinMode(2, OUTPUT);
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
  pinMode(8, INPUT);
}

void loop() {
  int a;
  int botton = digitalRead(8);

  if (botton == 1) {
    a = random(0, 7);
    colors(a);
  }
  digitalWrite(10, 0);
  delay(1000);
}

void colors(int a) {
  if (a == 0 or a == 3 or a == 4 or a == 6) {
    digitalWrite(2, 1);
  } else {
    digitalWrite(2, 0);
  }

  if (a == 1 or a == 3 or a == 5 or a == 6) {
    digitalWrite(3, 1);
  } else {
    digitalWrite(3, 0);
  }

  if (a == 2 or a == 4 or a == 5 or a == 6) {
    digitalWrite(4, 1);
  } else {
    digitalWrite(4, 0);
    }
} 
```

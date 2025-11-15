# 으아아아아아아아아아아아아아아아아아아아아아아두이노(선민재)
**버튼을 누르면 *LED*색깔이 무작위로 바뀝니다.**                                                                      
나오는 LED 색깔은 약한 빨간색, 파란색, 초록색, 초록색 + 파란색이 있습니다. 빨간색은 거의 안나옵니다. ㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠ
![image](./image.jpeg)
이 작품은단지 전구 하나와 버튼 한 개, 저항 한 개와 전선9개만 있으면 만들 수 있습니다.
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

  if (botton == 1) { // 버튼 누름 감지
    a = random(0, 7); // 랜덤한 색 저장
    colors(a); // 랜덤한 색 발광
  }
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

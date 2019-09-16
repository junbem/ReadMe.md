1.
브래드에 저항과 조도센서를 연결하고 아두이노에서 A0, GND와 5V에 연결한 후, 아래 
2번을 아두이노에 들어가서 먼저 코딩한 후 업로드를 하고, processing에 들어가서 3번을 코딩한 후 아두이노를 컴퓨터에 연결해서 조도센서를 가리지 않을 때는 초록빛이 가리면 빨간빛이 들어오게 했습니다. 

2.
void setup() {
  Serial.begin(9600);
}
int a;
void loop() {
  a = analogRead(A0);
  Serial.println(++a);
  delay(500);
}
 
3. 
import processing.serial.*;
Serial p;
void setup(){
  size(300,300);
  p=new Serial(this, "COM6", 9600);
}
void draw(){
  if(p.available()>0){
    String m=p.readString();
    int a = int(m.trim());
    println(a);
    if(a>250) fill (0,255,0);
    else      fill (255,0,0);
    ellipse(150,150, 200, 200); 
   }
}

소감

아두이노가 너무 재밌습니다. 아두이노를 코딩하고 설계하고 그 결과를 보면서 뿌듯함과 신기함이 몰려와서 너무 좋았습니다. 다음 아두이노 시간이 너무 기다려 집니다. 매우 유익한 수업이 되고 있는 것 같습니다. 이 수업을 즐겁게 해주시는 심재창 교수님 감사합니다.

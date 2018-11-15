오늘부터 약 2주간 프로세싱에 대한 기본 강좌를 몇회에 걸쳐 진행하려 합니다.



그 중 오늘은 첫번째 시간으로 프로세싱의 문법과 좌표, 점과 선에대해 강의하려합니다.

 

프로세싱과 아두이노를 동시에 제어하기 위해선, 프로세싱과 친해져야 합니다.





임베디드 마이크로콘트롤러의 C언어 기본 형식은 main과 while로 이루어져 있죠.

main 에서 기본적인 마이컴 환경 Setting을 하고 전원이 제거 되기 전 까지 while문 안에서 무한 루프를 수행하도록 일반적으로 코딩합니다.



아두이노 역시 main과 while로 이루어 져 있지만, 스케치안에서는 main이 setup으로 while이 loop로 비 공학자들이 사용하는 언어로 변경되어 있습니다.


 



이 프로세싱에서는 while 이 draw로 이해하면 됩니다.







즉, 아래의 형식이 되겠죠?

void setup()



{



  ;



}



 



void draw()



{

  ;

 }



본인이 사용할 디스플레이 창을 만들기 위해선, size 함수를 사용해야 합니다.



size(x,y);



이때, x는 넓이 , y는 높이의 픽셀 정보를 입력해야 합니다.

본인이 사용하고자 하는 크기의 스케치북을 만든다라고 생각하면 되겠네요.

참고로, 픽셀은 본인 모니터의 해상도에 따라 달라 질 수 있습니다.



제 모니터는 2560 * 1080 (wide)이므로, 이정도의 픽셀이 존재하고, 구현할 수 있습니다.

size(2560,1080); 이라고 입력하면 모니터를 가득 채우게 됩니다.





다음엔, 배경 색을 칠하는 것에 대해 알아봅시다.

이때 사용하는 함수는 background 입니다.

background에 사용되는 인자는 하나만 사용하거나, 3개를 사용할 수 있습니다.



▪background(흑백)


▪background(적, 녹, 청)

흑백의 경우는 (0~255) 사이의 숫자 정보를 입력하면 됩니다.
0이면, 검정이고 255이면 흰색이 되겠네요

적녹청(RGB)의 경우는 각각의 색을 혼합하여 사용하면 됩니다. 색에 대해선 다음시간에 다시 말씀드릴께요









이어서, 도형 그리기 중 포인트와 선에대해 알아봅시다.



포인트는 말그대로, 점을 찍는 것이다. 가령 내가 size(300,200)인 도화지에, 정 가운데인 150, 100인 곳에 점을 찍는다라고 가정합시다.

이런... 이렇게 하기 위해선, 좌표계에 대한 설명이 앞서야 될것 같네요

우린 아래와 같은 직교좌표계에 익숙합니다.



​

하지만, 우리가 Processing에서 사용해야할 좌표계는 불행히도 아래와 같습니다.

이것도 처음엔 어색해도 하루 이틀이면 익숙해 질것입니다.. 처음이 어렵습니다.


그럼.. 본론으로 돌아와서 내가 내가 (20,20) 인 지점에 점을 찍고 싶다면.. point(20,20) 이렇게 하면 됩니다.





프로세싱으로 돌아가서,

size(300,200)인 창을 만들고, 정 가운데인 150, 100인 곳에 점을 찍어봅시다.







점이 찍힌것을 알 수 있습니다. 하지만 너무 작습니다.

이때 필요한 함수가 strokeWeight() 입니다.

크게 하고자 하는 픽셀 만큼 수치를 넣으면 됩니다.



 



다음으로 알아 볼것은 선(line) 입니다.. 선을 그리기 위해선 line()함수를 사용하면 됩니다.



line 함수는 4개의 인자를 받습니다.

line(첫번째 점의 x 값, 첫번째 점의 y값, 두번째 점의 x값, 두번째 점의 y값)







다음엔, 사각형과 원에 대해 알아 보도록 하겠습니다.
[출처] 프로세싱 - 그림 그리기(1)|작성자 IoT


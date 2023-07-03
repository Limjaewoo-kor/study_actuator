# study_actuator

Actuator / Micrometer / Prometheus / Grafana / Metrics


실제 구성한 그라파나의 캡처 이미지는 아래와 같다. 


![그라파나1](https://github.com/Limjaewoo-kor/study_actuator/assets/68491295/b3b70047-de26-40f9-a9ae-fbf3d3d9ce12)


![그라파나2](https://github.com/Limjaewoo-kor/study_actuator/assets/68491295/733e076c-4d6f-4791-aa91-51bc4daf9c32)


관련 요약 -

모니터링 관련해서는

대시보드(요약본)와 네이버의 오픈소스인 핀포인트(세부사항)를 같이 구성해주는것이 좋다. 

로그는 MDC(uuid등의 로그에 붙는 구분값)를 적용해야 구분이 가능하다. -> MDC 는 대개 필터부분에서 붙이고 끝난후 클리어한다.

일반로그와 에러로그는 구분하자.


알람기능의 경우 이상이 있을시 슬랙이나 문자등을 연동하여 알람을 받으나 최근에는 슬랙(메신저)을 쓰는 추세임. ->옵스지니의 api사용시 전화까지도 가능하다.

알람은 [경고]와 [심각] 2가지 종류로 구분해라

port번호는 아래와 같이 구성하였다.

로컬 - 8080 / Prometheus - 9090 / Grafana - 3000


프로메테우스의 스테이터스 -> 타겟에서 설정 - 

![프로메테우스](https://github.com/Limjaewoo-kor/study_actuator/assets/68491295/c3998cb4-7860-43b4-a4d7-108122ca94d3)


그라파나 -> 톱니바퀴 -> 컨피그레이션에서 설정
![그라파나설정](https://github.com/Limjaewoo-kor/study_actuator/assets/68491295/2435f43f-82d5-415c-a0f1-cf481efec92e)

> java 현재 시간 구하기
> 

현재 시간을 구해야 한다. 쓸 곳이 많다.

```jsx
1.
DateTimeFormatter patten = DateTimeFormatter.ofPattern("HH:mm:ss");               //시간 패턴
String now               = LocalDate.now() + " " + LocalTime.now().format(patten);//전송일시
System.out.println("알림톡 전송시간: " + now);
System.out.println("알림톡 전송시간: " + LocalDate.now() + " " + LocalTime.now().format(patten));
System.out.println(LocalDate.now());
System.out.println(LocalTime.now());
System.out.println(LocalTime.now().getSecond());

2.
SimpleDateFormat sdf1 = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");    
Date now2 = new Date();
String nowTime1 = sdf1.format(now2);
System.out.println(nowTime1);
```

```jsx
2023-05-26 14:53:21
2023-05-26 14:53:21
```

그런데 `문제`가 있다. ㅠㅠ

위와 똑같은 코드로 돌렸는데 어떤 곳에는 초가 00이 나온다. 

`아직 해결 못함 ㅠㅠ`

```jsx
2023-05-26 14:53:00
2023-05-26 14:53:00
```

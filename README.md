## [랜덤 점심 메뉴 추천]
![image](https://github.com/Qnd1101/lunch_menu_recommend/assets/107795830/7032f45c-1e73-4d21-a299-9af7d884b51c)

## 시계 출력 코드
```javascript
window.onload = function() {
const todayDiv = document.getElementById("today");
const timeDiv = document.getElementById("time");

function getTime() {
  let now = new Date();
  timeDiv.textContent = now;
  let year = now.getFullYear(); // 년
  let month = now.getMonth() + 1; // 월
  let date = now.getDate(); // 일
  let hour = now.getHours(); // 시
  let minute = now.getMinutes(); // 분
  let second = now.getSeconds(); // 초
  let day = now.getDay();

  month = month < 10 ? `0${month}` : month;
  date = date < 10 ? `0${date}` : date;
  hour = hour < 10 ? `0${hour}` : hour;
  minute = minute < 10 ? `0${minute}` : minute;
  second = second < 10 ? `0${second}` : second;

  todayDiv.textContent = `${year}년 ${month}월 ${date}일`;
  timeDiv.textContent = `${hour}시 ${minute}분 ${second}초`;
}

getTime();
setInterval(getTime, 1000);
};
```
#### 위 코드에서 window.onload를 통해서 실행과 동시에 함수 내용이 출력 되는 형식으로 
#### getTime 메서드를 만들어서 시간을 가져와 출력하는 형식으로 만들었다

<br>

## 랜덤으로 메뉴를 선택 하는 코드
```javascript
document.write("<h1>오늘의 점심메뉴</h1>");
var com = Math.floor(Math.random() * 5) + 1;
var menu;
switch(com){
  case 1 : menu = "김치찌개";
    break;
  case 2 : menu = "스테이크";
    break;
  case 3 : menu = "비빔밥";
    break;
  case 4 : menu = "짜장면";
    break;
  case 5 : menu = "갓잡은 흑돼지 구이";
    break;
}
document.write("<h3>오늘의 점심메뉴는 " + menu + "</h3>");
document.write("<img src =\"imgs/menu_" + com + ".jpg\">");
```
#### 위 코드를 통해서 랜덤 메뉴를 추천해준다.

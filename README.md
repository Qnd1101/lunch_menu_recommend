## [랜덤 점심 메뉴 추천]
![image](https://github.com/Qnd1101/lunch_menu_recommend/assets/107795830/7032f45c-1e73-4d21-a299-9af7d884b51c)

## html 주요 내용 코드 설명
```html
<div id = "clock">
  <div id="today"></div> <!-- 오늘의 날짜를 표시할 요소 -->
  <div id="time"></div> <!-- 시간을 표시할 요소 -->
</div>
```

## JavaScript 주요 내용 코드 설명
```javascript
window.onload = function() {
};
```
window.onload를 통해서 실행과 동시에 함수 내용이 출력 되는 형식으로 만들었다.
<br>
```javascript
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
```


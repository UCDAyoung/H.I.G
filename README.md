# H.I.G
Human Interface Guildlines in iOS
--- 
(저의 이해를 확인하기 위한 공부 노트.)



### #H.I.G란?

개발자들의 경험과 노하우들을 바탕으로 사용자들에게 좋은 경험을 선사할 수 있는 앱을 만들 수 있게 만들어놓은 가이드라인 

### #왜 H.I.G를 읽어야 하는지? 

- 개발자 뿐 아니라, 디자이너, 기획자 모두 유저에게 좋은 경험을 선사할 수 있는 App을 만드는 것이 목적이기에 공통된 가이드라인이 될 수 있다. 
- 더 확실히 유저를 고려한 App을 만들 수 있을 것 같다.(유저에게 좋은 경험들을 내놓을 수 있는 것들을 공식화해놓은 것 같다.) 
- 일관성을 유지할 수 있다. 
- 이미 검증된 경험이고, 사용해본 경험이기에 유저가 App에 대해 위화감없이 다가갈 수 있다. 

---

### App Architecture

- [1. Launching](#1-launching) <br>
- [2. Onboarding](#2-onboarding)<br>
- [3. Loading](#3-loading) <br>
- [4. Modality](#4-modality) <br>
- [5. Navigation](#5-navigation) <br>
- [Acessing User Data](#6-acessing-user-date) <br>
- [Settings](#7-settings) <br>

---

### 1. Launching 
 
- 시작화면은 빠르고 잘 반응하고 부드러워야한다. 시작화면은 유저에게 너의 어플에 대한 첫인상을 결정하는 중요한 요소이다.
- 화면 방향은 현 화면방향을 유지하되, 사용자에게 필요에 따라 왼쪽이든, 오른쪽이든 화면을 변경할 수 있는 권한을 주면 된다.
- 앱 설정에 대한 정보는 미리 띄우지 말고, 유저가 필요하다면 찾아서 사용할 수 있게 하면 된다. 
- 인앱 라이선스 계약 및 면책 조항을 표시하지말고, 다운로드하기 전에 읽을 수 있도록 표시해놓는다. (사용자 경험을 방해하지 않는 것임)
- 앱이 다시 시작되어도 이전 상태를 유지시켜 계속 사용할 수 있도록 한다. 
- 재부팅이 되는 경우(오류발생,메모리초과 등)을 최대한 없앤다. 
- 앱 평가를 빨리 그리고 자주 요청하지 않는다.

### 2. Onboarding 
Onboarding의 역할은 새로운 유저들과 재방문유저들을 환영하는 용도 
- 직관적이면서 약간의 요약을 보여주어 앱에 대해 알려주는 용도 
- 만약 튜토리얼을 제공해야한다면 반드시 skip을 제공해서 유저들이 선택적으로 학습할 수 있게 해줘야 한다.
- 유저들이 이해하기?힘들어 할 부분을 고려해서 미리 제공하는게 좋은 것 같다.
- 원래 게임하면서,사용해보면서 배우는 것이 좋은 방법인 것처럼 일단 유저들을 바로 사용할 수 있는게 관건
<img width="348" alt="스크린샷 2021-07-23 오후 11 53 45" src="https://user-images.githubusercontent.com/70427427/126800321-b13351b3-cd83-44b3-8b61-78d9ab91c3e2.png">

### 3. Loading<br>
로딩 시 같은 화면이나, 빈 화면을 띄울 경우 앱이 고장난건지,어플이 고장난건지 등 사용자에게 혼란을 줄 수 있겠지?? 그러니 로딩화면에 대해서 알아보자. 
- 가장 기본적인 건 톱니바퀴?돌아가고 있는 사인을 보여주는 것. 진행상태를 보여주는 바를 보여주는게 더 낫다 
- 로딩화면은 빠를수록 좋다. 모두가 느끼는 것. 한국인은 특히 빠른 걸 좋아하기 때문에 더욱 더 기다리게해서는 안되겠다 ㅎㅎ..
- 로딩타임에 어플에 대해 알려주는 화면이나 영상을 넣는게 가장 좋다. 우리가 모바일게임을 할 때를 생각해보면, 로딩 중간중간에 게임이 플레이 되는 화면이나, 게임캐릭터들의 역동적인 활동을 본 적이 있을 것이다. 
- 커스텀하는게 베스트 오브 베스트 
- 아래는 쿠키런 로딩화면 
<img width="964" alt="스크린샷 2021-07-26 오후 1 03 33" src="https://user-images.githubusercontent.com/70427427/126931524-c1f58b39-31e5-42a8-931f-8eeccd5c4259.png">

### 4. Modality<br>
기존에 진행하고 있던 task들과 별개로 긴급한 알림, 특정 task들처럼 중간에 흐름과 별개로 수행해야하는 것들을 모달로 띄어주면 되는 것 같다. 
ios13버전 이후부터는 모달로 띄어주는 방법이 2가지가 있다고 한다. 
1.  Sheet(기존방법인 것 같다.) <br>
   1.1 설명 <br>
        - 카드형식처럼 기존페이지 위에 부분적으로 띄어주는 스타일, 이 방법은 사람들이 기존에 하던 과정들을 잊지않게 해주기 위해서 이렇게 만든 것 같다. <br>
   1.2 모달을 내리는 방법 <br>
        - 스크린 윗부분을 쓸어내린다. 
        - 어디든 쓰러내린다. 
        - 버튼을 클릭한다. <br>
   1.3 그럼 언제 sheet를 사용하냐? <br>
        - 복잡한 작업이 필요없는 nonimmersive(생동감 없는)한 컨텐츠에 <br>
2.  FullScreen <br>
    2.1 설명 <br>
        - 위의 방법과 달리 전체화면을 덮는 방법, 주의분산을 줄이는게 목적이라고 한다. <br>
    2.2 모달 취소 방법 <br>
        - 버튼을 클릭한다. <br>
    2.3 그럼 언제 FullScreen을 사용하나? <br>
        - immersvie(역동적인) 화면 e.g 사진,비디오,카메라 촬영 or 문서 작성 및 사진 편집 등 조금 복잡한 업무를 해야할 때 사용한다고 한다. (sheet과 확연하게 구분이 가능하다.) <br>
        
- 선택을 해야한다거나, 기존 작업과 별개로 다르게 수행해야하는 이유있는 작업일 때 사용하라고한다. 원래 하던 작업과 별개로 작업을 수행시키는 것이고, 게다가 유저가 화면을 직접 취소해야하기 때문에 확실한 이유가 있어야한다.
- 간단한 업무, 빠른, 짧고, 딱 집중해서 봐야할 것에 모달을 사용하면 된다. 
- Done button은 오로지 업무를 완료했을 때만 부여하는걸로 하자.
- 앱 내에 앱을 만들지 말라?? 현재로는 모달로 연속해서 띄우지 말라는 소리 같다. 원래 하던 업무가 무엇인지 까먹을 수 있을 것 같다. 계속해서 업급되는게 유저가 원래 하던 업무에서 길을 잃게 하면 안된다.
- 왜 모달을 띄웠는지에 대한 설명을 해라
- 앱과 조화를 이루게 커스텀해서 띄우고, 일관된 모달스타일을 고수해라. 

여기까지 H.I.G 문서를 읽으며 쓰고 있는데 experience라는 단어가 계속해서 언급이 된다. 정말 사용자 경험을 중요시 여기는구나 생각이 든다.
나처럼 아직 앱을 만들어본 경험이 없는 사람에게 사용자 경험에 대해 신경쓴다는 의미가 와닿지 않는 사람이 읽으면 좋을 것 같다. 


### 5. Navigation
사용자들은 앱이 자신의 기대에 미치지 못할 때 까지, 앱의 네비게이션에 대해 알지 못하는 경향이 있다 -> 이게 무슨 말이지..  <br>
최대한 자연스럽고 친숙하게 , 인터페이스보다 집중하게 만든다거나, 앱의 콘텐츠로부터 집중력을 떨어뜨리게 하면 안된다.  <br>
* 네이게이션의 3가지 메인 스타일 <br>
1.  Hierachical <br>
    1.1  설명 <br>
         - 계층구조라서 유저가 어떤 화면에 도달하기까지 각 화면에서 한 가지의 선택을 해서 찾아가야한다.  <br>
         - 다른 화면으로 이동하기 위해서는 처음부터 시작하거나, 돌아왔던 길을 다시 돌아가야한다 <br>
         - 사용되는 곳 : 설정 or 메일 <br>
         <img width="448" alt="스크린샷 2021-08-01 오전 1 18 43" src="https://user-images.githubusercontent.com/70427427/127746034-114aefdf-cee0-4b72-9e21-e082f4d33b2b.png"><br>

2.  Flat <br>

    2.1 설명 <br>
        - 다수의 카테고리를 이용해 스위칭 가능 <br>
        - 사용되는 곳 : 앱스토어, 음악 앱 <br>
        <img width="396" alt="스크린샷 2021-08-01 오전 1 18 57" src="https://user-images.githubusercontent.com/70427427/127746039-4a44a2cb-f285-4290-96e9-3af5e25245e0.png"><br>
        
3.  Content-Driven or Experience-Driven <br>
    3.1 설명 <br>
        - 그림과 같이 컨텐츠 사이를 자유롭게 오갈 수 있다. <br>
        - 사용되는 곳 : 게임,책 어플 <br>
 <img width="564" alt="스크린샷 2021-08-01 오전 1 19 46" src="https://user-images.githubusercontent.com/70427427/127746057-530b9d4c-c7d0-4b7a-aa5c-18a4b1ceea97.png"><br>

* 추가설명 
- 여러 네비게이션 방식을 결합해서 사용
- 유저 스스로가 어디로 갈지를 명확히 알고 갈 수 있을정도로, 명확한 이동경로를 제공해야 한다. 
- 최소한의 구조만 가질 수 있게, 그 만큼 간결하고 쉽고 빠르게 설계해라 
- 최소한의 터치?friction?만으로 이동할 수 있게 해라 (그 만큼 쉽게 이동할 수 있게 하라는 말인 듯)
- 유저에게 항상 익숙한 경험을 제공하는게 중요한가보다 표준 네비게이션을 사용하라고 한다. 
- 툴바,탭바 등을 이용해서 확실히 명확하게 길을 인지시켜주는게 관건인 것 같다. 계속해서 언급된다.
- 같은 토픽?컨텐츠?를 담아야 하는 화면들이 여러 개라면 page control 을 이용하라! 

### 6. Accessing User Data
유저의 권한이 가장 중요하다. 사람들이 앱에 신뢰를 갖기 위해서는 사적인 데이터들, 그리고 이들의 사용여부가 투명해야한다. 반드시 권한을 요청해서 접근해야한다. 
- 개인적인 정보 : 위치, 건강, 재정, 연락처, 다른 신상정보 
- 사용자로 인해 발생한 데이터 : 이메일, 메세지, 일정표, 연락처, 게임정보, 음악리스트?, Homekit data(와.. 이런 것 까지?), 음성메세지, 영상, 사진 등 
- protected 자원(?) :  블루투스 연결, 와이파이 연결, 로컬 네트워크 접근
- 장치 이용 가능 여부 : 마이크, 카메라 <br> 

> #Important notification <br>
iOS 14.5 그리고 iPadOs 14.5부터,[AppTrackingTransparency framework](https://developer.apple.com/documentation/apptrackingtransparency)를 사용하여 다음과 같은 권한을 확인 받아야 한다. <br>
> - track(사용자의 어플 활용데이터를 tracking? 하는건가 아직 사용해보지 않아서 모르겠다.) <br>
> - 사용자의 광고에 관여해도 되는지도 확인해야하는 것 같다. <br>

<img width="293" alt="스크린샷 2021-08-02 오전 12 08 02" src="https://user-images.githubusercontent.com/70427427/127776209-3fca49ca-c77b-4709-ae23-25ecbd2cdcc1.png">

새로 앱을 출시하거나 업데이트를 할 때 어떤 데이터를 활용하는지, 어떻게 활용하는지하는지 product화면에 게시해야 한다. 
여기서 [App Strore Connect](https://help.apple.com/app-store-connect/#/dev1b4647c5b) 관리가 가능하다. <br> 
다운로드하기 전에 유저가 위와 같은 detail을 읽고 결정할 수 있는 권한을 쥐여주는 것이다. <br>
더 자세한 사항은 [App privacy details on the App Store](https://developer.apple.com/documentation/apptrackingtransparency) 확인 <br>


### 6.1 Requesting Access Permission
권한 사용 요청에 대한 글 <br>
####  6.1.1 진짜 필요할 때 요청하라고 한다. <br>
당연한 말인 것 같은데 설명을 살펴보면, 아무래도 개인정보를 사용하는 것에 의심을 하는 건 당연한 일이다. 그니까 명백한 이유에서 사용한다고 알람을 띄우든, 근거가 될 만한 설명이나, 상황에 알람을 띄어야 한다는 것 같다. 예를 들어, "지도를 사용하려고 할 때 위치 접근 허용을 요청하는 것처럼" 내가 괜히 사용하지 않는 것 같은 데이터를 사용한다고 허가해달라고 하면 의심할 것 같긴하다. <br>
####  6.1.2 데이터가 필요할 때, Launch 타임을 이용해라 <br>
나는 아무래도 앱을 다운받고 바로 실행해서 런치 타임에 뜨는 알림(접근권한에 대한)은 크게 신경쓰지 않았다. 여기서 말한 신경은 "아무도 신경쓰지 않을때를 이용해서 접근을 하게해라!" 이게 아니라, "앱 사용하는데 불편함을 느끼지 않게, 걸리적 거리지 않게" 가 맞는 말인 것 같다.<br>
 data tracking을 할 때는 luanch하자마자 알람을 띄우라고 한다.<br>
유저가 설정에 직접 들어가서 권한 사용에 관한 이유 및 설명을 볼 수 있게 하면 좋은 것 같다.<br>
####  6.1.3 요청한 데이터나 리소스에 대한 사용을 명확하게 설명하는 문구를 써라 <br>
앱 이름 앞(?) 그리고 권한설정을 하기 전에 설명을 보여줘라.(purposing string or usage description string이라고 함)<br>
간결함에 목표르 두고 문장을 간단 명로하게 이해하기 쉽게 써야한다(당연하죠?) <br>
설명에서 약간의 조언을 해준다. 1. 문장을 사용할 것 2.수동적인 어투 쓰지말 것 3. 문장 마지막에 마침표(.)붙이기 <br>
설명을 더 보려면 [Requesting Access to Protected Resources](https://developer.apple.com/documentation/uikit/protecting_the_user_s_privacy/requesting_access_to_protected_resources) 과 [App Tracking Transparency](https://developer.apple.com/documentation/apptrackingtransparency)여기를 참고해라 <br>
#### 예시 <br>
0. 권한 확인하는 곳에 쓴 설명
1. 위치 접근
2. 카메라 접근
3. 연락처 접근 <br>

<img width="523" alt="스크린샷 2021-08-03 오후 10 44 20" src="https://user-images.githubusercontent.com/70427427/128026053-1a3b6b66-b7ae-4f8d-b98a-3377c0dd9809.png"><br>
<img width="300" alt="스크린샷 2021-08-03 오후 10 45 01" src="https://user-images.githubusercontent.com/70427427/128026161-509a1d0c-d795-4664-8d70-dab5c8569065.png">
<img width="332" alt="스크린샷 2021-08-03 오후 10 45 17" src="https://user-images.githubusercontent.com/70427427/128026207-ff99d9ef-739e-49c3-a137-719d482b1807.png">
<img width="297" alt="스크린샷 2021-08-03 오후 10 45 29" src="https://user-images.githubusercontent.com/70427427/128026232-7e0a9d89-967d-428a-85c0-fc24a075d348.png">
<br>

### 6.2 Using the Location Button
iOS 15이후부터 Core Location은 필요할 때만, 일시적인 접근허용을 하게 해준다.<br>

**버튼모양** <br>
- Location 버튼의 모양은 상관없지만, 단번에 이해할 수 있어야 한다.<br>
<img width="235" alt="스크린샷 2021-08-06 오전 11 58 32" src="https://user-images.githubusercontent.com/70427427/128449393-af84e96f-8dac-4960-9ec6-d14a027c79fe.png"><br>
커스터마이징 가능 (일정 부분 내에서만)
- 텍스트 선택 가능  1. Current Location or 2. Share My Current Loation
- 글리프 선택가능 
- 색상 변경 가능(배경색, 텍스트색, 글리프색)
- 테두리 radius 수정가능 
- 버튼이 신뢰가 가야하고, 단번에 이해할 수 있어야한다... 다른 속성들은 커스터마이징 불가  (이 부분은 따로 warningdmfh dkffuwnsekrh gksek.
- 주의할 점이라고는 번역했을 때 글자가 벗어나지 않게 글자크기도 고려해야한다.
>**IMPORTANT**<br>
>시스템이 버튼과 관련항 일관된 문제를 발견하는 경우에, 유저들이 탭해도 접근권한이 부여되지 않아서, 결국에는 유저들의 앱에 대한 신뢰도가 떨어질 수 있다는 점을 유의해라 


**Location Button 클릭 시** <br>
버튼 누름만으로 설정에서 접근권한을 허용한 것과 같은? 그런 기능을 해야 한다. <br>
1. if 클릭, 이전에 이미 허용한 상태라면, 아무 변화가 없으면 되고,  else 접근허용여부알람을 띄워주면 된다. <br>

  다음은 LocatinoButton 구조체이다.
    - at SwiftUi [LocationButton](https://developer.apple.com/documentation/corelocationui/locationbutton)<br>
    - at Swift [CLLoactionButton](https://developer.apple.com/documentation/corelocationui/cllocationbutton)<br>

2. 클릭 시 왜 허용해야하는지에 대한 설명, 그리고 유저의 위치표시자의 시작점을 보여준다.
<img width="263" alt="스크린샷 2021-08-06 오후 12 09 26" src="https://user-images.githubusercontent.com/70427427/128450229-6d585212-6fd9-4288-980e-9524c1058385.png">
3. 이미 한 번 허용한 사람들에게는 다시 설명할 필요 없이 띄어주기만 하면 된다.<br>
4. 만약 몇 번 허용을 누른사람은 따로 누를 필요 없이, 허용하는 법에 대해서 알려주면 될 것 같다. <br>

### 6.3 Using the Microphone in a ShazamKit App

### 6.4 Displaying Custom Messaging Before the Alert

### 6.5 Clarifying Tracking Requests

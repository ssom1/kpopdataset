# kpopdataset

## MobileBERT를 활용한 KPOP 리뷰 분석 프로젝트  
<!-- 
badge icon 참고 사이트
https://github.com/danmadeira/simple-icon-badges
-->
<img src="https://img.shields.io/badge/python-%233776AB.svg?&style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/pytorch-%23EE4C2C.svg?&style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/pycharm-%23000000.svg?&style=for-the-badge&logo=pycharm&logoColor=white" />

## 1. 개 요 
### 1.1 KPOP 영향력

K-pop은 현재도 성장세를 이어가고 있으며, 앞으로도 그 영향력은 더욱 확대될 것으로 예상됩니다. 이는 다양한 요인에 기인하는데, 예를 들어 소셜 미디어의 활성화로 인한 정보 전달력의 증가, 유튜브 등 온라인 플랫폼을 통한 글로벌 홍보와 팬들과의 소통 강화 등이 있습니다. 더불어 K-pop의 음악적 다양성과 고품질의 음악 비주얼, 퍼포먼스 등이 팬들을 매료시키고 있어 그 영향력은 한류 뿐만 아니라 음악 산업 전반에도 큰 파급력을 미칠 것으로 전망됩니다.

### 1.2 kpop시장규모

![동장화면](https://github.com/ssom1/example/blob/main/kpop%20%EC%84%B1%EC%9E%A5.png)
(출처 https://www.romanceip.xyz/kpop2023/) <br>
위 차트는 써클차트(구 가온차트)에서 집계한 연간 피지컬 앨범 판매량(출고 기준) 추이입니다. 국내에서 생산되어 국내 및 해외에 판매된 양을 집계하는 그래프이죠. CD/LP/Tape 등 물리적 매체를 음원 유통의 매개체로 사용하면 피지컬 앨범으로 집계가 되는데 2019년에는 2,500만 장 수준이었던 판매량이 2022년 7,700만 장 수준으로 불과 3년 만에 3배 이상 증가하였습니다.  

## 2. 데이터
### 2.1 원시 데이터
이 데이터는 외국의 reddit이라는 어플의 r/kpop의 게시물의 댓글을 모아둔 것 입니다.
(https://the-eye.eu/redarcs/)

## 기본적인 데이터 정보
submisson: 게시물의 큰 틀(날짜,id,subreddit,title)등 큰 틀을 가지고 있다.

comments : 게시물의 세부적인 댓글들이 작성되어있다.

### 2.2 추출한 데이터
comments에서 한국 여자아이돌 그룹(redvelvet,blackpink,itzy,ohmygirl)이 작성되어있는
댓글을 추출한다.

- 데이터명

|date|artist|comment|sebtiment|vader|
|----|------|---------|------|----|
|날짜|그룹이름|댓글|---|---|


- 활용할 데이터 예시

### 2.3 추출한 데이터에 대한 탐색적 데이터 분석
아이돌 이름 및 그룹, 댓글 게시물 날짜, 댓글 내용등 을 분석한다.
(pandas, matplotlib,pickle)

## 3. 학습 데이터 구축

## 4. MobileBERT 학습 결과

## 5. 느낀점 및 배운점

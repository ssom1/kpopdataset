<img src="https://github.com/ssom1/example/blob/main/k-pop-idol-center-stage-enveloped-in-a-spotlight-fans-silhouettes-forming-a-heart-shaped-ocean-in-.png" alt="동작확인" width="1000" height="350"/>

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
위 차트는 써클차트(구 가온차트)에서 집계한 연간 피지컬 앨범 판매량(출고 기준) 추이를 보여줍니다. 이 차트는 국내에서 생산되어 국내 및 해외에 판매된 CD, LP, 테이프 등 물리적 매체의 음반 판매량을 나타냅니다.

# 차트분석
- 2013년 ~ 2016년: 완만한 증가세 <br>
  이 기간 동안 피지컬 앨범 판매량은 비교적 완만한 증가세를 보였습니다. 2014년에는 약간 감소했지만, 전반적으로는 증가하는 추세였습니다. 이는 K-pop 산업의 꾸준한 성장과 함께 전통적인 음반 판매 방식이 여전히 유지되고 있었음을 보여줍니다.
  
- 2017년 ~ 2019년: 꾸준한 상승 <br>
  2017년부터 2019년까지의 기간은 피지컬 앨범 판매량이 꾸준히 상승한 시기입니다. 특히, 2016년 이후로 매년 5천 장 이상씩 증가하며 2019년에는 2,500만 장을 돌파했습니다. 이는 K-pop의 글로벌 인기가 상승하면서 해외 팬층이 확대됨에 따라 피지컬 앨범 판매량이 증가한 것으로 분석됩니다.

- 2020년 ~ 2022년: 급격한 상승세 <br>
  2020년부터 2022년까지는 피지컬 앨범 판매량이 급격하게 증가한 시기입니다. 2020년에는 약 4,170만 장, 2021년에는 약 5,710만 장, 그리고 2022년에는 약 7,710만 장으로, 불과 3년 만에 판매량이 3배 이상 증가했습니다.
  
## 2. 데이터
### 2.1 원시 데이터
이 데이터는 외국의 reddit이라는 어플의 r/kpop의 예전 게시물과 그 게시물에 대한 댓글을 모아둔 것 입니다. <br>
(https://the-eye.eu/redarcs/)

## 기본적인 데이터 정보
submisson: 게시물의 큰 틀(날짜,id,subreddit,title)등 큰 틀을 가지고 있다.

comments : 게시물의 세부적인 댓글들이 작성되어있다.

### 2.2 추출한 데이터
comments에서 한국 여자아이돌 그룹(redvelvet,blackpink,itzy,ohmygirl)이 작성되어있는
댓글을 추출한다.

- 데이터명

|artist|comment|sebtiment|
|------|---------|------|
|그룹이름|댓글|긍부정예측|

### 2.3 추출한 데이터에 대한 탐색적 데이터 분석
아이돌 이름 및 그룹, 댓글 게시물 날짜, 댓글 내용등 을 분석한다.
(pandas, matplotlib,pickle)

-활용 데이터 예시

|-|artist|review|sentiment|
|----|----|----|----|
|0|redvelvet|i’m gonna do some for my ults \n\nred velvet -...|0.9937|
|1|redvelvet|[seventeen - fear era](https:\/\/youtu.be\/jjv...|-0.7717|
|2|redvelvet|red velvet was robbed but i'm happy to see loo...|0.8847|
|3|redvelvet|**red velvet**\n\nhuff n puff, red dress, time...|0.9856|
|4|redvelvet|personally, i didn't think 2019 was a year of ...|0.4404|
|...|...|...|...|
|41369|itzy|i still think that itzy songs are obviously ha...|0.9722|
|41370|blackpink|yg is by far the best of the big companies whe...|0.9803|
|41371|ohmygirl|oh my girl.\n\nyes, she's indeed|0.4019|
|41372|blackpink|  it isn't the first time yg has recycled a name...|0.5267|
|41373|blackpink|blackpink is a fireeeeeeeeeeeeeeeeeeeeeeeeeeee...|0.9922|


## 3. 학습 데이터 구축
![image](https://github.com/ssom1/kpopdataset/assets/101031955/222a22f2-6af9-416d-8507-ec5b83a7ee52)

![image](https://github.com/ssom1/kpopdataset/assets/101031955/85996933-f81c-40cf-a31a-cfea827ff3c4)

- 댓글에서 0은 부정 1은 긍정인걸 알 수 있다
- 각 아티스트 별 긍부정을 달고 댓글을 확인 해 볼수 있다.

## 4. MobileBERT 학습 결과

## 5. 느낀점 및 배운점
처음으로 원하는 데이터를 가지고와서 직접 구축하니까 힘든일도 많았습니다
찾다가 reddit이라는 어플에서 옛날 계시물들을 보관해 두는 홈페이지를 찾아서
"comments"파일과 "submission"파일을 찾아내서 제가 원하는 년도와 원하는 그룹이 언급 되어 있는
댓글을 찾아서 긍부정을 찾아냈습니다 
데이터를 찾아내고 정리하는게 생각보다 쉽지 않아서 힘들었지만 데이터를

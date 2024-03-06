# 🎥  유튜브 썸네일 기반 조회수 예측(영화, 드라마 리뷰 영상 중심)

## 💡 Motivation

유튜브는 2023년 12월 기준으로 월간 활성 이용자 수 부문에서 카카오톡을 제치고 1위를 차지하였으며,

또한, 유튜브는 오래 사용하는 앱 부문에서 압도적인 1위를 차지하고 있는 명실상부 '국민 앱' 입니다.

이에 많은 개인과 기업들이 유튜브를 통해 다양한 콘텐츠를 제공하고, 수익을 창출하고 있습니다.

하루에도 많은 콘텐츠들이 생성되고 공유되고 있는 유튜브에서 사용자들은 시청할 하나의 영상을 선택해야 하기 때문에 어떤 영상을 시청할 것인지 고민에 빠집니다.

그렇다면 사용자들의 선택에 가장 많이 영향을 미치는 요소는 무엇일까요?

선행 연구에 따르면 유튜브 사용자는 썸네일에 집중하여 영상의 시청 여부를 결정하고, 이는 조회수 상승으로 이어져 해당 채널의 수익을 증가시킵니다.

최근 유튜브의 광고수익을 주 수입원으로 하는 크리에이터들이 늘어나면서, 수익에 큰 영향을 미치는 썸네일은 더욱 중요해지고 있습니다.

따라서 본 프로젝트에서는 머신러닝을 통해 유튜브 썸네일의 다양한 요소들을 기반으로 구독자 수 대비 조회수를 예측하고자 합니다.

여러 카테고리 중 영화 및 드라마 카테고리의 영상들에 대해 어떠한 요소들로 썸네일을 구성했을 때 조회수를 향상시킬 수 있을지 분석하였습니다.

여러 유튜브 카테고리 중 드라마 및 영화 리뷰를 선택한 이유는 크게 두 가지입니다.

첫째, 드라마 및 영화 리뷰는 원작 콘텐츠가 존재하기 때문에 영상 간 내용의 유사도가 높습니다.

둘째, 유재석, 신세경 등 썸네일의 효과를 상쇄시킬 가능성이 높은 유명 인플루언서 운영자가 희박합니다.

즉, 영화 및 드라마 리뷰 분야는 운영자와 콘텐츠의 차별성이 낮아 썸네일의 효과가 가장 극대화될 수 있는 분야라고 판단하였기에 이로 범위를 한정하였습니다.

## 🛠️ How?

드라마 및 영화 리뷰 채널 영상 데이터 수집 👉🏻 [[pytube]](https://pytube.io/en/latest/) 라이브러리

각 채널의 월별 구독자 수 추이 👉🏻 [[social blade]](https://socialblade.com/) 참고

썸네일 이미지 요소 분석 👉🏻 [[Google Cloud Vision]](https://cloud.google.com/vision?hl=ko) API 사용

텍스트 감정분석 👉🏻 SKT Brain [[KoBERT]](https://github.com/SKTBrain/KoBERT) 모델, Naver [[CLOVA Sentiment]](https://www.ncloud.com/product/aiService/clovaSentiment) API 사용

감정분석 모델 학습용 데이터 👉🏻 AI HUB [[감성대화 말뭉치]](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&dataSetSn=86), [[단발성 대화 데이터셋]](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=270) 사용

데이터 분석 및 시각화 👉🏻 Tableau

## 📚 참고 문헌

👉🏻 [Practical Assessment, Research, and Evaluation] Improving your data tr our data transformations: Applying the Bo ansformations: Applying the Box-Cox transformation - Jason Osborne

👉🏻 [IEEE TRANSACTIONS ON COMPUTATIONAL SOCIAL SYSTEMS] Visual Attributes of Thumbnails in Predicting YouTube Brand Channel Views in the Marketing Digitalization Era - Ha Eun Jang, Seung Ho Kim, Jong Seok Jeon and Joo Hee Oh

👉🏻 [ResearchGate] More than meets the eye: The functional components underlying influencer marketing - Colin Campbell

👉🏻 [광고PR실학연구] 인플루언서 유형에 따른 유튜브 동영상 콘텐츠에 대한 소비자 반응 - 정태영, 황장선

👉🏻 [디지털콘텐츠학회논문지 Vol. 22, No. 6] 유튜브 섬네일의 시각표현 요소가 사용자 만족도와 재시청의도에 미치는 영향 연구 - 이승민

👉🏻 [디지털콘텐츠학회논문지 Vol. 23, No. 6] 유튜브 알고리즘 요인 탐색을 위한 역공학설계 연구 : 머신러닝과 딥러닝 응용을 중심으로 - 김철년, 배승주, 하윤수, 이상호

👉🏻 [한국융합학회논문지 제13권 4호] 유튜브 ‘인기급상승’ 장기 노출을 위한 콘텐츠 전략에 관한 연구 - 이민영, 변국도, 최상현

👉🏻 [한국디자인문화학회지 Vol. 27, No. 4] 유튜브 콘텐츠 섬네일의 시각적 표현이 이용자들의 상호작용에 미치는 영향 연구 - 문상호, 강태임

👉🏻 [한국스포츠산업경영학회지 제26권 3호] 유튜브 스포츠 영상 콘텐츠의 소비 결정 요인 : 다층회귀모형을 통한 빅데이터 분석 - 김종호, 김기한

👉🏻 Hand Gesture Recognition Based on Karhunen-Loeve Transform - Joyeeta Singha, Karen Das

👉🏻 Understanding the Characteristics of Internet Short Video Sharing: YouTube as a Case Study - Xu Cheng, Cameron Dale, Jiangchuan Liu

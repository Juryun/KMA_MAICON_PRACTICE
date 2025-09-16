# 🏆 Sentence Event Classification Challenge

## 📌 Overview

현대 사회에서는 수많은 학술 활동과 이벤트가 개최됩니다. 회의, 세미나,
논문 발표 등 다양한 이벤트를 빠르고 정확하게 분류하는 것은 일정 관리,
정보 검색 및 자동화된 추천 시스템에 필수적인 요소입니다.

이번 대회의 목표는 **문장(`Sentence`)을 입력으로 받아 어떤 이벤트
유형(`Label`)에 속하는지 분류하는 모델**을 개발하는 것입니다.

참가자들은 주어진 학습 데이터를 활용하여 머신러닝/딥러닝 기반 분류
모델을 학습시키고, 테스트 데이터에 대한 예측 결과를 제출해야 합니다.

------------------------------------------------------------------------

## 📂 Data Description

데이터는 이벤트 관련 문장과 해당 문장의 카테고리로 구성되어 있습니다.

-   **Train 데이터 (`problem1_train.csv`)**
    -   `Sentence`: 영어 문장 (이벤트 관련 문장)
    -   `Label`: 해당 문장의 이벤트 유형
        -   예시 클래스: `meetings`, `papers`, `seminar`, ...
-   **Test 데이터 (`problem1_test.csv`)**
    -   `Sentence`: 영어 문장 (레이블 없음)
-   **Submission 파일**
    -   참가자가 예측한 결과를 제출하는 CSV 파일

### Example (Train)

  -----------------------------------------------------------------------
  Sentence                                Label
  --------------------------------------- -------------------------------
  Excited for the mindfulness retreat for meetings
  educators next week!                    

  Experience the fusion of art and        papers
  technology in our research!             

  Excited to be part of the               seminar
  #CybersecurityConference this year!     
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 🎯 Evaluation

-   평가 지표는 **Accuracy (정확도)** 입니다.\
-   테스트 데이터에 대한 참가자의 예측 결과를 기준으로 리더보드 점수가
    산출됩니다.

공식 평가 지표:

\[ Accuracy =
`\frac{ \text{Number of Correct Predictions} }{ \text{Total Predictions} }`{=tex}
\]

------------------------------------------------------------------------

## 📑 Submission Format

제출 파일은 CSV 형식이어야 하며, 두 개의 컬럼을 포함해야 합니다:

-   `Sentence`: 테스트 데이터의 원본 문장\
-   `Label`: 참가자가 예측한 이벤트 유형

### Example (Submission)

    Sentence,Label
    "Excited for the mindfulness retreat for educators next week!",meetings
    "Experience the fusion of art and technology in our research!",papers
    "Excited to be part of the #CybersecurityConference this year!",seminar
    ...

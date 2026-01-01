# (Master-2, 2025) Supply-Chain Project
<LCA 기반 탄소감축을 고려한 OEM–공급자 간 공급망 조정모형 연구
“A Supply Chain Coordination Model Between OEMs and Suppliers Considering Carbon Reduction Based on Life Cycle Assessment (LCA)”>

## 0. Project Overview
- **Project Period**: 2025.09 - 2025.12

---

## 1. 프로젝트 개요 (Overview)

본 프로젝트는 **3단계 공급망(OEM–Tier1–Tier2)** 구조에서  **탄소 배출 감축 의사결정과 경제적 인센티브 설계**를 수리적으로 분석하는 것을 목표로 합니다.

특히,
* 탄소 규제(Cap, Carbon Tax),
* 중앙집중 최적화,
* Stackelberg 게임 기반 보조금(subsidy)

이 **공급망 성과(이윤)**와 **탄소 감축 수준**에 미치는 영향을 비교·분석합니다.

> **핵심 질문**
> * 분산된 기업들이 탄소 감축을 자발적으로 수행할 수 있는가?
> * 중앙집중 혹은 OEM 주도의 인센티브가 언제 효과적인가?
> * 규제 기반(cap)과 인센티브 기반(subsidy)의 차이는 무엇인가?

---

## 2. 연구 배경 및 동기 (Motivation)

* EU CBAM, 탄소세, Scope 3 배출 관리 강화로 인해 **자동차 공급망 전반의 탄소 감축 의사결정**이 필수가 됨
* 기존 연구는 개별 기업 또는 단일 단계 분석에 집중
* 본 연구는 **다단계 공급망 + 전략적 상호작용 + 비용 구조**를 동시에 고려
<img width="1041" height="465" alt="image" src="https://github.com/user-attachments/assets/cf695d45-5115-4d8e-ad13-60694b090cb7" />


---

## 3. 공급망 구조 (Supply Chain Structure)
<img width="524" height="480" alt="image" src="https://github.com/user-attachments/assets/194cd97c-f245-4e74-aa97-f4b05ad0b6cf" />

```
Tier 2 (원자재 / 부품)
        ↓
Tier 1 (중간재 / 모듈)
        ↓
OEM (완제품 / 시장 판매)
```

* 모든 기업은 **동일한 수요 D**를 충족
* 단일 제품, 단일 기간, 결정론적 환경 가정

---

## 4. 기본 가정 (Model Assumptions)

### 4.1 생산 및 수요

* 각 기업 생산량:
  [
  q_i = D
  ]

### 4.2 배출 함수 (Emission)

* 기준 배출량: ( e_{i0} )
* 감축 노력: ( z_i \in [0,1] )

[
E_i = e_{i0} \cdot (1 - \alpha_i z_i)
]

---

### 4.3 비용 함수 (Cost)

[
C_i = c_i D + \beta_i z_i^2
]

* (c_i): 단위 생산비
* (\beta_i): 감축 비용 계수 (convex)

---

### 4.4 탄소 비용

[
\text{Carbon Cost}_i = \lambda E_i
]

---

## 5. 시나리오 설계 (Scenarios)
<img width="1041" height="292" alt="image" src="https://github.com/user-attachments/assets/32a183ad-ecba-45ec-9cf2-c2b2edf3eb7d" />


### 🔹 S1 : Subsidy Model (보조금 분담 모형)

* 각 기업은 **감축 노력 미수행**: ( z_i = 0 )
* 개별 이윤 극대화
* 탄소 감축 없음

> **기준선(Benchmark)** 역할

---

### 🔹 S2 : Hierarchical Pricing Model (계층적 가격 모형)

* 전체 공급망 이윤 최대화:

[
\max_{z_1,z_2,z_3} \sum_i \Pi_i
]

* 총 배출량 Cap 제약:

[
\sum_i E_i \le \text{Cap}
]

* 사회적 최적(Social Optimum)에 가장 근접
* 실제 산업 적용은 어려움 (정보 공유 필요)

---

## 6. 실험 및 분석 방법 (Methodology)
연구 대상 모델 : 현대자동차의 대표 전기차인 아이오닉 5 Standard 모델을 선정하여 파라미터 구성하며 '현대자동차 지속가능성 보고서'의 공개된 데이터를 참조

* 민감도 분석

  * Best Response
  * Stackelberg Equilibrium
* 비교 정태 분석 (Comparative Statics)

  * ( \lambda, \beta_i, \gamma, D ) 변화
* 수치 시뮬레이션

  * 시나리오별 이윤, 배출량, 감축률 비교

---

## 7. 실험 결과 

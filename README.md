[# Human Intelligence Modeling — Research

> 인간이 여러 감각으로부터 하나의 세계를 구성하는 계산 원리를 이해하고,
> 그로부터 나만의 연구 질문을 찾기 위한 개인 연구 저장소.

이 문서는 **나침반**이다. 논문을 읽다가, 실험을 돌리다가 방향을 잃었을 때
30초 안에 열어보고 "내가 무엇을 왜 하고 있었는지"를 다시 맞추기 위한 한 페이지.

상세 내용은 이 문서에 쌓지 않는다. 늘어나면 하위 파일·노션으로 내려보내고,
여기에는 방향과 상태만 남긴다.

---

## 핵심 가설

인간은 각 감각을 독립적으로 처리하는 것이 아니라,
외부 세계에 대한 **하나의 내부 표현(Internal World Representation)** 을
지속적으로 구성하고 갱신한다.

각 감각은 그 표현을 갱신하기 위한 **관측(Observation)** 이며,
행동(Action)은 새로운 관측을 만들어 다시 표현을 수정한다.

```
External World
      ↓
 Observation  ← (각 감각 = 같은 세계를 다르게 관측하는 센서)
      ↓
 Perception
      ↓
 Representation  ← (프로젝트의 중심 대상)
      ↓
 Prediction → Cognition → Decision
      ↓
 Action
      ↓
 New Observation  → (순환)
```

> 이것은 **작업 가설(working hypothesis)** 이지 검증된 사실이 아니다.
> Predictive Processing, Active Inference, World Models, Multisensory Integration 등
> 기존 연구와의 관계 속에서 검토·수정된다.

---

## 스코프 경계

**지금 다루는 것**

- 하나의 에이전트가 지각과 상호작용을 통해 외부 세계의 내부 표현을
  어떻게 구성·유지·갱신하는가.

**지금 다루지 않는 것** (중요 — 이걸 못 박아야 프로젝트가 다시 불어나지 않는다)

- 의식 (Consciousness) / Qualia / hard problem
- 감정 (Emotion)
- 언어의 기원 (Language as origin of intelligence)
- 사회적 지능 (Theory of mind, 협력, 문화)

위 주제들은 나중에 확장될 수 있으나, 현재의 전제조건은 아니다.

---

## 반증 조건 (이 가설이 흔들린다고 볼 때)

이 프로젝트의 핵심 가설은 다음 중 하나가 성립하면 재검토한다.

- 명시적 내부 표현을 가정하지 않고도(예: 생태심리학, behavior-based robotics)
  같은 현상이 더 적은 가정으로 설명될 때.
- 여러 감각이 하나로 통합되지 않고, 부분적 결합만으로 충분함이 드러날 때.
- 표현·예측·행동을 잇는 순환 구조가 유용한 예측이나 연구 질문을
  더 이상 만들어내지 못할 때.

> 원칙: **어떤 가설도 수정으로부터 보호받지 않는다.**
> 목표는 이 틀이 옳음을 증명하는 것이 아니라, 더 정확한 이해로 나아가는 것이다.

---

## 지금의 상태

- **지금의 질문:** _(미정 — 관련 공부를 더 한 뒤 확정한다)_
- **지금 공부 중:** _(예: Predictive Processing / Multisensory Integration / World Models)_
- **다음 액션 3개:**
  - [ ]
  - [ ]
  - [ ]

---

## 저장소 구조

```
research/
├── README.md          ← 이 파일. 나침반 (가설·경계·반증·현재 상태)
├── ARCHIVE.md         ← 초기 브리프 전문. 평소엔 안 봄. SOP·서베이 쓸 때의 광산.
├── literature/        ← 논문별 요약 (노션 Papers DB와 1:1 대응)
├── experiments/       ← 실험별 폴더 (코드 + 노트)
└── figures/           ← 다이어그램
```

**역할 분담**

- **노션** = 관제탑. 논문·gap·실험의 *상태*를 본다 (Papers · Gaps · Experiments DB).
- **깃허브(이 레포)** = 원본 텍스트와 코드가 사는 곳.
- 둘은 링크로 연결한다 (노션 항목 → 이 레포의 파일/커밋).
Uploading README.md…]()

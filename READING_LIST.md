# 읽기 리스트 (순서 있음)

> ROADMAP의 세 겹 동심원을 실제 논문으로 채운 것.
> **위에서 아래로 읽는다.** 각 항목: 왜 읽나 / 무엇을 뽑아낼까.
> 읽으면 반드시 노션 Papers DB에 10개 질문 틀로 요약을 남긴다.
>
> ⚠️ 이 리스트는 2026년 1월까지의 지식 기준. 고전·앵커는 확실하지만
> 2025~26년 최신 world model / physical AI 후속작은 빠졌을 수 있다.
> 웹 검색으로 각 트랙의 최신작을 보강할 것.

---

## 트랙 0 — 출발점: 내가 이미 아는 것 (복습, 0.5주)

이미 구현해봤으니 빠르게 "왜"만 다시 짚는다.

1. **Chi et al. (2023), "Diffusion Policy"** — RSS.
   *왜:* 내 quadruped 프로젝트의 뿌리. behavior cloning의 multimodality 문제를
   diffusion이 어떻게 푸는지. *뽑을 것:* action chunk, receding horizon, FiLM conditioning.

2. **Janner et al. (2022), "Planning with Diffusion" (Diffuser)** — ICML.
   *왜:* diffusion을 "정책"이 아니라 "계획"으로 쓰는 관점. *뽑을 것:* classifier
   guidance, trajectory를 하나의 분포로 보는 시각.

3. **Ajay et al. (2023), "Decision Diffuser"** — ICLR.
   *왜:* classifier-free guidance로 조건부 생성. *뽑을 것:* states-only diffusion +
   inverse dynamics. (준성님이 강의 정리에서 이미 다룬 것)

---

## 트랙 1 — World Models: 표현을 "왜"로 다시 읽기 (1~2주)

**목표:** diffusion policy를 아는 것에서, "world model이 지능에서 뭘 하나"를 아는 것으로.

4. **Ha & Schmidhuber (2018), "World Models"**.
   *왜:* 짧고 직관적. 시작점으로 최적. *뽑을 것:* V(표현)→M(예측)→C(행동) 분리,
   "왜 예측이 행동을 돕는가".

5. **Hafner et al. (2019), "Learning Latent Dynamics for Planning from Pixels" (PlaNet)**.
   *왜:* 잠재 공간에서 예측하고 계획하는 실제 구현. *뽑을 것:* latent dynamics model,
   픽셀이 아닌 표현에서 planning.

6. **Hafner et al. (2023), "Mastering Diverse Domains through World Models" (DreamerV3)**.
   *왜:* world model 계열의 성숙한 형태. 하나의 모델로 여러 도메인. *뽑을 것:*
   imagination 기반 학습, "상상 속에서 정책을 학습한다"는 아이디어.

7. **LeCun (2022), "A Path Towards Autonomous Machine Intelligence"** — 포지션 페이퍼.
   *왜:* 내 브리프와 소름 돋게 비슷. 읽으면 "내 생각이 이미 여기 있었네" 싶을 것.
   *뽑을 것:* JEPA — 픽셀 재구성이 아닌 표현 공간 예측. world model 중심 아키텍처.

8. **(선택) Assran et al. (2023), "I-JEPA"** / **V-JEPA (2024), V-JEPA 2 (2025)**.
   *왜:* 위 JEPA 철학의 실제 구현. 웹 스케일 영상 사전학습 + 최소 로봇 데이터로
   작동하는 world model. *뽑을 것:* 표현 공간에서의 예측이 실제로 작동하는 방식.

9-S. **[지형도] Ding et al. (2025), "Understanding World or Predicting Future?
   A Comprehensive Survey of World Models"** — ACM Computing Surveys.
   *왜:* 2018 이후 world model 연구 전체를 정리한 최신 서베이. 고전으로 뿌리를
   잡은 뒤 이걸로 현재 지형을 한눈에. *뽑을 것:* "세계를 이해하는가 vs 미래를
   예측하는가"라는 분류축 — 내 브리프의 핵심 긴장과 정확히 겹친다.
   *참고 최신 시스템(2024~26, 개념만 훑기):* DeepMind Genie 3, NVIDIA Cosmos
   (physical AI용 world foundation model), Meta V-JEPA 2, DreamerV3 (Nature 2025).

**이 트랙 완료 신호:** "world model은 왜 픽셀을 직접 예측하지 않고 표현 공간에서
예측하는가?"에 내 말로 답할 수 있다.

---

## 트랙 2 — 이론적 뿌리: Predictive Processing / Active Inference (2~3주)

**목표:** 내 브리프의 순환 구조가 이 이론의 재발견임을 확인. 그 위에서 "나는 뭘 더할까".

9. **Clark (2013), "Whatever Next? Predictive Brains, Situated Agents…"**.
   *왜:* 철학자가 쓴 서베이. 수식 없이 읽혀 진입점으로 최적. *뽑을 것:* 예측오차
   최소화가 지각과 행동을 동시에 설명하는 방식.

10. **Rao & Ballard (1999), "Predictive Coding in the Visual Cortex"**.
    *왜:* predictive coding의 원전. *뽑을 것:* 뇌가 예측하고 오차만 위로 보낸다는
    계층적 구조. 내 "관측→표현" 단계의 신경과학적 근거.

11. **Friston (2010), "The Free-Energy Principle"** — Nature Reviews Neuroscience.
    *왜:* Active Inference의 수학적 뼈대. 어렵지만 핵심. *뽑을 것:* 행동이 "예측을
    맞추기 위한 능동적 표집"이라는 관점 — 내 브리프의 Action 가설과 직결.

> **열린 공간 (2024~26 기준):** predictive processing의 "계층적 예측" 주장은
> 신경과학적으로 잘 지지되지만, *예측과 예측오차를 담당하는 별개의 신경 단위가
> 실제로 존재하는가*는 아직 확립되지 않았다. 이건 내게 빈 연구 공간의 신호 —
> 계산 모델로 이 구분을 검증하는 방향이 열려 있다.

**이 트랙 완료 신호:** 내 브리프의 Assumption 3~5(행동이 관측을 만들고 표현을
갱신)를 Predictive Processing 용어로 다시 쓸 수 있다.

---

## 트랙 3 — Physical AI / Embodied: 행동과 세계 (2~3주)

**목표:** 준성님 강점 영역의 큰 그림. "행동이 표현을 어떻게 만드는가".

12. **Bajcsy (1988), "Active Perception"** (또는 Bajcsy et al. 2018 재조명판).
    *왜:* "지각은 능동적이다"의 원전. 내 브리프의 "action is part of perception"
    가설의 뿌리. *뽑을 것:* 관측이 행동에 의존한다는 관점.

13. **Brohan et al. (2022), "RT-1"** / **(2023) "RT-2"** — robot foundation models.
    *왜:* 대규모 로봇 정책 = physical AI의 현재. *뽑을 것:* vision-language-action의
    통합, 스케일이 여는 것. (2024~26 후속작은 웹 검색으로 보강)

14. **(선택) Driess et al. (2023), "PaLM-E"** — embodied multimodal.
    *왜:* 언어+지각+행동을 한 모델로. 내 브리프의 "통합 표현" 관점과 연결.

15-S. **[지형도] Ma et al. (2025), "A Survey on Vision-Language-Action Models
    for Embodied AI"** — arXiv.
    *왜:* VLA(vision-language-action) 분야 전체 입문. RT/OpenVLA/π0 등 최신
    generalist policy들의 지형. *뽑을 것:* 지각·언어·행동을 하나로 매핑하는
    현재의 주류 접근과 그 한계.

15-T. **★ Huang et al. (2025), "Tactile-VLA: Unlocking VLA Model's Physical
    Knowledge for Tactile Generalization"** — arXiv:2507.09160.
    *왜:* **내 브리프의 촉각 출발점과 정확히 겹치는 최신작.** VLA에 촉각을
    결합한 연구. *뽑을 것:* 촉각이 "또 하나의 모달리티"가 아니라 물리적
    이해를 여는 열쇠라는 관점 — 내 "감각 = 같은 세계의 다른 관측" 가설의 실증.

**이 트랙 완료 신호:** "행동은 단순 출력이 아니라 정보 수집 과정"이라는 주장을
구체적 사례로 설명할 수 있다.

---

## 트랙 4 — 반대 진영과 실증: 정직한 시험 (여유 될 때)

**목표:** 브리프 91·95장에서 스스로 약속한 것. 지지와 반대를 같은 무게로.

15. **Ernst & Banks (2002), "Humans Integrate Visual and Haptic Information…"** — Nature.
    *왜:* **지지 증거.** 인간이 시각+촉각을 베이지안 최적으로 통합. 내 "통합 표현"
    가설의 정량적 근거. 짧다. *뽑을 것:* 통합이 실험으로 측정된다는 사실.

16. **Brooks (1991), "Intelligence without Representation"**.
    *왜:* **반대 진영.** 내부 표현 없이도 지능이 된다는 주장. *뽑을 것:* 내 핵심
    가설(표현 중심)에 대한 가장 강한 반론.

17. **Gibson (1979), "The Ecological Approach to Visual Perception"** — 책(개요만).
    *왜:* **반대 진영.** affordance, direct perception. *뽑을 것:* "표현이 정말
    필요한가?"라는 근본 질문.

**이 트랙 완료 신호:** "내 가설이 틀렸다면 어떤 증거가 그걸 보여줄까?"에 답할 수
있다 → README 반증 조건이 날카로워진다.

---

## 읽는 순서 요약 (한 줄)

```
0 (복습) → 4·5·6·7 (World Models) → 9·10·11 (Predictive Processing)
        → 12·13 (Physical AI) → 15·16·17 (반대 진영)
        선택항목(8·14)은 관심 생길 때
```

## 원칙

- **주 1편.** 많이 읽는 게 목표가 아니다. 한 편을 10개 질문으로 깊게.
- **트랙을 건너뛰지 마라.** World Models 없이 Predictive Processing으로 가면 붕 뜬다.
- **완료 신호로 판단.** 각 트랙 끝의 "완료 신호"에 답할 수 있으면 다음으로.
- **이번 주 할 일:** 4번(Ha & Schmidhuber) 읽고 Papers DB에 첫 요약. 그거 하나.

# 루프 실행 기록 (loop-run)

handover-navigator 산출물을 **Generator–Evaluator 루프**로 실제로 돌린 기록입니다. "완료 게이트가 self-check"라는 약점을, 작성(Generator)과 채점(Evaluator)을 분리해 **합격할 때까지 반복**함으로써 해결하는 과정을 보여줍니다. (모든 데이터는 가상)

## 결과 요약

| 회차 | 결과 | 비고 |
| --- | --- | --- |
| 1회차 | **8/9 PASS** | 기준1(출처 추적) FAIL — 표는 출처 완비였으나 1페이지 요약 문장에 인라인 출처 누락 |
| 2회차 | **9/9 PASS** | 해당 항목만 수정 → STATUS: COMPLETED. 기준2(환각 0)는 두 회차 모두 유지 |

핵심: self-check였다면 그대로 통과시켰을 결함(요약 문장 무출처)을 **독립 Evaluator**가 잡아냈고, Generator는 그 항목만 고쳐 2회차에 수렴했습니다. 가장 엄격한 기준2(환각 0)는 원본 대조로 끝까지 PASS.

## 파일

- `loop-practice.md` — 루프 설계: `/loop` 한 줄 + Generator/Evaluator 프롬프트(간략·상세) + Rubric 9개 + 정지장치
- `01_handover-summary.md` · `02_open-tasks-tracker.md` · `03_questions-to-ask.md` — Generator 최종 산출물(2회차 반영)
- `feedback-r1.md` — Evaluator 1회차 채점 (8/9, FAIL 근거 포함)
- `feedback-r2.md` — Evaluator 2회차 재채점 (9/9, COMPLETED)

설계 배경은 상위 `../../README.md`, 환각 대조 실험은 `../../evals/eval-report.md` 참고.

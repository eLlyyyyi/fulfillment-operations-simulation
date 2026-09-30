# Fulfillment Operations Simulation

물류센터의 입고(IB) → 피킹 → 패킹 → 허브 공정을 이산사건 시뮬레이션으로 모델링하고, 인력 배치 변화가 처리시간과 대기열에 미치는 영향을 비교한 프로젝트입니다.

## What this project shows

- 시간대별 주문 유입과 점심·휴식 시간의 작업 인원 감소 모델링
- 공정별 리소스와 대기열 추적
- 병목 공정 식별 및 추가 인력 배치 시나리오 비교
- 주문 처리시간 분포와 공정별 대기열 시각화

실험에서는 피킹과 허브 공정의 인력 배치를 조정해 기존 병목을 완화했습니다. 최종 시나리오는 9시간 동안 생성된 1,560건 중 1,559건을 허브까지 처리했고, 평균 처리시간은 약 127초였습니다. 이 수치는 노트북에 저장돼 있던 마지막 실행 결과를 요약한 것이며, 무작위 시뮬레이션 특성상 다시 실행하면 조금 달라질 수 있습니다.

## Repository structure

```text
.
├── fulfillment_simulation.ipynb  # simulation scenarios and analysis
├── requirements.txt              # runtime dependencies
└── README.md
```

## Run locally

Python 3.10 이상을 권장합니다.

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab fulfillment_simulation.ipynb
```

노트북 출력은 저장소 크기와 개인정보 노출 가능성을 줄이기 위해 제거했습니다. 위에서 아래 순서로 셀을 실행하면 그래프와 결과가 다시 생성됩니다.

## Notes

- 특정 기업의 실제 운영 데이터나 내부 시스템을 사용하지 않은 교육용 시뮬레이션입니다.
- 기업명 대신 일반적인 물류 공정 용어로 저장소를 구성했습니다.
- 입력값은 가정에 기반하므로 실제 운영 의사결정에는 별도 검증이 필요합니다.


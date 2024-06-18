## KR-ELECTRA finetuning NSMC dataset

네이버 영화리뷰 데이터셋(NSMC)으로 KR-ELECTRA 모델을 파인튜닝합니다.

아래 패키지가 필요합니다.

```
torch==1.8.0
transformers==4.16.1
seqeval
fastprogress
attrdict
```

추가로 국립국어원 인공지능 말평에서 부적절성 문장에 대한 태도 탐지 과제의 말뭉치를 [다운로드](https://kli.korean.go.kr/benchmark/taskOrdtm/taskDownload.do?taskOrdtmId=108&clCd=ING_TASK&subMenuId=sub02) 해야합니다.

다운로드한 데이터셋(train, dev, test)은 `./data` 디렉터리 하위에 위치시켜 주세요.

### Guide

1. Clone the repository

```bash
git clone https://github.com/jaewoogwak/KR-ELCTRA-finetune-NSMC.git
```

2. Navigate to the project directory

```bash
cd KR-ELCTRA-finetune-NSMC
```

3. Install packages

```bash
pip install -r requirements.txt
```

4. Finetune Model

```bash
python3 run_seq_cls.py --task nsmc --config_file kr-electra.json
```

파인튜닝이 완료되면 `run.ipynb` 코드를 실행시켜 평가할 수 있습니다.

# Truth Tag : OCR Server
> _OCR model을 서빙하는 OCR Server의 코드를 관리한 Repository_

<!-- <img width="1456" alt="image" src="https://github.com/dev-munchkins/truthtag-ai-server/assets/68195241/678d1058-fad2-4a55-b123-be373f7af8af">
![alt text](image.png) -->
![alt text](image-3.png)

## OCR Pipeline
![alt text](<Group 39.png>)

## Tech Stack
#### Model Serving
- ```Python 3.11.8```
- ```FastAPI 0.111.0```

#### AI (OCR)
- ```easyocr==1.7.1``` 기반 finetuning한 모델
- ```torch==2.3.0```
- ```torchvision>=0.9.0```
- ```rapidfuzz```
- ```ultralytics==8.2.36```

## How to...
> ⚠️ 해당 프로젝트는 GPU가 있는 환경에서 실행해야 빠른 결과를 얻을 수 있습니다.

### Install
- 터미널에 접속하여 다음 명령어를 실행한다.
```bash
git clone https://github.com/dev-munchkins/truthtag-ocr-server.git
```

### Build
1. 터미널에 다음 명령어를 실행하여 다운로드 받은 프로젝트 내부로 이동한다.
```bash
cd truthtag-ocr-server
```

2. 터미널에 다음 명령어를 실행하여 가상 환경을 생성한다.
```bash
python3 -m venv ./venv
```

3. 터미널에 다음 명령어를 실행하여 가상 환경을 활성화한다.
```bash
source venv/bin/activate
```

4. 터미널에 다음 명령어를 실행하여 가상 환경 내부에 필수 라이브러리를 설치한다.
```bash
pip install -r requirements.txt
```

5. 터미널에 다음 명령어를 실행하여 서버를 동작시킨다.
```bash
python3 app.py
```

### Test
- 환경에 따라 다음 링크를 클릭하여 Swagger 문서로 접속하면 테스트가 가능하다.
  - [로컬 환경](http://localhost:8000/docs)
  - [배포 환경](https://ai.truthtag.site/docs)

- <b>Request 예시<b>: AWS S3 bucket에 저장되어 있는 이미지 url을 입력합니다. <br>
![alt text](image-1.png)
<br>

- <b>Response 예시<b>: 상품 이름과 브랜드가 인식된 결과를 반환합니다. <br>
![alt text](image-2.png)
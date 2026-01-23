1. requirement.txt  만들기
 파이참 터미널에서  pip freeze > requirements.txt

2. 깃에 올리기
 git add requirements.txt
 git commit -m "Add requirements.txt for deployment"
 git push origin main

3. 우분투에서 받기
 git clone https://github.com/twomoonclub/fastapi01.git
 cd 리포지토리명 (리포지트리 폴더 생김)

4. 우분투에서 환경 설정
 sudo apt update
 sudo apt install python3-venv -y
 python3 -m venv venv
 source venv/bin/activate

5. pip install -r requirements.txt
6. 테스트 실행 (도커 실행전)
  uvicorn main:app --host 0.0.0.0 --port 8000
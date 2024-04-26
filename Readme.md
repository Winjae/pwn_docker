# 도커 이미지 생성 명령어
docker build -t [이름]:[태그} .  

# 도커 컨테이너 생성 
docker run -it -d --name [컨테이너 이름] [이미지 이름]:[이미지 태그]  

# 생성된 도커 컨테이너 실행
docker exec -it [컨테이너 이름] /bin/bash

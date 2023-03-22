## Colima 설치

```bash
$ brew install colima
```

[homebrew가 없다면](https://github.com/abiosoft/colima)

## Docker 설치

```bash
$ brew install --cask docker
```

[docker 설치 경로](https://www.docker.com/products/docker-desktop/)

docker설치 후 로그인 진행

## Colima 실행

Colima and Docker를 설치했다면 실행

```bash
$ colima start --memory 4 --arch x86_64
```

`docker ps`명령어가 제대로 작동하면 정상적으로 설치가 된 것이다

## Oracle Database 11gR2 XE 설치

```bash
docker search oracle-xe-11g
```
다운 받을 수 있는 docker images 확인

```bash
docker pull jaspeen/oracle-xe-11g
```
설치할 이미지

```bash
docker run --name oracle -d -p 1521:1521 jaspeen/oracle-xe-11g
```
컨테이너 옵션 설정

```bash
docker exec -it oracle sqlplus
```
sqlplus실행

user-name은 "system"
password는 "oracle"(기본값)

SQL연결 완료

## SQL Developer 설치

[SQL Developer 설치 경로](https://www.oracle.com/database/sqldeveloper/technologies/download/)

Apple Silicon은 "Mac ARM64 with JDK 11 included"를 다운로드

Intel은 "Mac OSX with JDK 11 included"를 다운로드

다운받은 SQL Developer.app 파일을 Applications 폴더에 이동

[만약 실행이 안된다면](https://shanepark.tistory.com/87)

SQL Developer를 들어가서 수동으로 접속 생성 클릭
Name은 필수 입력 
Username은 "system"입력
Password은 "oracle"입력

```
Name : 이 접속을 뜻하는 이름
UserName : 설정한 계정명
Password : 계정의 비밀 번호
Connection Type : 연결 타입
```

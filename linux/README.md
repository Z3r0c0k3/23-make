# 2023-03-31 linux 수업 스크립트
## 1.  Kali Linux 설치
- VirtualBox 설치. [virtualbox 홈페이지](https://virtualbox.org)
- kali linux vm 이미지 파일 다운로드 [이미지 파일 홈페이지](https://url.dyhs.kr/kali)
- 압축 풀고 .vbox파일 실행
## 2.  CLI 환경 적용
- 터미널 실행
## 3.  기본적인 Linux 명령어
- ls 명령어
	- ls는 현재 위치한 디렉토리의 파일과 폴더를 출력하는 명령어입니다. ls 명령어에는 다양한 옵션이 존재합니다. 예를 들면, -a 옵션은 숨겨진 파일까지 출력하는 옵션입니다.
- cd 명령어
	- cd는 디렉토리를 이동하는 명령어입니다. cd 명령어 뒤에 이동하고자 하는 디렉토리의 경로를 입력하면 해당 디렉토리로 이동할 수 있습니다. 예를 들면, cd /home/user/Downloads는 /home/user/Downloads 디렉토리로 이동하는 명령어입니다.
-  pwd 명령어
	- pwd는 현재 위치한 디렉토리의 경로를 출력하는 명령어입니다.
- mkdir 명령어 
	- mkdir은 디렉토리를 생성하는 명령어입니다. 예를 들면, mkdir mydir는 mydir이라는 이름의 디렉토리를 생성하는 명령어입니다.
- rmdir 명령어
	- rmdir은 디렉토리를 삭제하는 명령어입니다. 예를 들면, rmdir mydir는 mydir이라는 이름의 디렉토리를 삭제하는 명령어입니다. 하지만 해당 디렉토리에 파일이 존재하면 삭제가 불가능합니다.
- cp 명령어
	- cp는 파일을 복사하는 명령어입니다. 예를 들면, cp file1.txt file2.txt는 file1.txt 파일을 file2.txt 파일로 복사하는 명령어입니다.
- mv 명령어
	- mv는 파일을 이동하거나 이름을 변경하는 명령어입니다. 예를 들면, mv file1.txt /home/user/Downloads는 file1.txt 파일을 /home/user/Downloads 디렉토리로 이동하는 명령어입니다. 또한, mv file1.txt file2.txt는 file1.txt 파일을 file2.txt 파일로 이름을 변경하는 명령어입니다.
- rm 명령어
	- rm은 파일을 삭제하는 명령어입니다. 예를 들면, rm file1.txt는 file1.txt 파일을 삭제하는 명령어입니다.
- chmod 명령어
	- chmod는 파일 또는 디렉토리의 권한을 변경하는 명령어입니다. 예를 들면, chmod 755 file1.txt는 file1.txt 파일의 권한을 rwxr-xr-x로 변경하는 명령어입니다. chmod 명령어에는 다양한 옵션이 존재하며, 권한을 숫자로 표현할 수도 있습니다.
- chown 명령어
	- chown은 파일 또는 디렉토리의 소유자를 변경하는 명령어입니다. 예를 들면, chown user1 file1.txt는 file1.txt 파일의 소유자를 user1으로 변경하는 명령어입니다.
- grep 명령어
	- grep은 파일 내에서 특정한 문자열을 검색하는 명령어입니다. 예를 들면, grep "hello" file1.txt는 file1.txt 파일에서 "hello" 문자열을 검색하는 명령어입니다.
- wget 명령어
	- wget은 인터넷에서 파일을 다운로드하는 명령어입니다. 예를 들면, 
wget  [http://example.com/file1.txt](http://example.com/file1.txt) 파일을 다운로드하는 명령어입니다.
## 5.  Docker 설치 및 사용
### Docker 설치
-  apt 업데이트 및 필요 패키지 설치
```sh
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release
```
- docker gpg키 설치
```sh
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
- docker 저장소 설정
```sh
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
- docker 설치
```sh
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
- 리눅스 부팅시 자동 실행
```sh
sudo systemctl enable docker
sudo systemctl start docker
```
- docker 사용 권한 변경
``` sh
sudo usermod -aG docker $USER
```
- 재부팅
- 재부팅 후 도커 설치 확인
```sh
docker --version
```
### Docker 사용방법


6.  다양한 OS 처리

-   Linux에서 다른 운영 체제의 파일을 복사하고 이동하는 방법을 학습합니다.
-   Linux에서 다른 운영 체제와의 파일 공유를 위해 Samba 서비스를 설치하는 방법을 학습합니다.
-   Linux에서 다른 운영 체제와의 네트워크 공유를 위해 NFS(Network File System)를 설치하는 방법을 학습합니다.

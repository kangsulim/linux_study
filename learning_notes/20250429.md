# 리눅스(우분투) 기본 명령어 정리

## 📁 파일·디렉토리 관련

| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `pwd` | 현재 경로 출력 | `pwd` |
| `ls` | 파일/폴더 목록 보기 | `ls -l` (자세히 보기) |
| `cd [경로]` | 디렉토리 이동 | `cd /home/user` |
| `mkdir [폴더명]` | 새 폴더 만들기 | `mkdir myfolder` |
| `rmdir [폴더명]` | 비어있는 폴더 삭제 | `rmdir myfolder` |
| `rm -r [폴더명]` | 폴더(비어있지 않아도) 삭제 | `rm -r myfolder` |
| `touch [파일명]` | 새 파일 만들기 | `touch file.txt` |
| `cp [원본] [복사본]` | 파일/폴더 복사 | `cp a.txt b.txt` |
| `mv [원본] [대상]` | 파일/폴더 이동/이름변경 | `mv a.txt folder/` |
| `rm [파일명]` | 파일 삭제 | `rm a.txt` |
| `cat [파일명]` | 파일 내용 출력 | `cat file.txt` |
| `nano [파일명]` | 파일 편집(간단 편집기) | `nano file.txt` |
| `vim [파일명]` | 파일 편집(고급 편집기) | `vim file.txt` |

---

## 🔎 파일·내용 찾기

| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `find [경로] -name [파일명]` | 파일 찾기 | `find /home -name "*.txt"` |
| `grep [찾을내용] [파일명]` | 파일 안에서 문자열 찾기 | `grep "hello" file.txt` |
| `grep -r [찾을내용] [폴더]` | 폴더 안 모든 파일에서 찾기 | `grep -r "test" ./` |

---

## 🖥️ 시스템 정보 확인

| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `uname -a` | 시스템 전체 정보 | `uname -a` |
| `hostname` | 호스트 이름 확인 | `hostname` |
| `whoami` | 현재 사용자 확인 | `whoami` |
| `top` | 실시간 CPU/메모리 상태 보기 | `top` |
| `htop` | (더 보기 편한 top, 설치 필요) | `htop` |
| `df -h` | 디스크 사용량 보기 | `df -h` |
| `free -h` | 메모리 사용량 보기 | `free -h` |

---

## ⚙️ 사용자/권한 관리

| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `sudo [명령어]` | 관리자 권한으로 실행 | `sudo apt update` |
| `chmod [권한] [파일/폴더]` | 권한 변경 | `chmod 755 script.sh` |
| `chown [소유자]:[그룹] [파일/폴더]` | 소유자 변경 | `chown user:user file.txt` |
| `adduser [사용자명]` | 사용자 추가 | `sudo adduser newuser` |
| `passwd [사용자명]` | 비밀번호 변경 | `sudo passwd newuser` |

---

## 🌐 네트워크 관련

| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `ping [주소]` | 연결 테스트 | `ping google.com` |
| `curl [주소]` | 웹 요청 보내기 | `curl https://example.com` |
| `wget [주소]` | 파일 다운로드 | `wget https://example.com/file.zip` |
| `ip a` | IP 주소 확인 | `ip a` |
| `ssh [user]@[주소]` | 원격 접속 | `ssh user@192.168.0.10` |

---

## 📦 패키지 설치/관리

(우분투는 apt 씀!)

| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `sudo apt update` | 패키지 목록 갱신 | `sudo apt update` |
| `sudo apt upgrade` | 설치된 패키지 업그레이드 | `sudo apt upgrade` |
| `sudo apt install [패키지명]` | 프로그램 설치 | `sudo apt install git` |
| `sudo apt remove [패키지명]` | 프로그램 삭제 | `sudo apt remove git` |

---

## 🛠️ 프로세스/서비스 제어

| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `ps aux` | 모든 프로세스 보기 | `ps aux` |
| `kill [PID]` | 프로세스 죽이기 | `kill 1234` |
| `kill -9 [PID]` | 강제 종료 | `kill -9 1234` |
| `systemctl start [서비스명]` | 서비스 시작 | `sudo systemctl start nginx` |
| `systemctl stop [서비스명]` | 서비스 중지 | `sudo systemctl stop nginx` |
| `systemctl restart [서비스명]` | 서비스 재시작 | `sudo systemctl restart nginx` |
| `systemctl status [서비스명]` | 서비스 상태 확인 | `systemctl status nginx` |

---

## 🔥 기타 유용한 명령어
| 명령어 | 설명 | 예시 |
| --- | --- | --- |
| `history` | 입력했던 명령어 기록 보기 | `history` |
| `clear` | 터미널 화면 깨끗하게 | `clear` |
| `alias [새이름]='[명령어]'` | 명령어 짧게 만들기 | `alias ll='ls -l'` |
| `exit` | 셸 종료 | `exit` |
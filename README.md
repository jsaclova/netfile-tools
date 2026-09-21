# 📂 대화형 파일 전송 및 원격 제어 시스템 (netfile-tools)

맥(macOS) 환경에서 동일 네트워크상에 존재하는 다른 PC들과 대화형 UI를 통해 파일/폴더를 안전하게 송수신하고, 터미널 SSH 원격 접속 제어 및 전송 이력을 일자별로 정밀 기록하는 단독 자동화 툴킷입니다.

---

## 🚀 원클릭 초고속 자동 설치 가이드 (Installation)

```bash
curl -sSL https://githubusercontent.com -o /tmp/netfile_install && chmod +x /tmp/netfile_install && /tmp/netfile_install && rm -f /tmp/netfile_install
```

---

## 🛠️ 핵심 명령어 안내

| 명령어 | 주요 기능 | 비고 |
| :--- | :--- | :--- |
| **`netsend`** | 대화형 파일/폴더 **보내기** | `Path ➡️ 목적지 선택 ➡️ 원격지 경로` 3단계 가이드<br>실시간 `%` 출력 및 일자별 로그에 `[SEND_SUCCESS]` **2줄 적재** |
| **`netget`**  | 대화형 파일/폴더 **가져오기** | 원격지 컴퓨터의 기물을 내 다운로드 폴더로 수신<br>실시간 `%` 출력 및 일자별 로그에 `[GET_SUCCESS]` **2줄 적재** |
| **`netssh`**  | 주소록 기반 **SSH 원격 접속** | 주소록에서 기기를 선택하면 IP/유저명을 칠 필요 없이<br>자동으로 원격 터미널 세션 연결 구동 |

---

## 📋 목적지 주소록 관리 (`target_list.txt`)
```text
# [Target_Name] [Remote_Username] [Destination_IP]
Host1 User:merong IP:192.168.55.49
Host2 User:airjin IP:192.168.55.100
Host3 User:prox   IP:192.168.55.156
Host4 User:jin    IP:192.168.55.3
```

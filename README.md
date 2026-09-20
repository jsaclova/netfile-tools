# 📂 대화형 파일 전송 및 수신 시스템 (netfile-tools)

맥(macOS) 환경에서 동일 네트워크상에 존재하는 다른 PC들과 대화형 UI를 통해 파일 및 폴더를 안전하게 송수신하고, 개별 파일 단위의 전송 이력을 일자별로 정밀 기록하는 단독 자동화 툴킷입니다.

---

## 🚀 원클릭 초고속 자동 설치 가이드 (Installation)

새로운 PC나 포맷한 맥 터미널에서 **아래 한 줄만 복사해서 실행**하면 깃허브로부터 단독 패키지를 전송받아 환경 변수 매핑까지 5초 만에 완료합니다.

```bash
curl -sSL https://githubusercontent.com -o /tmp/netfile_install && chmod +x /tmp/netfile_install && /tmp/netfile_install && rm -f /tmp/netfile_install
```

> ⚠️ **설치 후 필수 완료 명령어**: 무결점 작동을 위해 설치가 끝나면 아래 명령어를 한 번 치거나 터미널 창을 새로 열어주세요.
> ```bash
> source ~/.zshrc
> ```

---

## 🛠️ 핵심 명령어 안내

터미널 작업 위치와 상관없이 어디서든 명령어 이름만 입력하면 즉시 구동됩니다.

| 명령어 | 주요 기능 | 비고 |
| :--- | :--- | :--- |
| **`netsend`** | 대화형 파일/폴더 **보내기** | `Path ➡️ 목적지 선택 ➡️ 원격지 경로` 3단계 가이드<br>실시간 `%` 출력 및 전송 완료 개별 하위 파일 목록을 일자별 로그에 `[SEND_SUCCESS]` 마크로 **파일당 정확히 2줄씩 적재** |
| **`netget`**  | 대화형 파일/폴더 **가져오기** | 원격지 컴퓨터의 기물을 내 다운로드 폴더로 수신<br>복제 직후 로컬 저장소를 정밀 추적하여 실제 안착한 모든 하위 파일 주소를 `[GET_SUCCESS]` 마크로 **파일당 정확히 2줄씩 적재** |

---

## 📋 목적지 주소록 관리 (`target_list.txt`)

* **경로**: `~/bin/netfile-tools/target_list.txt`
* **포맷**: 새로운 기기 정보가 추가되면 파일 끝에 동일한 영문 규칙으로 더해주면 메뉴에 실시간 자동 반영됩니다.
```text
# [Target_Name] [Remote_Username] [Destination_IP]
Host1 User:merong IP:192.168.55.49
Host2 User:airjin IP:192.168.55.100
Host3 User:prox   IP:192.168.55.156
```

---

## 📂 디렉토리 구조 (Directory Map)
```text
~/bin/netfile-tools/
├── README.md        # 본 단독 저장소 메인 대시보드 지침서 (현재 파일)
├── netfile_install  # 타 기기 원클릭 복제 전용 자동 설치 스크립트
├── netsend          # 대화형 원격 파일 전송 스크립트 (실시간 % 출력)
├── netget           # 대화형 원격 파일 수신 스크립트 (실시간 % 출력)
├── target_list.txt  # User:텍스트, IP:텍스트 명세 주소록 데이터베이스
└── log/             # 개별 파일별 전송 소요 시간 적재소 (2줄 포맷, Git 제외)
```

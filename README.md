# Git-diff-wargame-lv1

# Lv.1 — Can you find a flag?

## 문제
`lv1.py`를 실행하면 플래그를 입력하라고 한다.
git 명령어를 활용해서 플래그를 찾아라.

## 실행 방법
```bash
python lv1.py
```

## 풀이 흐름
1. 커밋 히스토리 확인
2. git diff로 패치 파일 생성
3. patch -R로 파일 복원
4. 복원된 파일 실행 후 플래그 입력

## 명령어 설명
- `git log --oneline` : 커밋 히스토리를 한 줄로 출력
- `git diff <커밋1 해시> <커밋2 해시>` : 두 커밋 사이의 변경사항 출력. `-`로 시작하는 줄은 삭제된 줄, `+`로 시작하는 줄은 추가된 줄

## 주의사항 (PowerShell 환경)
PowerShell에서는 `>` 대신 아래 명령어를 사용해야 한다.
```powershell
git diff <커밋1 해시> <커밋2 해시> | Out-File -FilePath fix.patch -Encoding utf8
```
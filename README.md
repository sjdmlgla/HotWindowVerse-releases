# HotWindowVerse 배포 저장소

순수 C17 / Win32로 만든 Windows 3×3 창 작업 공간 **HotWindowVerse**의 설치·업데이트 파일만 올리는 저장소입니다. 소스 코드는 공개하지 않습니다.

## 설치

1. [최신 릴리스](https://github.com/sjdmlgla/HotWindowVerse-releases/releases/latest)에서 `Setup_HotWindowVerse.exe`를 내려받습니다.
2. 실행하면(관리자 승인 필요) `C:\HotUtility\HotWindowVerse`(바꿀 수 있음)에 설치하고, 이미 설치되어 있으면 새 버전으로 업데이트합니다.
3. 제거는 Windows 설정 → 앱 → 설치된 앱 → HotWindowVerse에서 합니다.

## 자동 업데이트

Setup으로 설치한 HotWindowVerse는 시작할 때와 실행 중 하루 한 번 이 저장소의 최신 릴리스를 확인합니다. 새 버전이 있으면 알려 주고, [지금 업데이트]를 누르면 설치 파일을 내려받아 함께 올린 `Setup_HotWindowVerse.exe.sha256` 검증값과 같을 때만 실행해 새 버전으로 바꿉니다. 이때 HotWindowVerse가 관리하던 다른 앱 창은 원래 위치로 되돌린 뒤 정상 종료합니다. 도움말 → 업데이트 확인 또는 트레이 메뉴의 업데이트 확인에서 직접 확인할 수 있고, 새 버전 창의 확인란으로 자동 확인을 끌 수 있습니다.

## 검증값 확인

```
certutil -hashfile Setup_HotWindowVerse.exe SHA256
```

결과가 릴리스의 `Setup_HotWindowVerse.exe.sha256` 내용과 같아야 합니다.

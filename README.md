# kiosk-releases

우리동네 균형코치 키오스크 앱의 **배포 파일만** 두는 저장소입니다. 코드는 없습니다.

- `latest.json` — 기기가 6시간마다 읽는 최신판 안내. 이 파일이 바뀌는 순간 현장 기기가 새 판을 받습니다.
- Releases — 판마다 APK 한 개 (`kiosk-<versionName>-<versionCode>.apk`). 파일은 덮어쓰지 않고 판마다 새로 올립니다.

올리는 방법은 앱 저장소의 `scripts/release.sh` 한 번입니다. APK 를 먼저 올리고 `latest.json` 을 마지막에 바꿉니다.
APK 는 공개돼도 됩니다 — 안드로이드가 설치할 때 깔린 앱과 서명 키를 대조하므로 다른 파일은 설치되지 않습니다.

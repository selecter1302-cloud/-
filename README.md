# Android MOD v0.4.2 — 관계 잠금 팝업 수정

[모바일 ZIP 다운로드](https://github.com/selecter1302-cloud/-/raw/refs/heads/gensokyo-android-v0.4.2/Gensokyo-Mod-Android-v0.4.2.zip)

[APK 직접 다운로드](https://github.com/selecter1302-cloud/-/raw/refs/heads/gensokyo-android-v0.4.2/Gensokyo-Mod-Android-v0.4.2.apk)

기존 앱을 삭제하지 말고 업데이트 설치하세요. 모바일에서 APK 다운로드가 실패하면 ZIP 링크를 Chrome에서 열어 다운로드하고 압축을 푼 뒤 APK를 설치하세요.
ARM64 Android 7.0 이상. 동일 앱 ID·서명 유지, versionCode 6.

수정한 버그
- 게임 자체의 관계 잠금에서 주인공과의 관계를 고정하면, 협박 중 → 복종 관계 변경 제안이 나오지 않도록 수정.
- 제안 가능 여부, 장면 종료 시 대기 질문 생성, 이미 남은 질문 응답 모두 잠금을 확인.
- 질문이 이미 대기 중일 때 관계 잠금 또는 전체 잠금을 켜면 해당 질문을 정리.
- 이전 저장 파일에 잠긴 관계의 질문이 남아 있어도 불러올 때 정리. 저장된 관계와 잠금은 그대로 유지.
- 잠금을 풀면 기존 게임의 제안 조건을 그대로 사용. 다른 히로인/라이벌 쪽 잠금이나 수치 잠금만으로 이 질문을 막지 않음. 다른 종류의 질문은 유지.
- 기존 모드 기능, 길게 누르기, 화면 비율과 게임 데이터/이미지는 이전 v0.4.1과 동일.

원인: 실제 관계 변경은 잠금을 검사했지만, 변경 제안을 생성하는 경로가 잠금을 확인하지 않았음.
실제 게임 동작을 바꾼 파일은 scripts/scene_sex_result.gd, scripts/game_state.gd 두 개입니다.

검증
- 이전 버전에서 히로인 4명 모두 버그 재현.
- 완성 APK 추출 리소스를 Linux Godot 4.6.3에서 검사: 잠금/질문/이전 저장 복구 80개, 입력·수치·저장 630개(두 해상도), 기존 모드 996개, 모바일 UI 40개 통과. 총 1,746개.
- 서명, 동일 인증서, versionCode, ARM64, 16KB 정렬과 ZIP CRC 검사 통과.
- 실제 Android 기기 설치·실행은 미검증.

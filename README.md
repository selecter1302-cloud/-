# Gensokyo Dialogue Review v0.1.0

[Download the complete review ZIP](https://github.com/selecter1302-cloud/-/raw/refs/heads/gensokyo-dialogue-review-v0.1.0/Gensokyo-Dialogue-Review-v0.1.0.zip)

한국어 대사 창작 검토본입니다. APK에는 아직 적용하지 않았습니다.

- 레이무·마리사·사쿠야·사나에의 기본 발화 후보 616개.
- 일곱 관계, 두 몸 상태, 직후·다음 만남·시간 경과, 허용/거절을 나눈 완성 항목 1,232개.
- 1,232개는 몸 상태별로 기본 발화를 공유하는 변형을 포함한 수입니다.
- ZIP을 푼 뒤 review/index.html을 브라우저로 여세요. 캐릭터별 Markdown 전체본과 모든 항목 JSON도 있습니다.
- 원문 초안, 상태별 지문·속마음, 문서 생성 Python 소스, 적용 조건, 실제 실행 검증 기록을 포함합니다.
- EXE·APK는 포함하지 않습니다. 게임 실행·Android 기기 검증·브라우저 동작 검증을 마친 결과물이 아닙니다.

## 실제 검증

별도 폴더에서 Python 생성 스크립트를 실행해 7개 검토 산출물이 원본과 바이트 단위로 일치하는 것을 확인했습니다.
기본문장 616개가 모두 다른 문자열이며, 1,232개 ID와 모든 조건별 후보가 존재하는지 검사했습니다.
검토 화면의 JavaScript 구문 검사와 ZIP CRC 검사도 통과했습니다.
실행 상세 기록은 VALIDATION.json, ZIP SHA-256은 SHA256SUMS.txt에 있습니다.

이 브랜치는 기존 APK 배포 브랜치를 덮어쓰지 않는 검토본 전용 배포입니다.

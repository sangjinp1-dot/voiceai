# Sangjin Voice AI - React Native Expo v1.0.0

Flutter 소스를 React Native Expo 프로젝트로 변환한 버전입니다.

## 주요 구조

- package.json
- app.json
- eas.json
- App.js
- docs/

## 포함 기능

- 녹음
- OpenAI Whisper STT
- OpenAI TTS
- AI 음성 비서
- TXT Reader
- 문단별 읽기
- AI 요약
- Voice Profile 샘플 녹음 구조
- 약관/개인정보 화면
- 무료/프리미엄 플랜 구조
- 온보딩
- Expo EAS APK/AAB 빌드 구조

## Termux 준비

```bash
pkg update -y
pkg install nodejs git unzip -y
npm install -g eas-cli
```

## 실행

```bash
npm install
npx expo start
```

## APK 빌드

```bash
eas login
eas init
eas build -p android --profile preview
```

## AAB 빌드

```bash
eas build -p android --profile production
```

## 중요

- `app.json`의 `extra.eas.projectId`는 `eas init` 후 본인 프로젝트 ID로 교체하세요.
- 실제 출시 전 API 키는 AsyncStorage가 아니라 서버 프록시/보안 저장소로 바꾸는 것이 좋습니다.
- PDF 텍스트 추출은 Expo 기본 안정성을 위해 제외하고 TXT Reader 중심으로 변환했습니다.

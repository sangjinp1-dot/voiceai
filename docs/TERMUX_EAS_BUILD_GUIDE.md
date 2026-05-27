# Termux + Expo EAS Build Guide

```bash
pkg update -y
pkg upgrade -y
pkg install nodejs git unzip -y
npm install -g eas-cli
unzip sangjin_voice_ai_expo_v1_0_0.zip
cd sangjin_voice_ai_expo_v1_0_0
npm install
eas login
eas init
eas build -p android --profile preview
```

APK 빌드가 끝나면 EAS가 다운로드 링크를 제공합니다.

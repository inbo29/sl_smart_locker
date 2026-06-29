# SHOES LOVE · Ухаалаг хадгалах локер (UI/UX дизайны баримт бичиг)

신발 세탁 브랜드 **SHOES LOVE**의 스마트 보관 로커 시스템 UI/UX 설계서입니다.
모든 화면 설명은 **몽골어(Cyrillic)**, 디자인은 2022 리브랜딩 가이드라인(틸 `#00babe` + 옐로우 `#ffd400`) 기반.

단일 파일 `index.html` 로 동작합니다. (외부 의존성: Google Fonts CDN만)

## 🔗 라이브 (GitHub Pages)

`main` 에 push 하면 GitHub Actions가 자동 배포합니다:

```
https://inbo29.github.io/sl_smart_locker/
```

> 최초 1회: 저장소 **Settings → Pages → Build and deployment → Source = "GitHub Actions"** 로 설정하세요.

## 📱 화면 구성 (총 10개)

**시스템 A — 스마트 디스플레이 (키오스크)**
- `A1` 광고/대기 (지점 표시 · 영상 무한재생 · 기사 QR 버튼)
- `A2` 고객 — 맡기기 (전화 입력 → 함 추가 → 완료 → 5초 후 자동 복귀)
- `A3` 고객 — 찾기 (전화 입력 → "№__ 함 열림" → 5초 후 자동 복귀)
- `A4` 기사 — 키오스크 QR (리스트는 기사 휴대폰에 표시)

**시스템 B — 기사 앱 (모바일)**
- `B0` 기사 로그인
- `B1` 알림 / `B2` QR 스캔 → 보관 리스트 / `B3` 지도 / `B4` 내 수거 이력
- 로그인 후 하단 탭바: 알림 · 위치 · QR · 리스트

## 🎬 광고/사용법 영상 넣기

`index.html` 스크립트 상단 `AD_PLAYLIST` 배열에 경로를 순서대로 추가하면 무한 반복 재생됩니다:

```js
const AD_PLAYLIST = [
  'videos/ad1.mp4',
  'videos/guide1.mp4',
];
```

- 로컬: 저장소에 `videos/` 폴더를 만들고 mp4를 넣은 뒤 함께 push
- 비워두면 SHOES LOVE 브랜드 화면(폴백)이 표시됩니다

## 🚀 처음 올리기 (command line)

```bash
git init
git add .
git commit -m "SHOES LOVE smart locker UI/UX spec"
git branch -M main
git remote add origin https://github.com/inbo29/sl_smart_locker.git
git push -u origin main
```

이후에는 변경 후 `git add . && git commit -m "..." && git push` 하면 자동 재배포됩니다.

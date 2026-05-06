# Roadmap

솔로 개발·현역 복무 중이라 페이스는 느슨합니다. 버전·일정은 목표일 뿐 확정 아님.

> Solo developer, currently in active military service — pace is light. Versions and dates are aspirational.

## v0.1 — MVP ✅ (현재 0.1.2)

- Spotify / Apple Music 재생곡 감지
- LRCLIB 싱크 가사 + Google 무료 번역 (9개 언어)
- MenuBarExtra UI, 현재 / ±1 라인 표시
- 선번역 (`withTaskGroup`) · 싱크 외삽 (메타데이터 500ms + UI 100ms)
- 팔레트 전환 ambient 배경 (TimelineView 60fps)
- 재생 컨트롤 (play / pause / prev / next)
- 번역 표시 토글 (eye 아이콘) · `@AppStorage` 영속화
- 커스텀 리본 마크 아이콘
- `.dmg` 패키징 파이프라인

## v0.2 — 공개 배포 준비

- Sparkle 기반 자동 업데이트 (appcast)
- 타 음악 앱 지원 확장 (예: VLC, Apple Podcasts, YouTube Music 데스크톱 앱)
- 다국어 번역 프로바이더 추가 (대체 엔드포인트 + BYO key 검토)
- 설정 패널 (팔레트 선택, 폰트 크기, 기본 번역 언어 고정)
- About / 피드백 메뉴 (앱 내 버전·이슈 링크)

## v0.3 ~ 0.5 — 기능 확장

- 시스템 오디오 캡처 (ScreenCaptureKit + Whisper) — YouTube · 브라우저 · 모든 소스 범용 지원
- 가사 감정 분석 기반 3D 이펙트
- 풀스크린 카라오케 모드
- 광고 모듈 (실험적, 무료 티어만)

## v1.0 — 정식 공개

- Apple Developer 가입 + 서명 · 공증
- 무료 / Pro 티어 분리
- LicenseStore 활성화

## Maybe / later

- iOS 컴패니언 (검토 단계)
- 번역 품질 개선용 LLM 옵션 (BYO key)
- 커뮤니티 팔레트 공유

---

피드백 · 제안: <https://github.com/currenjin/versa/issues>

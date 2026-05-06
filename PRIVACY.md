# Privacy

_Last updated: 2026-04-28 · Applies to Versa v0.1.x._

Versa는 메뉴바에 가사를 띄우기 위해 필요한 최소한의 데이터만 외부에 보냅니다. 식별자 · 계정 정보 · 사용 텔레메트리는 일절 수집하지 않습니다.

## 외부로 나가는 데이터

| 보내는 곳 | 무엇을 | 왜 |
|---|---|---|
| **LRCLIB** (`lrclib.net`) | 곡 제목 · 아티스트 · 앨범 · 길이 | 싱크 가사를 받아오기 위해 |
| **Google Translate** (`translate.googleapis.com`, 무인증 엔드포인트) | 가사 라인 한 줄씩 | 번역을 받아오기 위해 |

두 호출 모두 **음원 자체나 사용자 식별 정보는 포함하지 않습니다.** 곡 메타데이터와 가사 텍스트만 전송됩니다.

## 로컬에만 머무는 데이터

- 번역 결과 캐시 (라인 단위)
- 사용자 설정 (선택한 번역 언어, 토글 상태)

모두 macOS `UserDefaults` (`@AppStorage`) 에 저장되며 외부로 나가지 않습니다.

## 수집하지 않는 것

- IP 주소 · 위치 · 기기 식별자
- 계정 · 로그인 정보 (Versa는 로그인이 없습니다)
- 사용 기록 · 분석 텔레메트리 · 크래시 리포트
- 광고 · 추적 SDK

## 향후 변경 가능성

- **자동 업데이트(Sparkle)** 도입 시 — 업데이트 확인을 위해 앱이 주기적으로 `appcast.xml` 을 fetch 합니다. 이때 호스팅 서버 액세스 로그에 IP 가 기록될 수 있습니다.
- **선택적 사용 분석** 도입 시 — 명시적 opt-in 토글로만 동작합니다. 가사 내용 · 곡명 · 식별자는 전송 대상에 포함되지 않습니다.

위 변경은 새로운 버전에서만 적용되며, 이 문서가 함께 갱신됩니다.

## 문의

데이터 처리에 대한 질문은 <https://github.com/currenjin/versa/issues> 에 남겨주세요.

---

# Privacy (English)

_Last updated: 2026-04-28 · Applies to Versa v0.1.x._

Versa sends only the minimum data required to display lyrics in your menu bar. It does **not** collect identifiers, account information, or usage telemetry.

## What leaves your Mac

| Sent to | What | Why |
|---|---|---|
| **LRCLIB** (`lrclib.net`) | Track title · artist · album · duration | To fetch synced lyrics |
| **Google Translate** (`translate.googleapis.com`, unauthenticated endpoint) | One lyric line at a time | To fetch translations |

Neither request contains audio data or any user-identifying information.

## What stays local

- Translation cache (per line)
- Your settings (selected target language, translation toggle)

All stored in macOS `UserDefaults` (`@AppStorage`); none of it is uploaded.

## What Versa does not collect

- IP address · location · device identifiers
- Account or login information (Versa has no login)
- Usage logs · analytics telemetry · crash reports
- Advertising or tracking SDKs

## Possible future changes

- **Auto-update (Sparkle)**: when introduced, the app will periodically fetch `appcast.xml` from the hosting server. The hosting server's access logs may record the requesting IP.
- **Optional usage analytics**: if introduced, will be strictly opt-in. Lyrics content, track titles, and identifiers will not be transmitted.

Any such change will apply only to new versions and will be reflected in this document.

## Contact

For privacy questions, open an issue at <https://github.com/currenjin/versa/issues>.

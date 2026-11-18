# 오늘의 시간표 탑

자폐성장애 학생을 위한 태블릿용 수업 시간표 구조화 앱이에요.

- 웹앱: GitHub Pages 주소로 열어요. (크롬에서 "앱 설치"도 가능)
- 안드로이드 앱: 이 저장소에 올리면 GitHub Actions가 APK를 만들어 Releases에 올려요.
  태블릿 다운로드 주소: `https://github.com/<아이디>/<저장소>/releases/latest/download/timetable-tower.apk`

## 파일 구성
| 파일 | 하는 일 |
| --- | --- |
| `index.html` | 앱 본체. 위쪽 `TT_CONFIG`에 Supabase 주소와 키를 넣어요. |
| `manifest.webmanifest`, `sw.js`, `icons/` | 웹앱 설치(PWA)와 오프라인 화면용 |
| `app/` | 안드로이드 앱(Capacitor) 설정, 아이콘 원본, 서명 키 |
| `.github/workflows/build-apk.yml` | APK를 자동으로 만드는 설정 |

`app/debug.keystore`는 업데이트할 때 앱을 지우지 않아도 되도록 항상 같은 서명을 쓰기 위한 키예요.
교실에서 직접 설치해 쓰는 용도로만 쓰고, Play 스토어에 올리려면 따로 만든 키를 써야 해요.

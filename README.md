# 제8차 권역계획 동남권 현장실사 협의회(8.20)

동남권(부산·대구·경북·경남) 전략별 관광개발 및 신규 관광(단)지 현장실사 대상지 대시보드.

## 구성

- **전략별 관광개발**: 부산 11개 전략 / 대구 4개 / 경북 6개(개발3+진흥3) / 경남 4개, 세부과제 포함
- **신규 관광(단)지 현장실사 대상 지도**: 동남권 7개소를 지도에 표기, 위치 이미지 팝업 제공
  - 통영 도산관광단지는 문체부 사전협의 완료로 **현장조사 제외**로 표기
- 원본 자료: `26.8.14 제8차 권역계획 현장실사 대상선정을 위한 협의회_ 동남권_최종_krpark.docx`, `위치 그림.docx`

## 파일 구성

| 파일 | 설명 |
|------|------|
| `index.html` | 대시보드 진입점 (단일 파일 · 정적 HTML) |
| `data.js` | 전략·세부과제·현장실사 대상지 데이터 |
| `img_data.js` | 위치 그림 6개(울진/상주/통영/함안 아라가야/악양/평산) — Base64 임베드 |
| `imgs/*.jpg` | 위치 이미지 원본 (참고용) |

## GitHub Pages로 발행하기

1. 이 저장소를 `krparkTourism` 계정 등에 새 public repo로 업로드
   - 저장소 이름 예: `dongnam-tourism-dashboard-820`
2. **Settings → Pages** → **Source: Deploy from a branch** → **Branch: `main` / root** 선택 → Save
3. 1~2분 후 `https://krparkTourism.github.io/<repo>/` 에서 접속 가능

## 로컬 미리보기

```bash
python3 -m http.server 8080
# 브라우저에서 http://localhost:8080 접속
```

외부 의존성: 네이버 지도 API v3 (Client ID 인증), Google Fonts (Noto Sans KR, IBM Plex Sans KR).
데이터·이미지는 모두 로컬 파일에 내장되어 있어 오프라인에서도 지도 타일을 제외한 콘텐츠는 동작합니다.

## 네이버 지도 API 설정

`index.html` 상단의 스크립트 태그에서 `ncpKeyId` 값이 배포 환경의 등록 도메인과 일치해야 합니다.
지도가 표시되지 않는 경우 네이버 클라우드 플랫폼 콘솔의 Application → Web 서비스 URL에
배포 도메인(예: `https://krparktourism.github.io`)이 등록되어 있는지 확인하세요.

## 라이선스

내부 검토용 자료. 배포 전 원본 부처 승인 필요.

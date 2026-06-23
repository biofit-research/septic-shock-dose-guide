# 패혈성 쇼크 약물 가이드

중환자실(ICU)에서 패혈성 쇼크 환자 관리에 쓰는 약물 계산을 한 곳에 모은 웹 도구입니다. 설치 없이 브라우저에서 바로 동작하는 단일 HTML 파일이며, 상단 탭으로 두 기능을 전환합니다.

## 기능

### 1. 약물 주입 변환
- 승압/강심 · 진정 · 진통 · 근이완제 카테고리별 약물 선택
- `mcg/kg/min ↔ cc/hr` 양방향 자동 변환 (어느 쪽에 입력해도 반대값 계산)
- 입력 단위 전환: mcg/kg/min, mcg/kg/hr, mg/kg/hr, mcg/hr, mg/hr, cc/hr
- 앰플(A)·바이알(V)·프리믹스(Bag) 규격 표시
- 믹스 조성 입력: 앰플 용량 × 개수로 총량 자동 계산, 또는 총 약물량·총량 직접 입력
- 약물 선택 시 권장 최소 용량으로 자동 세팅, 체중 기준 권장 범위를 cc/hr로 환산
- 시간당 약물량(mg/hr)·시간당 용량(mcg/hr) 표시

### 2. 신기능 · 항생제 용량 조절
- Cockcroft-Gault 식으로 CrCl 자동 계산 (성별·나이·체중·크레아티닌)
- 검사실 eGFR(MDRD/CKD-EPI) 직접 입력 옵션
- 주요 정맥 항생제의 신기능 구간별 용량표 (계열별 정렬)
- 일반/경증 vs 중증/특수 적응증 전환
- 현재 신기능 구간 자동 강조, 신기능 조절 불필요 약물 표시
- Vancomycin·아미노글리코사이드는 TDM/AUC 관리 안내

## 사용 방법

`index.html`을 브라우저에서 열면 됩니다.

### GitHub Pages 배포
1. 저장소에 파일을 push
2. Settings → Pages → Source를 `main` 브랜치 / `root`로 설정
3. 생성된 URL(`https://<사용자명>.github.io/<저장소명>/`)로 접속

## 파일 구성
- `index.html` — 통합 앱 (약물 변환 + 신기능·항생제)
- `renal.html` — 구버전 호환용 리디렉션 (index.html로 자동 이동)

## 참고문헌
- 약물 농도·믹스: 사용자 제공 ICU 약물 표 기준
- 약물 권장 용량 범위: UpToDate (Lexicomp drug information) 및 일반 ICU 약물 참고서
- 항생제 용량: Stanford Health Care Antimicrobial Dosing Reference Guide, Antimicrobial Stewardship Program (ABX Subcommittee 승인 2026년 2월)
- 신기능 계산식: Cockcroft DW, Gault MH. Prediction of creatinine clearance from serum creatinine. Nephron. 1976;16(1):31-41.

## 주의사항

본 도구는 **참고용 계산기**입니다. 실제 약물 투여와 처방은 반드시 소속 기관 내규, 약제팀, 감염내과 협진과 최신 약품 라벨을 확인한 뒤 진행하십시오. 항생제 용량표는 미국 기관(Stanford) 지침 기반으로, 국내 기관 내규나 약품 라벨과 다를 수 있습니다.

## 라이선스
MIT

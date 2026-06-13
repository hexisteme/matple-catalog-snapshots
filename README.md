# matple-catalog-snapshots

맛플 전국 음식점 **카탈로그 스냅샷** 호스팅. 소스: 지방행정 인허가데이터(LOCALDATA, localdata.go.kr) — 공공 개방데이터(재배포 허용).

- 시도별 `<코드>.json.gz` 샤드 + `manifest.json` 을 **Release asset** 으로 배포.
- 앱은 manifest 버전 확인 후 위치 기준 시도 샤드만 on-demand 다운로드.
- **평점·리뷰 미포함** — 그건 앱에서 런타임 노이즈 read(저장X). 본 스냅샷은 영업/주소/좌표/업태만.

배치: `data_pipeline/build_localdata_snapshot.py` (맛플 앱 레포).

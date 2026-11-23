# 가상 롤러코스터 4DX 시네마

GitHub Pages에서 실행하는 1인칭 롤러코스터 체험 콘텐츠입니다. Three.js로 철로, 지지대, 차량 일부를 생성하고, 배경에는 별도의 PNG 이미지를 사용합니다. **GLB 파일은 필요하지 않습니다.**

## 파일 구성

```text
rollercoaster-4dx/
├── index.html
├── README.md
└── assets/
    └── backgrounds/
        └── rollercoaster-background.png
```

**배경 이미지 경로는 정확히 `assets/backgrounds/rollercoaster-background.png`입니다.** 이미지가 없으면 단색 대체 배경이 표시됩니다.

## 체험 기능

- 1인칭 시점의 출발, 상승, 급강하, 수직 루프, 터널, 도착
- 탑승 시작, 일시정지, 재시작
- 완만 / 보통 / 스릴 모드
- 화면 흔들림 및 소리 켜기/끄기
- PC 및 모바일 웹브라우저 지원

## 배경 구현에 관한 중요 안내

- 배경 PNG는 **실제 에버랜드 T익스프레스 현장 사진이 아닌 생성 이미지**입니다. 특정 시설의 정확한 지형이나 건물 배치를 재현한 것이 아닙니다.
- 배경은 화면 뒤에 고정된 **2D 사진형 레이어**입니다. 카메라가 철로를 따라 움직이더라도 배경에 실제 3D 시차나 원근 변화가 생기지 않습니다.
- 따라서 이 버전은 실제 장소를 3D로 복원한 완성형 시뮬레이터가 아닌, **사진형 배경을 결합한 웹 4DX 스타일 체험의 개선판**입니다.
- 향후 사실적인 전방위 체험을 구현하려면 촬영 허가와 사용 권한이 확보된 여러 시점의 사진/360도 영상, 3D 지형 또는 사진측량 자료가 필요합니다.

## 실행 및 배포

1. GitHub 계정 `imm-content`에 공개 저장소 `rollercoaster-4dx`를 생성합니다.
2. `index.html`, `README.md`를 최상위에 업로드합니다.
3. `assets/backgrounds/rollercoaster-background.png`를 업로드합니다.
4. 저장소 **Settings → Pages → Deploy from a branch → main / (root)**를 선택합니다.
5. 배포 완료 후 `https://imm-content.github.io/rollercoaster-4dx/`에서 실행합니다.

Three.js는 jsDelivr CDN에서 로드하므로 **인터넷 연결이 필요**합니다. 배경 사진의 로딩 여부는 개발자 도구 Network 탭에서 확인할 수 있습니다.

## 안전 및 사용 범위

어지럼증이 있다면 완만 모드를 선택하고 화면 흔들림을 끄십시오. 실제 좌석 움직임, 바람, 물 분사 등 물리적 4DX 장치는 지원하지 않습니다. 브라우저별 오디오 자동 재생 제한으로 소리는 사용자의 시작 버튼 조작 후 활성화됩니다.

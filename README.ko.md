<div align="center">

![Camera Gesture Slides](docs/readme-banner.svg)

# Camera Gesture Slides

손동작·키보드·화면 버튼으로 HTML 발표 자료를 넘깁니다.

[English](README.md) · **한국어**

![project: experiment](https://img.shields.io/badge/project-experiment-c084fc?style=flat-square) ![stack: MediaPipe](https://img.shields.io/badge/stack-MediaPipe-c084fc?style=flat-square)

[Repository](https://github.com/wilgon456/ppt_camera_html)

</div>

---

## 기능

- 검지를 편 채로 좌우로 움직여 슬라이드를 넘깁니다.
- 손바닥을 펴면 이미지가 있는 슬라이드의 사진을 확대합니다.
- 방향키와 이전·다음 버튼으로도 조작할 수 있습니다.
- 발표 화면 배율을 바꾸고 카메라 미리보기를 켜거나 숨깁니다.
- MediaPipe로 손을 인식하고, 얼굴 인식으로 발표자의 손 선택을 돕습니다.

## 로컬 실행

```bash
git clone https://github.com/wilgon456/ppt_camera_html.git
cd ppt_camera_html
python3 -m http.server 8000
```

**http://localhost:8000**을 열고 카메라 시작 버튼을 누른 뒤 접근 권한을 허용합니다. 카메라는 **localhost 또는 HTTPS**에서 사용할 수 있습니다. MediaPipe 스크립트와 모델은 외부 CDN에서 불러옵니다.

## 조작

| 입력 | 동작 |
| --- | --- |
| 왼쪽 / 오른쪽 방향키 | 이전 / 다음 슬라이드 |
| `+` / `-` | 발표 화면 확대 / 축소 |
| 검지 스와이프 | 슬라이드 이동 |
| 손바닥 펼치기 | 현재 슬라이드 이미지 확대 |

## 파일과 한계

`index.html`, `vax_ax_briefing.html`에 발표 자료와 조작 코드가 들어 있습니다. 예제는 `img/` 아래 이미지를 참조하지만, **해당 이미지 파일은 이 저장소에 포함되어 있지 않습니다.** 발표 전에 이미지를 준비하거나 경로를 수정해 주세요. 인식 결과는 조명·카메라 구도·손이 보이는 정도에 따라 달라집니다. 카메라를 시작하지 않아도 키보드로 넘길 수 있습니다.

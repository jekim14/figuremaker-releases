# FigureMaker 배포본.

Precision Food Lab의 논문 figure 제작 앱 FigureMaker의 Windows 설치 파일을 배포하는 저장소다. 소스 코드는 별도 비공개 저장소에 있다.

## 설치.

1. 최신 릴리스의 `FigureMaker-<버전>-Windows.zip`을 받아 새 폴더에 압축을 푼다.
2. `Install.cmd`를 실행한다. `%LOCALAPPDATA%\Programs\PrecisionFoodLab\FigureMaker` 아래 버전별 폴더에 설치되고 시작 메뉴에 바로가기가 생긴다. 관리자 권한과 Python은 필요 없고 Windows WebView2 런타임은 필요하다.

## 자동 업데이트.

앱은 시작할 때 아래 주소의 `latest.json`을 읽어 새 버전이 있으면 ZIP을 내려받아 크기와 SHA-256을 검사한 뒤, 앱을 정상 종료할 때 새 버전 폴더에 설치한다. 이전 버전은 지우지 않는다.

```
https://github.com/jekim14/figuremaker-releases/releases/latest/download/latest.json
```

이 저장소에는 설치 파일만 있으며 연구 데이터는 없다. 앱이 이 주소로 보내는 것은 업데이트 파일 요청뿐이다.

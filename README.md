# frontline-sfx

카드 전략 게임 **전선(FRONTLINE)** 의 음원 파일입니다.
https://frontline-kr.duckdns.org

## 왜 따로 두는가

게임 서버(GCP 영구 무료 등급)는 월 외부 전송량이 1GB 뿐인데 음원이 53MB 입니다.
서버에서 그대로 내보내면 금세 한도가 차므로, 음원만 jsDelivr 로 서빙합니다.

## 사용 방법

```
https://cdn.jsdelivr.net/gh/<계정>/frontline-sfx@v1/sfx/<파일명>.mp3
```

게임 코드에서는 `index.html` 의 `SFX_BASE` 한 줄만 바꾸면 전환됩니다.
빈 문자열로 두면 게임 서버에서 직접 받습니다(폴백도 그렇게 동작합니다).

## 음원을 바꿀 때

파일을 교체·추가하고 **새 태그**(`v2`, `v3` …)를 만든 뒤
`index.html` 의 `SFX_BASE` 안 버전을 함께 올리세요.
jsDelivr 는 태그 단위로 영구 캐시하므로, 같은 태그에 덮어써도 반영되지 않습니다.

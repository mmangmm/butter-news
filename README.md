# Butter 소식

Butter 카메라 앱의 설정 화면 "소식" 칸에 뜨는 글입니다. 앱은 이 저장소의 `news.json`을 읽습니다.

## 글 올리기

1. `news.json`을 열고 연필(편집) 단추를 누릅니다.
2. `"posts": [` 바로 아래에 글 한 덩어리를 넣습니다. 맨 위에 넣으면 됩니다(앱은 날짜순으로 다시 늘어놓습니다).
3. 덩어리 사이에는 쉼표(`,`)가 있어야 합니다.
4. Commit changes로 저장합니다. 앱에 뜨기까지 5분쯤 걸릴 수 있습니다.

```json
{
  "id": "2026-11-01-new-look",
  "date": "2026-11-01",
  "title": { "ko": "새 색감이 나왔어요", "en": "A new look is here" },
  "body":  { "ko": "본문", "en": "Body" },
  "image": "https://…/photo.jpg",
  "link":  { "url": "https://www.instagram.com/mmangmm", "label": { "ko": "인스타그램에서 보기", "en": "See on Instagram" } }
}
```

- `id` — 글마다 달라야 합니다. 새 글 점(주황)을 가르는 데 씁니다. 날짜 + 짧은 이름이면 충분합니다.
- `date` — `YYYY-MM-DD`. 폰의 말로 바뀌어 보입니다.
- `title` — 꼭 있어야 합니다. 나머지(`body`, `image`, `link`)는 없어도 됩니다.
- 말: `ko` `en` `ja` `zh-Hans` `zh-Hant` `es` `fr` `de`. 폰의 말이 없으면 영어 → 한국어 순으로 대신 보여 줍니다.
- `"format": 1`은 바꾸지 않습니다. 파일이 깨지면(쉼표 하나만 빠져도) 앱은 바로 전에 받은 글을 그대로 보여 줍니다.

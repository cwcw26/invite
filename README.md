# 산 너머 삶 — 출판기념 소음악회 초대장

`index.html` 한 장으로 된 초대장입니다. 사진·종이 질감·글꼴 그림은 모두 파일 안에 들어 있어
따로 받아 오는 것이 없습니다.

## 고치는 법

원본은 이 저장소가 아니라 작업 폴더에 있습니다.

```
python3 scripts/build_assets.py versions/책넘김-3d   # 본문·사진을 index.html 로 굽는다
python3 scripts/make_site.py versions/책넘김-3d site # 밖에 올릴 독립 문서로 감싼다
```

그다음 이 저장소에 commit·push 하면 GitHub Pages 가 다시 펴냅니다.

## 표지 판 (`cover/`)

책 표지 그대로 세로로 내려 읽는 판입니다. 배경 음악이 들어 있어 `cover/assets/bgm.mp4` 를
함께 둡니다. 카톡 미리보기 그림은 아티팩트와 달리 여기서는 자동으로 붙지 않으므로
`cover/thumb.jpg` 를 직접 찍어 두고 og 태그로 가리킵니다.

```
python3 scripts/build_assets.py                                    # index.html 을 굽는다
python3 scripts/make_site.py . site/cover                          # 독립 문서로 감싼다
python3 scripts/add_og.py site/cover https://cwcw26.github.io/invite/cover/
cp assets/bgm.mp4 site/cover/assets/bgm.mp4
```

`thumb.jpg` 는 800×420 화면을 1.5배로 찍은 1200×630 그림입니다. 표지를 고쳤으면 다시 찍습니다.

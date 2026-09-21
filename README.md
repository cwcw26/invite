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

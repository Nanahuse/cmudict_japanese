# cmudict_japanese
[CMUdict(the Carnegie Mellon Pronouncing Dictionary)](https://github.com/cmusphinx/cmudict)

英語の発音辞書をカナ読みへと変換したものです。

発音記号を機械的に変換しています。
変な部分があれば教えてください。

# How to use
yaml形式のファイルですが、最初の45行をスキップすることでjsonファイルとしても読み込めます。

```python
# how to use on python
import json

with open("./cmudict_jp_dict.yaml", encoding="UTF-8") as f:
    # skip header (45 line)
    for _ in range(45):
        f.readline()

    # load as json
    dictionary = json.load(f)

print(dictionary["pronounce"])
```

# License
元の辞書のライセンスを引き継ぎ、BSD2条項ライセンスでライセンスされています。
詳しくは[LICENSEファイル](LICENSE)を確認してください。


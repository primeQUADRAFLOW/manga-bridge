# キュウチャへの渡し方（この経路は 2026-09-02 に変わりました）

**もう、この長い文章をコピペする必要はありません。**
キュウチャに渡すのは**URL 1本**だけです。

```
https://raw.githubusercontent.com/primeQUADRAFLOW/manga-bridge/main/ROUND.md
```

このURLは**永久に変わりません**。中身だけが毎回入れ替わります。
キュウチャはここを読めば「今回の依頼」「6人の顔とシートの画像」「守るルール」
「返し方」が全部そろいます。**画像のアップロードも不要**です（URLで参照できます）。

## オーナーがChatGPTへ送る文（これをコピペ）

```
このURLを読んで、書いてある依頼をやってください。
https://raw.githubusercontent.com/primeQUADRAFLOW/manga-bridge/main/ROUND.md
画像もそのページのリンクから参照できます。記憶ではなく、このページを正としてください。
```

## 仕組み

| 向き | 経路 | 自動/手動 |
|---|---|---|
| ピック → キュウチャ | `bridge/_task.md` を書く → `python tools/bridge_publish.py` → ROUND.md が更新される | **全自動** |
| キュウチャ → ピック | キュウチャの出力をオーナーが**受け取りフォルダ**へ入れる → `python tools/inbox_ingest.py` | 半自動（1回だけ人手） |

キュウチャ側から GitHub へ書き込む手段は無いため、**戻りだけはオーナーが1回運ぶ**
（入れる場所は `tools/bridge_common.py` の `INBOX` が正本）。
その1回を確実にするために、返しの形式を `RETURN.md` で固定してある。

## 過去のやりとり

- round1（2026-09-01・沙耶シート修正の依頼）: `bridge/_archive/REPLY_20260901_round1.md`
- 受領と判定の記録: `bridge/CHATGPT_INBOX.md` ／ `management/COLLABORATION_LOG.md`
- v2 の検証（実測値つき）: `bridge/REVIEW_SAYA_v2.md`

## 今回の依頼の中身をここで読みたいとき

正本は `bridge/_task.md`。**編集するのもそこだけ。**
このファイルや ROUND.md を直接書き換えても、次の publish で上書きされる。

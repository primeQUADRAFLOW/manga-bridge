# CURRENT REFERENCES — 現在のマスター画像一覧

**ここに載っている画像が現行のマスター。** 上書き禁止。差し替えは `_v2` として新規保存する。

## 1. 6人集合マスター（顔の最上位ビジュアルマスター）

| ファイル | 内容 | 状態 |
|---|---|---|
| `assets/master/MASTER6_dress_cards.png` | 6人のドレス姿カード（顔アップ＋全身3面） | ⚠ **どちらが「これで決定」版かオーナー未確認** |
| `assets/master/MASTER6_profile_cards.png` | 6人のカード（顔アップ＋全身3面＋目/唇クローズアップ＋身長/誕生日/血液型） | ⚠ 同上 |

> オーナーが「これで決定」とした集合写真が最上位マスター（顔の最終根拠）。
> 上記2枚のどちらか（または両方）がそれに当たる。**確認後に LOCKED を確定させる。**

## 2. 個別キャラクターシート（3パネル・白衣装）

**現行は `_v2`（帯統一版）。** 2026-09-02 にオーナー承認（HD-08 / HD-09 / HD-10）で更新した。

| ID | 名前 | 現行シート | 顔マスター（最優先参照） |
|---|---|---|---|
| 01 | あかり | `assets/characters/01_akari/character_sheet/akari_sheet_v2.png` | `assets/characters/01_akari/master_face/akari_face_v1.png` |
| 02 | しおり | `assets/characters/02_shiori/character_sheet/shiori_sheet_v2.png` | `assets/characters/02_shiori/master_face/shiori_face_v1.png` |
| 03 | 優花 | `assets/characters/03_yuka/character_sheet/yuka_sheet_v2.png` | `assets/characters/03_yuka/master_face/yuka_face_v1.png` |
| 04 | りん | `assets/characters/04_rin/character_sheet/rin_sheet_v2.png` | `assets/characters/04_rin/master_face/rin_face_v1.png` |
| 05 | ほのか | `assets/characters/05_honoka/character_sheet/honoka_sheet_v2.png` | `assets/characters/05_honoka/master_face/honoka_face_v1.png` |
| 06 | 沙耶 | `assets/characters/06_saya/character_sheet/saya_sheet_v3.png` | `assets/characters/06_saya/master_face/saya_face_v2.png` ← **正面** |

### v1 → v2 で何が変わったか

- **01〜05**: 絵は v1 のまま。**上下の帯だけ**を描き直して6枚の形式をそろえた
  （ID表記は2桁に統一＝`MASTER/[[CHARACTER_INDEX]]` と一致させた）。
  再生成は `python tools/rebuild_bands.py`
- **06 沙耶**: 絵そのものがキュウチャの修正版に差し替わった（**左パネルの顔を隠した**）＋帯統一
- **顔マスターは6人とも v1 のまま据え置き**（承認 HD-09）。沙耶 v2 の顔は v1 と同一人物であり、
  v1 の顔アップのほうが正面に近く、固定資料として適するため切り出し直さない

### 06 沙耶は v3 で完了（2026-09-02）

髪色（明るいままアッシュ化: 彩度0.533→0.352／明度0.312→0.389）・完全なかき上げ・
右パネル正面化・胸元を閉じる、すべて達成。顔は同一人物のまま。実測は `bridge/[[REVIEW_SAYA_v3]]`。
**顔マスターも v3 の正面に差し替えた**（06だけ `_face_v2`。他5人は `_face_v1` のまま）。

**正面同士でないと顔の同一性は判定できない。** 斜めのシートしか無い5人については、
`assets/master/MASTER6_profile_cards.png` の各カード中央にある**正面の小パネル**が比較資料になる。

`*_face_v1.png` は、各シートの右パネル（顔アップ）をピックが自動切り出ししたもの。
**個別生成時の顔の最優先参照はこれ。**

## 3. 履歴（現在状態ではない）

| ファイル | 内容 |
|---|---|
| `assets/master/OLD6_sheet_forbidden_names_ARCHIVE.png` | 旧版6人シート。**禁止名（美咲/紫/れい）を含む。** 名前の出典にしない |
| `assets/characters/01_akari/rejected/akari_sheet_altdesign_notselected.png` | あかりのシート別デザイン案。オーナーがINBOXに入れなかった＝未採用 |
| `assets/characters/0X_*/character_sheet/*_sheet_v1.png` | 6枚のシート v1。帯が不統一・06は左パネルの顔が出ている。**現行ではない** |
| `assets/characters/06_saya/character_sheet/saya_sheet_v2_source.png` | 沙耶 v2 の元画像（帯未処理）。再生成の入力 |

## 4. 台帳との対応

すべて `management/[[ASSET_INVENTORY]]` に Asset ID 付きで登録済み（IMG_001〜018 / FACE_001〜006）。
**台帳に載っていない制作物は「存在しない」ものとして扱う。**

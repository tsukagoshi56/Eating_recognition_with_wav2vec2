# Wav2Vec2を用いた食行動音声認識

---

## プロジェクト概要
このプロジェクトは、Wav2Vec2を使用して食行動を認識するモデルの開発を目的としています。

---

## 使用方法

1. **データ準備**  
   `data_prepare` フォルダ内でモデルの学習に必要なデータセットを準備します。

2. **モデルのトレーニング**  
   `model` フォルダ内のスクリプトを使用してモデルをトレーニングします。

```bash
torchrun --nproc_per_node=4 train_with_wav2vec.py config.yaml --find_unused_parameters 
```
--nproc_per_nodeには使用するGPUの数を指定。 --test_onlyを指定すればテストのみ可能。


---

## ディレクトリ構成

- `data_prepare`: データセットを準備するスクリプト
- `model`: モデルの学習と評価に関連するコード

---

## 今後の予定
- モデルの改善
- 他のデータセットでのテスト

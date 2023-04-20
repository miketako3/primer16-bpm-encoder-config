# primer16 with BLE-Pro-Micro and rotary encoder

primer16にBLE-Pro-Microとロータリーエンコーダを組み合わせたときに以下の問題を解決する設定ファイル。

- ロータリーエンコーダの回転をRemapで変更できない。

## 使い方

BLE-Pro-Microは設定ファイルを更新することで動作を直接変更できる。

primer16をUSB接続するとストレージとして認識されるので、そこにある設定ファイルを以下内容で上書きする(ファイル名はそのままで中身だけ置き換えること)。

| 上書き対象       | 上書き内容                 |
|-------------|-----------------------|
| CONFIG.JSN  | primer16_config.json  |
| KEYMAP.JSN  | primer16_default.json |
| ENCODER.JSN | primer16_encoder.json |

すると、Remap上でロータリーエンコーダの回転を変更できるようになる。

ただし、ロータリーエンコーダの時計回り回転はRemap上では表示されないような動作となる (キーマップ自体は変更されている)。
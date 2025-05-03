# ZMK Firmware for SEIBOKU（青墨）

このリポジトリでは、[ZMK Firmware](https://zmk.dev/) による [SEIBOKU（青墨）](https://github.com/snize/BOB-PMW3610-SEIBOKU)のファームウェア例を提供します。

Seeed Studio XIAO nRF52840 を採用し、BLE での接続をサポートしていますが有線での接続も可能です。

本プロジェクトは学習用も兼ねており、できるだけ公式ドキュメントに沿うように作成しました。気になる点あればフィードバックお願いします。

## ファームウェアの書き込み

1. [Releases](https://github.com/snize/zmk-seiboku-example/releases) から最新のファームウェア `seiboku-seeeduino_xiao_ble-zmk.uf2` をダウンロードしてください。
2. PC と XIAO nRF52840 を USB ケーブルで接続します。
3. XIAO nRF52840 のリセットボタンを素早く2回押してブートローダーモードにします。
4. 各OSに合わせたファイラが開くので、ダウンロードしたファームウェアをドラッグ＆ドロップしてください。
5. 以上でファームウェアの書き込みが完了します。

## BLE 接続

通常のBLEデバイスと同様に、PCやスマートフォンから接続することができます。`SEIBOKU`というデバイス名で検出されます。キーマップに`BT_CLR`をアサインしているので、デバイス側のボタンを押すことでペアリング情報を削除することができます。


## 設定変更

本リポジトリのキーボードモジュール化対応完了に伴い、ユーザが設定を変更する場合のためのテンプレートリポジトリ [zmk\-seiboku\-example\-config\-template](https://github.com/snize/zmk-seiboku-example-config-template) を用意しました。このページの右上の Use this template からご自身のリポジトリにコピーを作成し、必要に応じて config 内の `seiboku.conf` や `seiboku.keymap` を変更してください。

ユーザによる設定変更のサンプルとして、SEIBOKUを傾けて取り付けた場合のカーソルの移動量を補正するプロジェクト [zmk-seiboku-config-tilt](https://github.com/snize/zmk-seiboku-config-tilt) を用意しました。

## ビルド

ビルドはGithub Actionsを利用すると環境構築が不要で簡単に行えます。公式のdevcontainerを利用する事もできます。[ZMK Firmwareをdevcontainerでビルドするときのディレクトリ構成｜snize](https://note.com/snize/n/n10310eaeac22)などを参考にしてみてください。

## 免責事項

このファームウェアは無保証です。自己責任でご利用ください。特にBLE接続のためリチウムイオンポリマー電池を使用する場合は、適切な取り扱いを行ってください。

## ライセンス

このリポジトリはMITライセンスで提供されています。詳細は[LICENSE](LICENSE)を参照してください。
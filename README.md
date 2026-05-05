# pico-slcan
RP2040搭載 Low‑Cost CAN FDインターフェース（Windows標準ドライバ対応）

Low‑Cost CAN FD Interface Powered by RP2040 (Uses Windows Built‑in Drivers)

### 特徴
CAN FDは車載・産業用途で広く使われていますが、

- 市販のCAN FDアナライザは高価
- 専用ドライバやSDKが必要
- USB-シリアル（UART）では通信速度がボトルネックになりやすい

といった課題があります。本プロダクトでは、

- MCP2518 + MCP2562FD（SPI接続CAN FDコントローラ）
- RP2040（USBデバイス機能搭載｜Raspberry Pi Picoの主要チップ）

を組み合わせることで、

- 低コスト
- Windows標準ドライバで動作
- USBベース通信により、UARTのボーレート制約に依存しない
- 書き込みソフト変更により任意の動作を実装できる

CAN FD Interfaceを実現します。

特に

- Windows標準ドライバのみで認識
- UARTベースのUSB-シリアル変換を使用しない
- CAN FDフレーム転送時のボトルネックを回避しやすい

というメリットをRP2040のUSB CDC（仮想COM）動作により狙っております。

### 製品
![TopImage](/docs/pico-slcan_Top_Image.png)
![BottomImage](/docs/pico-slcan_Bottom_Image.png)
![TopPhoto_01](/docs/pico-slcan_Top_Photo_01.jpg)
![TopPhoto_02](/docs/pico-slcan_Top_Photo_02.jpg)
<!-- ![TopPhoto](/docs/CAN-FD_4ch_HAT_Top_Photo_02.jpg)
![TopPhoto](/docs/CAN-FD_4ch_HAT_Top_Photo_03.jpg)-->

### 基板の設定
![TopPhoto](/docs/pico-slcan_Top_Image_explanation.png)

- 終端抵抗のあるなしをジャンパスイッチにて切り替えできます。
- IO引き出しブロック／Raspberry Pi Picoデバッグプローブ接続端子／CAN引き出しジャンパピンの部品は拡張IFであり、部品は付属致しません。適時ご用意ください。

### 使用例
![UseCase_01](/docs/UseCase_01.jpg)

- 出荷時は[CANの汎用計測用ソフト]()を書き込み済
  - 拡張対応した[SavvyCAN](https://github.com/TLDSJPWORK/SavvyCAN/releases/tag/V221_JPWORKS_V100)にて利用可能です
  - 動作状況をLCDにて確認できます

### 販売ページ

スイッチサイエンス様にて委託販売を準備中
<!-- - [スイッチサイエンス様](https://ssci.to/10018)-->

### 資料
- [サポートページ](https://github.com/TLDSJPWORK/pico-slcan)
- [回路図](/docs/pico-slcan_sch.pdf)
- [基板図](/docs/pico-slcan_gerber.pdf)
- [上筐体3Dデータ](/docs/pico-slcan_Upper.stl)
- [下筐体3Dデータ](/docs/pico-slcan_Under.stl)
<br><br>

- [RP2040ハードウェア設計資料](https://pip-assets.raspberrypi.com/categories/814-rp2040/documents/RP-008278-DS-1-hardware-design-with-rp2040-JP.pdf?disposition=inline)
- [MCP2518データシート](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/External-CAN-FD-Controller-with-SPI-Interface-DS20006027B.pdf)
- [MCP2526FDデータシート](https://ww1.microchip.com/downloads/aemDocuments/documents/OTH/ProductDocuments/DataSheets/20005284A.pdf) 
<br><br>

- [pico-slcan-soft](https://github.com/TLDSJPWORK/pico-slcan-soft)
- [SavvyCAN pico-slcan対応改造版](https://github.com/TLDSJPWORK/SavvyCAN/releases/tag/V221_JPWORKS_V100)

### 本製品に対する相談先
本デバイスに対するスペック、性能に対するお問い合わせは下記へご相談ください。

- tldsjpwork@gmail.com

<!-- 本デバイスを用いた検討／評価ソリューションをご希望の方は下記へご相談ください。

- [] -->
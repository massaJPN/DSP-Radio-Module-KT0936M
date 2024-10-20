# DSP-Radio-Module-KT0936M(B9)
https://massa4649.booth.pm/items/5751220 の製品説明となります。  

## 概要  
このモジュールは,コントロール用のマイコン不要で手軽にAM放送とFM放送のラジオが楽しめる様に,DSPラジオICとしてKT0936M(B9)を使用しています。  

## 外観  
動作させるための最小限のIC周辺回路部品を実装したモジュール部分と、周波数調整用ボリュームなどの回路部品を実装したオプション回路部分から構成されています。  
モジュール部分とオプション回路部分は結線されていますが、分割可能な仕様となっておりモジュール部分だけを切り離して各自のオリジナル回路に組み込み可能です。  
![DSC_0898-30per](https://github.com/user-attachments/assets/e041a882-cf47-4a82-98d3-5dfec1a336d6)  
全体サイズ：Typ 35.0(L) x 59.0(W) mm  
モジュール部分：Typ 35.0(L) x 20.0(W) mm  

## 回路図  
![kt0936_3_circuit-50per](https://github.com/user-attachments/assets/3e9e724c-bf9f-4328-a693-0c28450533a1)  

以下に回路図の説明をします。KT0936M(B9）のデータシートとともにご参照下さい。  
参考WEBサイト：秋月電子通商  
TOPページ：https://akizukidenshi.com/catalog/c/c0/  
販売コード：117874  

#### 選局/周波数変更  
モジュールの３番端子の電圧を可変させることで所望の周波数チャンネルを選局します。  
受信周波数はモジュールの2番端子に接続する抵抗値で決定します。例えば、1kΩを接続とすると、AM周波数の513KHz～1719KHz、412Ωを接続とすると、FM:63.5MHz～108.5MHzとなります。

#### 音量調節  
ICの機能としてレジスタ設定を変更することで音量調整は可能なようですが、モジュールの1番端子から出力されるオーディオ信号に可変抵抗を結線して音量調整する方式がお手軽で良いと思います。  

#### その他  
オプション回路部分のLEDインジケータを点灯させて受信状態を確認したい場合は、下図の赤線の箇所に抵抗R6と白色LED D1のアノード端子をリード線で半田付けして結線をお願いします。  
![jampwire](https://github.com/user-attachments/assets/e48b2e63-1d04-4f28-a70c-d0d1a0bdd69c)  

## 端子配列  
モジュール端子については、多くの端子をICと直結となっており、配列は以下の通りです。
|端子番号|端子名|I/O|機能|  
|-----|-----|-----|-----|  
|１|AOUT|Analog Output|Audio output|  
|２|SPAN|Analog Input|Band switching control|  
|３|CH|Analog Input|Frequency control pin|  
|４|AM_FM|Digital I/O|default 47Kohm Pull-up resistor.|  
|５|RF_SW|Digital I/O|RF circuit switching control pin.|  
|６|TUNING|Digital Output|Effective instructions|  
|７|VDD|Power|Power　Typ 3.3V（2.1V～3.6V）|  
|８|GND|Ground|Ground|  
|９|AMINP|Analog|MW with LW The positive electrode antenna input|  
|10|AMINN|Analog|MW with LW Antenna negative input|  
|11|RFINP|Rf in|RF input|  

## 使用例  
動画にてご参照下さい。  
オプション回路部分のVR1で音量調整、VR2で周波数調整、SW2でAM,FMバンド切替ができます。  
[![紹介動画]()](https://youtu.be/TwNbtVV50xo)  

## 関連ブログ  
https://massa4649.com/kt0936_3/  

以上です。

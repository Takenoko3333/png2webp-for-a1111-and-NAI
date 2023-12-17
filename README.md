# png2webp-for-a1111-and-NAI
[日本語](#日本語) | [English](#english)

# 日本語

# 説明
## 1. Automatic1111生成画像の変換について
- Automatic1111に取り込むことが可能なメタデータを維持したままPNG(.png)をWEBP(.webp)に変換します。  
- 元画像のメタデータ（PNG Info）はWEBP画像のExifコメントに格納されます。  
- WEBP画像は元画像同様にAutomatic1111のPNG Infoから情報を読み込ませて利用することが可能です。

## 2. NovelAI生成画像の変換について
- NovelAIに取り込むことが可能なメタデータを維持したままPNG(.png)をWEBP(.webp)に変換します。
- 元画像のメタデータはWEBP画像のExifコメントに格納されます。  
- WEBP画像は元画像同様にNovelAIに情報を読み込ませて利用することが可能です。 
- NovelAI生成画像は一般的なメタデータ以外に、特殊な方式で埋め込まれた情報が含まれています。変換後のWEBPはその情報を維持しているためNovelAIに情報を読み込ませて利用することが可能となっています。
- Automatic1111に情報を読み込ませて利用することはできませんが、Automatic1111のPNG InfoやWEBPのExifを閲覧可能なアプリ等で情報を参照することが可能です。  

## 3. 日付情報について
元画像の日付情報を変換後の画像に引き継ぎます。  
- Windows: 更新日時, 作成日時  
- Mac, Linux: 更新日時
<br><br>

# 前提
Python3環境
<br><br>

# 準備
以下のライブラリを使用するため、入っていない場合はインストールします。
- PIL  
~~~
pip install pillow
~~~

- piexif  
~~~
pip install piexif
~~~

Windowsのみ  
- pywin32  
~~~
pip install pywin32
~~~
<br>

# 使い方
1. inputsフォルダに変換したいPNG画像を入れます。  
2. png2webp.batをダブルクリックします。コマンドラインが起動します。  
3. outputsフォルダにWEBP画像が保存されます。コマンドラインが閉じます。
<br><br>

# 設定変更等
- WEBP品質の初期設定は80です。変更したい場合はpng2webp.py内のJPEG_QUALITYを編集してください。  
- 処理完了後にコマンドラインを閉じないようにしたい場合はpng2webp.bat内の@REM pauseのコメントアウトを外してください。
<br><br>

# 変更履歴

## [1.0.0] - 2023-12-17
### 追加
- GitHubで公開
<br><br>

# ライセンス
Copyright © 2023 Takenoko  
Released under the [MIT](https://opensource.org/licenses/mit-license.php) license.
<br><br><br>

# English

# Description
## 1. Conversion of Automatic1111 generated images
- Converts PNG (.png) to WEBP (.webp) while maintaining metadata that can be imported into Automatic1111.  
- The metadata (PNG Info) of the original image is stored in the Exif comment of the WEBP image.  
- The WEBP image can be used in the same way as the original image, by reading the information from the PNG Info in Automatic1111.

## 2. Conversion of NovelAI generated images
- PNG(.png) is converted to WEBP(.webp) while maintaining metadata that can be imported into NovelAI.
- The metadata of the original image is stored in the Exif comment of the WEBP image.  
- WEBP images can be used by loading the information into NovelAI in the same way as the original image. 
- In addition to general metadata, NovelAI-generated images contain information embedded by a special method. The converted WEBP retains this information, so it can be loaded into NovelAI and used.
- Although it is not possible to load the information into Automatic1111, it is possible to refer to the information using Automatic1111's PNG Info or applications that can view WEBP's Exif.  

## 3. About date information
The date information of the original image will be transferred to the converted image.  
- Windows: Modified date, Created date  
- Mac, Linux: Modified date
<br><br>

# Assumptions
Python3 environment
<br><br>

# Preparation
The following libraries are used, so install them if they are not included.
- PIL  
~~~
pip install pillow
~~~

- piexif  
~~~
pip install piexif
~~~

Windows only  
- pywin32  
~~~
pip install pywin32
~~~
<br>

# How to use
1. put the PNG images you want to convert in the inputs folder.
2. Double-click on png2webp.bat. A command line will be launched.
3. WEBP images will be saved in the outputs folder. The command line will close.
<br><br>

# Change settings, etc.
- The default WEBP quality setting is 80. If you want to change it, edit WEBP_QUALITY in png2webp.py.  
- If you do not want to close the command line after processing is complete, uncomment @REM pause in png2webp.bat.
<br><br>

# Change log

## [1.0.0] - 2023-12-17
### Added
- Published on GitHub. 
<br><br>

# License
Copyright © 2023 Takenoko  
Released under the [MIT](https://opensource.org/licenses/mit-license.php) license.



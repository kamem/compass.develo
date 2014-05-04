compass.develo
===========

便利なカスタム関数集

使い方
------
1. config.rbに記述

		require "./rb/develo.rb"



isFile
------
1. isFile('fileName')で ture or false が文字列で返って来ます。
※ fileNameはcompass watch している場所からのパスになります。

2. 実際に使う

		@if isFile('fileName') == 'true' {

		}

fileList
------
* fileList('folderName/\*')でフォルダ内の全てのファイルリストが取得できます。（例えばgifの画像だけを取得したい場合にはfileList('folderName/\*.gif')となります。）
* 初期状態ではcompass watchした場所からのパスを全て表示します。
* 第2引き数にfalseを入れることにより<code>fileList('folderName/*',false)</code>ファイル名 + 拡張子だけを取得することができます。
* 拡張子が必要ない場合には第3引き数に必要のない拡張子を指定します<code>fileList('folderName/\*',false,'.gif')</code>

### 実際に使う
	$images_dir: 'html/img/';
	$imgs: fileList($images_dir + "*.gif",false,'.gif');
	
	.fileList li {
		@each $img in $imgs {
			#{"&." + $img} {
				background: image-url("#{$img}.gif");
			}
		}
	}

ライセンス
----------
+ Copyright 2014 &copy; kamem
+ [http://www.opensource.org/licenses/mit-license.php][mit]

[MIT]: http://www.opensource.org/licenses/mit-license.php

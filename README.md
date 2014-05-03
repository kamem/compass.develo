compass.develo
===========

便利なカスタム関数集


compass.isFile
------

### 仕様・使い方
1. config.rbに記述

		require "./rb/isFile.rb"

2. isFile('fileName')で ture or false が文字列で返って来ます。
※ fileNameはcompass watch している場所からのパスになります。

3. 実際に使う
		
	    @if isFile('fileName') == 'true' {

		}


ライセンス
----------
+ Copyright 2014 &copy; kamem
+ [http://www.opensource.org/licenses/mit-license.php][mit]

[MIT]: http://www.opensource.org/licenses/mit-license.php

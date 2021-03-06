-------------------------------------
Step5: 対話システムを外部に接続しよう
-------------------------------------

対話システムを外部のコンポーネントに接続してみましょう。

対話マネージャへ与えるスクリプトを以下のように編集してください。

  
  sample2.seatml	   

  .. literalinclude:: sample2.seatml

SEATコンポーネントを起動している端末をCtrl+Cなどで停止させて、編集したスクリプトファイルを引数に与えて再度起動します。
  ::

  % seat sample2.seatml

再起動した対話マネージャは出力ポートがひとつ増えています。

  .. image:: step5_02.png

このポートに外部のコンポーネントを接続することで、対話システムからコマンドを出すことができるようになります。

例えば、以下のスクリプトに示されるコンポーネントを接続してみましょう。


  ConsoleOut.py	   

  .. literalinclude:: ConsoleOut.py

このコンポーネントは受け取ったコマンドを端末に表示します。マイクに「こんにちは」「さようなら」と発話することで、音声による応答があると同時に、スクリプトに追加したコマンドが表示されるか確認して下さい。

対話マネージャへのスクリプトを変更することにより、応答メッセージの追加はもちろん、任意のデータタイプのポートを作成し情報を送出できます。この機能を用いることで、例えば外部の車輪型機構コントローラに接続し、「前進」「後退」などの台詞でコントロールするといったことが実現できます。



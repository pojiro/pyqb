QB Process Incubator
=========

## 概要
プロセス管理システムを含むシステムです。

プロセスが停止した時は自動的に同一のコマンドで再起動されます。

## 起動方法
このスクリプトは起動時にコマンドラインそのもの(--targetオプション)
または、コマンドラインを生成する関数(commands())を含むスクリプトを指定(--scriptオプション)します。

起動されたプログラムのワーキングディレクトリがセットされていることは保証されていません。

## --script
--scriptを指定した場合コマンドラインを生成する関数をもつPythonスクリプトを指定することができます。

Pythonスクリプトはcommands()関数を必ず持ち、その返り値は文字列のリストになります。
現状スクリプトは最初の一回のみ呼ばれます。

指定するスクリプトはフルパスが好ましいです。
相対パスで指定した場合正しく動かない可能性があります。

プログラムもシェルを介さない場合はフルパスで指定するべきです。
スクリプトファイルもまた同様です。

## --shell
このオプションをつけるとコマンドの実行がシェルの中で行われます。
不特定のユーザーがこのシステムにコマンドを送りうる場合は指定しないほうが好ましいです。
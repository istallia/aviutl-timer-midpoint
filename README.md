# 中間点制御式タイマースクリプト

公式やサードパーティによって配布されている既存のタイマースクリプトは停止や再開がそれなりに面倒くさい。1、2回止めるくらいならいいが……。  
そこで中間点と瞬間移動を指定したトラックバーを用いて簡単にカウントスピードを制御できるようにしたスクリプトを制作する。  

## 要件

- 中間点で区切ってトラックバーでスピードを設定したら、その通りにカウントが進んだり止まったり戻ったりする
- 表示に関してはなるべく[元のスクリプト](https://github.com/minfia/aviutl_count_timer)の機能を維持する
- カウントのスピードはtrack3で与えられるようにする(単位は1秒間に進むカウント)
- 初期値はdialogの中に押し込む。単位は秒

## 諦めること

- 終点基準のカウント設定
	- 元のスクリプトの大きな特長だったが、中間点制御と両立できない
- 処理の重さ
	- 中間点が増えれば増えるほど見なければならない区間が増えて重くなる
	- 乗算と加算が増えるだけだからそんなに影響はないはず
- エフェクト対応とか
	- そもそも表示まわりは流用するので

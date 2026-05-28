# 🐧 インフラエンジニア向け 実践チートシート＆学習メモ

## 🛠️ コマンドシート（実務で毎日叩くコマンド）

### 1. Linux 必須コマンド
* [cite_start]`pwd` : 自分が今いるディレクトリ（カレントディレクトリ）の絶対パスを表示します [cite: 107][cite_start]。Print Working Directoryの略です [cite: 200]。
* [cite_start]`mkdir` : 新しいディレクトリ（フォルダ）を作成します [cite: 107][cite_start]。Make Directoryの略です [cite: 200]。
* [cite_start]`cd` : 作成したフォルダの中に移動します [cite: 107]。
* [cite_start]`ls -a` : 隠しファイル（.gitなど）も含めて一覧表示するオプションです [cite: 192]。
* [cite_start]`cat` : ファイルの中身をすべて画面に出力して確認します [cite: 107]。
* [cite_start]`grep` : ファイルの中から特定の文字が含まれる行だけを抽出して表示します [cite: 107][cite_start]。ログ調査の主役です [cite: 195]。

### 2. サバイバルVim術
* [cite_start]`i` : 文字を入力するモード（Insertモード）に切り替える [cite: 118]。
* [cite_start]`Esc` : 入力モードを終了して、コマンド待ち状態に戻る [cite: 118]。
* [cite_start]`:wq` : 保存して終了する（Write & Quit） [cite: 118]。
* [cite_start]`:q!` : 保存せずに強制終了する（間違えて設定を消してしまった時などの命綱！） [cite: 118, 119]。

### 3. Git の基本フロー
1. [cite_start]`git init` : Gitの金庫（.gitフォルダ）を作る [cite: 195]。
2. [cite_start]`git add` : 変更をステージング（準備置き場）に上げる [cite: 195]。
3. [cite_start]`git commit` : 変更を金庫に永久保存する [cite: 195]。
4. [cite_start]`git log` : タイムマシンの履歴を確認する [cite: 195]。

---

## 📚 勉強用学習シート（インフラの裏側・知識メモ）

### 💡 コマンドの覚え方のコツ
* [cite_start]**英単語の略で覚える**：コマンドはすべて、ただの英単語の頭文字です [cite: 200][cite_start]。これを知るだけで定着率が10倍変わります [cite: 200]。
* [cite_start]**上矢印（↑）キーを活用**：さきほど打ったコマンドが履歴として呼び出せます [cite: 201][cite_start]。過去の履歴を呼び出して使い回すことで、自然とコマンドの形を指に馴染ませています [cite: 201]。

### 🏢 現場環境の違い（Ubuntu vs Red Hat）
* [cite_start]インフラエンジニアの基礎体力の9割は共通スキルで構成されているため、基本のコマンドやVim、Gitの操作はRed Hatでも全く同じように動きます [cite: 197, 198]。
* [cite_start]ソフトウェアをインストールする時のコマンドだけは異なります [cite: 198]：
  * [cite_start]練習用（Ubuntu等）: `apt` コマンドを使います（例：`sudo apt install vim`） [cite: 198]。
  * [cite_start]現場用（Red Hat等）: `dnf` （または少し古い環境だと `yum` ）というコマンドを使います（例：`sudo dnf install vim`） [cite: 198]。

### 🕰️ タイムマシン（Git）の正体
* [cite_start]変更履歴が保存された場所は、フォルダの中に隠されている `.git` という秘密のフォルダの中です [cite: 192]。
* [cite_start]最新のファイルが1つあるだけで、過去のすべての記憶はこの `.git` フォルダの中にギュッと圧縮されてしまわれています [cite: 193]。

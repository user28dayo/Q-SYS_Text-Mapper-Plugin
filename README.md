# Q-SYS Text Mapper Plugin

## 概要 (Overview)
入力されたあらゆるシグナル（True/False、数値、文字列）を判定し、事前に設定した任意のカスタム文字列に変換して出力する Q-SYS 用のカスタムプラグインです。
システムの生データを人間が読みやすい状態（例: `再生中`、`停止`）に変換したり、外部機器へ送信する特定のコマンドを生成したりする際に役立ちます。

## 特徴 (Features)
* **柔軟な入力対応:** String（テキスト）、Boolean（トグルボタン等）、Value（数値）のどのデータ型が入力されても、自動的に文字列として安全に処理・判定します。
* **動的なルール設定:** プロパティ（Properties）の `Mapping Count` から、変換ルールの数を 2〜20 個まで自由に増減可能です。
* **フォールバック保護:** どの条件にも当てはまらない想定外のシグナルが入力された場合に備え、デフォルトで出力する文字（Fallback Text）を設定できます。
* **リアルタイム反映:** Q-SYSのエミュレーション中やコアの実行中でも、GUI上でルールを書き換えるだけで即座に変更が適用されます。

## インストール方法 (Installation)
1. 本リポジトリから `TextMapper.qplug` をダウンロードします。
2. ご使用のPCの以下の Q-SYS プラグインフォルダにファイルを配置します。
   `C:\Users\[あなたのユーザー名]\Documents\QSC\Q-Sys Designer\Plugins`
3. Q-SYS Designer Software を再起動します。
4. 右側の Schematic Elements ペインにある **User Plugins** フォルダから `user28dayo Text Mapper` を回路図にドラッグ＆ドロップして配置します。

## 使い方 (Usage)
1. **ピンの数の調整:** ブロックを選択し、右側の Properties ペインから `Mapping Count`（変換ルール数）を指定します。
2. **変換ルールの作成:** プラグインのコントロールパネルを開き、各行に以下を設定します。
   * **Match:** 入力と一致させたい値（例: `true`, `1`, `Error` など）
   * **Text:** 一致した際に出力したい文字列（例: `On`, `Low`, `エラー発生` など）
3. **デフォルト値の設定:** 一番上の `Default Fallback` 欄に、どの Match 条件にも合致しなかった場合に出力する文字（例: `Unknown` や 空白）を入力します。
4. **注意点:** テキストボックスに文字を入力した後は、必ず `Enter` キーを押すか別の場所をクリックして入力を確定させてください。

## 作者 (Author)
* **user28dayo**

## 動作確認環境 (Tested Environment)
* Q-SYS Designer Software v9.x.x （※ご自身が使っているバージョンに書き換えてください）

## ライセンス (License)
This project is for personal use. / MIT License

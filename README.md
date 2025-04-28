# Steamゲームプレイ時間取得ツール

このツールは、Steam APIを使用して、あなたのSteamアカウントで所有しているゲームのプレイ時間やその他の情報を取得し、テキストファイルに出力します。

## 機能

- Steam APIを使用して、所有ゲームのプレイ時間、最終プレイ日時、ジャンル、カテゴリなどの情報を取得します。
- プレイ時間0分のゲームは除外して表示します。
- 最終プレイ日時順にソートして表示します。
- 取得した情報は `output_detailed.txt` というファイルに出力します。

## Google Colabでの使用方法

1. このノートブックをGoogle Colabで開きます。
2. コードを実行する前に、以下の手順でSteam APIキーとSteamIDを設定してください。
    - Steam APIキーの取得:
        1. Steam Developersポータル にアクセスします。
        2. Steamアカウントでログインします。
        3. "Register for a Steam Web API Key" をクリックします。
        4. ドメイン名を入力します (任意)。
        5. 利用規約に同意して "Register" をクリックします。
        6. 表示された "Key" がSteam APIキーです。
    - SteamID64の取得:
        1. SteamプロフィールページのURLから確認できます。
        2. 例：`https://steamcommunity.com/profiles/XXXXXXXXXXXXXX/`
        3. 上記のURLの場合、SteamIDは `XXXXXXXXXXXXXX` です。
3. コードの先頭にある `userdata.set()` を使用して、APIキーとSteamIDを設定します。

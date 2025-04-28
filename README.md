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
4. コードを実行します。
5. 処理が完了すると、結果が `output_detailed.txt` に保存されます。

## 注意

- Steam APIのレート制限により、多数のゲームを所有している場合、処理に時間がかかることがあります。
- Steamプロフィールのゲーム詳細が非公開になっている場合、ゲームリストを取得できません。
- このツールは、非公式であり、Steamの利用規約に違反する可能性があります。自己責任でご利用ください。

## 免責事項

このツールは、Steamの提供するAPIを利用していますが、Steamとは一切関係ありません。
このツールの使用によって生じた損害について、作者は一切の責任を負いません。

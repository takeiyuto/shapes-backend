# Shapes Backend

[Shapes NFT](https://github.com/takeiyuto/shapes) のバックエンドです。

## 前提条件

このレポジトリの親ディレクトリに、`blockchain` という名称で [Shapes NFT のコントラクト](https://github.com/takeiyuto/shapes-contract)のプロジェクトがあること。また、コントラクトはコンパイルされて、デプロイ済みであること。詳細は、[徹底解説 NFTの理論と実践](https://www.ohmsha.co.jp/book/9784274230608/)の第9章2節を参照してください。

## 動作方法

1. このレポジトリをクローンし、ライブラリをダウンロードします。
```bash
git clone https://github.com/takeiyuto/shapes-backend.git backend
cd backend
yarn
```

2. コントラクトの型情報を生成します。
```bash
yarn type
```

3. [server.ts](./server.ts) の 9 行目にある以下のような `address` 定数に、既にデプロイしてある Shapes NFT コントラクトのアドレスを記述します。
```ts
const address = "0x...CONTRACT_ADDRESS...";
```

4. `.secret` というファイルに、Shapes NFT のコントラクトのデプロイに用いたアカウントの秘密鍵 (**ニーモニックではありません**) を記載します。MetaMask をお使いの場合、[ヘルプページ (英語)](https://support.metamask.io/hc/en-us/articles/360015289632-How-to-export-an-account-s-private-key) に表示方法が説明されています。
<img src="https://support.metamask.io/hc/article_attachments/9025953096603/How_to_export_an_account_s_private_key.gif" width="200px">

5. コンパイルした後、バックエンドを起動します。
```bash
yarn build
yarn serve
```

6. Shapes NFT の[フロントエンド](https://github.com/takeiyuto/shapes-frontend)を起動します。起動の方法は、[Shapes Frontend の README.md](https://github.com/takeiyuto/shapes-frontend/blob/main/README.md) を参照してください。

7. バックエンドは Ctrl + C で終了できます。

## ライセンス表示

このサンプル コードは、[MIT License](LICENSE)で提供しています。

# 参照

[徹底解説 NFTの理論と実践](https://www.ohmsha.co.jp/book/9784274230608/)の第9章3節を参照してください。[本書の Web サイト](https://takeiyuto.github.io/nft-book)も参考にしてください。

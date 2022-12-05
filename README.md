# fastlabel-sretest-auth

## 課題

AWSを用い以下のアーキテクチャにて運用しているシステム(SaaS)があります。

![Architecture](/architecture.png)

認証基盤には `Auth0` を用いていますが、

- プライベートクラウド(AWS)への対応

を行うことになり、前提条件として認証基盤にAuth0以外の代替案が必要になりました。  
このケースにおける代替方法を提示してください。

AWSには認証サービスとしてCognitoがありますが、  
それ以外にOSSも選択肢として入れてもらって構いません。

## 前提条件
Auth0にて以下の機能を利用中とします。

- メールアドレス/パスワード による認証
- Google/GitHubソーシャルログイン による認証
- MFA
  - Google Authenticator(TOTP)によるMFA
  - メールアドレスドメイン単位でMFA要・不要を切り替える
- パスワードポリシー
  - 文字数は8文字以上
  - 大文字、小文字、数値、記号の4種のうち3種を必ず含めるように
- [CloudWatchへのログ出力](https://auth0.com/docs/customize/extensions/export-log-events-with-extensions/export-logs-to-cloudwatch)
- メールアドレスのエクスポート

## 提出方法
面接の日までに課題を終わらせ、当日ご自身が考えた解決策をご説明ください。  
必要に応じて作成した資料などを用い、画面共有にてご説明をお願いいたします。

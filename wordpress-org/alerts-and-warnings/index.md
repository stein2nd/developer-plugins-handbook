<!--
# Alerts and Warnings
-->

# アラートと警告

<!--
When you visit plugin pages on WordPress.org, you may notice special alerts or warnings. These exist to help visitors understand the status of various plugins.
-->

WordPress.org のプラグインページにアクセスすると、特別なアラートや警告が表示されることがあります。これらは、さまざまなプラグインの状態を、訪問者が理解しやすくするために存在します。

<!--
## Approved and Pending Data
-->

## 承認済みおよび保留中のデータ

<!--
![Blue background - This plugin is approved and awaiting data upload but not visible to the public yet. Once you make your first commit, the plugin will become public.](https://developer.wordpress.org/files/2018/02/approved.jpg)
-->

![青色の背景 - このプラグインは承認され、データのアップロードを待っていますが、まだ公開されていません。最初のコミットを行うと、プラグインは公開されます。](https://developer.wordpress.org/files/2018/02/approved.jpg)

<!--
Plugins that have been approved but no code has yet been uploaded will see this message:This _only_ displays to the plugin owner and will go away once code has been pushed via SVN.
-->

プラグインが承認されたが、コードがまだアップロードされていない場合、このメッセージが表示されます: このメッセージはプラグインの所有者に **のみ** 表示され、Subversion (SVN) 経由でコードがプッシュされると消えます。

<!--
## Closed
-->

## クローズ

<!--
As of November 2017, plugins that are closed display a notice:
-->

2017年11月現在、クローズしたプラグインには、お知らせが表示されます:

<!--
![Red background: This plugin has been closed and is no longer available for download.](https://i3.wp.com/developer.wordpress.org/files/2018/02/closed.png)
-->

![赤色の背景: このプラグインは既にクローズされ、もうダウンロードできません。](https://i3.wp.com/developer.wordpress.org/files/2018/02/closed.png)

<!--
This is viewable by all visitors and indicates a plugin was closed. Plugins closed after January 2018 will include a date:
-->

これはすべての訪問者が見ることができ、プラグインがクローズされたことを示します。2018年1月以降にクローズされたプラグインには、日付が表示されます:

<!--
![Red background: This plugin was closed on February 7, 2018 and is no longer available for download.](https://i3.wp.com/developer.wordpress.org/files/2018/02/closed-alt.jpg)
-->

![赤色の背景: このプラグインは2018年2月7日にクローズし、もうダウンロードできません。](https://i3.wp.com/developer.wordpress.org/files/2018/02/closed-alt.jpg)

<!--
After 60 days, the alert will be updated to explain _why_ the plugin was closed:
-->

60日後、警告はプラグインがクローズされた **理由** を説明するために更新されます:

<!--
![Alert detailing why a plugin was closed](https://i3.wp.com/developer.wordpress.org/files/2018/02/why-closed.png)
-->

![プラグインがクローズされた理由を、詳細に示す警告](https://i3.wp.com/developer.wordpress.org/files/2018/02/why-closed.png)

<!--
Plugin committers will see the following additional note:
-->

プラグインの開発コミッターには、以下の追記が表示されます:

<!--
![Blue background: If you did not request this change, please contact plugins@wordpress.org for a status. All developers with commit access are contacted when a plugin is closed, with the reasons why, so check your spam email too.](https://i3.wp.com/developer.wordpress.org/files/2018/02/closed-owner.png)
-->

![青色の背景: この変更をリクエストしていない場合は、plugins@wordpress.org に連絡してステータスを確認してください。プラグインがクローズされたときには、コミット権限のある開発者全員にその理由とともに連絡されますので、迷惑メールもチェックしてください。](https://i3.wp.com/developer.wordpress.org/files/2018/02/closed-owner.png)

<!--
### Reasons why plugins are closed
-->

### プラグインがクローズされる理由

<!--
- Author Request – the author has asked the plugin to be closed.
- Guideline Violation – a violation of any of the guideline.
- Licensing/Trademark Violation – non-GPL code in use, or trademarks are being misused.
- Merged Into Core – the plugin is now a part of core (reserved for feature projects).
- Security Issue – a security concern has been found in this plugin.
-->

- 作者からの依頼 – 作者がプラグインをクローズするよう要請しました。
- ガイドライン違反 – ガイドラインのいずれかに違反しています。
- ライセンス/商標違反 – 非 GPL コードが使用されていたり、商標が誤用されていたりします。
- コアにマージ – プラグインはコアの一部になりました (機能プロジェクトのために予約されていました)。
- セキュリティ問題 – このプラグインにセキュリティの懸念が見つかりました。

<!--
Additional details on why a plugin is closed are not provided to anyone outside the WordPress.org security team or the plugin authors, unless there is an extreme circumstance.
-->

プラグインがクローズされた理由の追加の詳細は、極端な事情がない限り、WordPress.org セキュリティチームやプラグイン作者以外の人には提供されません。

<!--
## Out of Date
-->

## 期限切れ

<!--
Plugins that do not support the last 3 major releases of WordPress have the following notice:
-->

WordPress の直近3メジャーリリースに対応していないプラグインは、以下の注意書きが表示されます:

<!--
![Yellow background: This plugin hasn’t been tested with the latest 3 major releases of WordPress. It may no longer be maintained or supported and may have compatibility issues when used with more recent versions of WordPress.](https://i3.wp.com/developer.wordpress.org/files/2018/02/old.jpg)
-->

![黄色の背景: このプラグインはWordPressの最新の3つのメジャーリリースでテストされていません。メンテナンスまたはサポートが終了している可能性があり、WordPress の最新バージョンで使用すると、互換性の問題が発生する可能性があります。](https://i3.wp.com/developer.wordpress.org/files/2018/02/old.jpg)

<!--
Previously this message alerted users to plugins not updated within the last 2 years. In 2018 it was modified to rely on more pertinent data. Since WordPress updates major releases 2 to 3 times per year, and a maintained a plugin should be testing with the recent versions, this alert can be avoided by updating a plugin readme when new versions of WordPress is released.
-->

以前は、このメッセージは過去2年以内に更新されていないプラグインをユーザーに警告していました。2018年には、より適切なデータにもとづいて修正されました。WordPress は年に2～3回メジャーリリースを更新しており、メンテナンスされたプラグインは最近のバージョンでテストされているはずですので、WordPress の新バージョンがリリースされた際にプラグインの readme を更新することで、この警告を回避できます。

<!--
Developers are emailed before every major release of WordPress and asked to update this value. They _do not_ need to push a new version, just [update the readme](https://developer.wordpress.org/plugins/wordpress-org/how-your-readme-txt-works/) and edit the value of `Tested up to:` to the latest version of WordPress.
-->

WordPress のメジャーリリースのたびに、開発者は、この値を更新するようメールで依頼されます。開発者は新しいバージョンをプッシュする **必要はなく**、[readme を更新](https://ja.wordpress.org/team/handbook/plugin-development/wordpress-org/how-your-readme-txt-works/) して、`Tested up to:` の値を WordPress の最新バージョンに編集するだけです。

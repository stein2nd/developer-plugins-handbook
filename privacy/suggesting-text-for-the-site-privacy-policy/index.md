<!--
Suggesting text for the site privacy policy
-->

サイトのプライバシーポリシー用の文章の提案
-------------------------------------------

<!--
Every plugin that collects, uses, or stores user data, or passes it to an external source or third party, should add a section of suggested text to the privacy policy postbox. This is best done with `wp_add_privacy_policy_content( $plugin_name, $policy_text )`. This will allow site administrators to pull that information into their site’s privacy policy.
-->

ユーザーデータを収集、使用、保存したり、外部ソースやサードパーティに渡したりするプラグインはすべて、プライバシーポリシーの投稿ボックスに推奨テキストのセクションを追加する必要があります。これは `wp_add_privacy_policy_content( $plugin_name, $policy_text )` で行うのがベストです。これにより、サイト管理者はその情報を自分のサイトのプライバシーポリシーに取り込むことができます。

<!--
To make this simpler for the users, the text should address the questions provided in the default privacy policy:
-->

ユーザーにとってより簡単なものにするために、テキストはデフォルトのプライバシーポリシーで提供されている質問に対応する必要があります:

<!--
- What personal data we collect and why we collect it
	- Their own manually input information
	- WP: Contact forms
	- WP: Comments
	- WP: Cookies
	- WP: Third party embeds
	- Analytics
- Who we share your data with
- How long we retain your data
- What rights you have over your data
- Where we send your data
- Your contact information
- How we protect your data
- What data breach procedures we have in place
- What third parties we receive data from
- What automated decision making and/or profiling we do with user data
- Any industry regulatory disclosure requirements
-->

- 当社が収集する個人データとその理由
	- 独自の手入力情報
	- WP: コンタクトフォーム
	- WP: コメント
	- WP: Cookie
	- WP: 第三者の埋め込み
	- アナリティクス
- お客様のデータを共有する相手
- お客様のデータの保持期間
- お客様のデータに関する権利
- データの送付先
- お客様の連絡先情報
- お客様のデータの保護方法
- 当社が実施しているデータ侵害手続き
- 当社がどのような第三者からデータを受領しているか
- 当社がユーザーデータを使用して行う、自動化された意思決定および/またはプロファイリングについて
- 業界規制による開示要件

<!--
While not all of these questions will be applicable to all plugins, we recommend taking care with the sections on data sharing.
-->

これらの質問のすべてがすべてのプラグインに当てはまるわけではありませんが、データ共有に関するセクションには注意することをおすすめします。

<!--
## Code Example
-->

## コード例

<!--
[info]It is recommended to call [`wp_add_privacy_policy_content()`](https://developer.wordpress.org/reference/functions/wp_add_privacy_policy_content/) during the [admin_init](https://developer.wordpress.org/reference/hooks/admin_init/) action. Calling it outside of an action hook can lead to problems, see ticket [#44142](https://core.trac.wordpress.org/ticket/44142) for details.[/info]
-->

[info]アクション [admin_init](https://developer.wordpress.org/reference/hooks/admin_init/) 中に、[`wp_add_privacy_policy_content()`](https://developer.wordpress.org/reference/functions/wp_add_privacy_policy_content/) を呼び出すことを推奨します。アクションフック外で呼び出すと問題が発生する可能性があり、詳細はチケット [#44142](https://core.trac.wordpress.org/ticket/44142) を参照してください。[/info]

<!--
[info]Supplemental information can be provided through the use of the specialized `.privacy-policy-tutorial` CSS class. Any content contained within HTML elements that have this CSS class applied will be omitted from the clipboard when the section content is copied.[/info]
-->

[info]特別な CSS クラス `.privacy-policy-tutorial` を使うことで、補足情報を提供できます。この CSS クラスが適用された HTML 要素に含まれるコンテンツは、セクションの内容がコピーされる際に、クリップボードから省かれます。[/info]

```
/**
 * Adds a privacy policy statement.
 */
function wporg_add_privacy_policy_content() {
  if ( ! function_exists( 'wp_add_privacy_policy_content' ) ) {
    return;
  }
  $content = '<p class="privacy-policy-tutorial">' . __( 'Some introductory content for the suggested text.', 'text-domain' ) . '</p>'
  . '<strong class="privacy-policy-tutorial">' . __( 'Suggested Text:', 'my_plugin_textdomain' ) . '</strong> '
  . sprintf(
    __( 'When you leave a comment on this site, we send your name, email address, IP address and comment text to example.com. Example.com does not retain your personal data. The example.com privacy policy is <a href="%1$s" target="_blank">here</a>.', 'text-domain' ),
    'https://example.com/privacy-policy'
  );
  wp_add_privacy_policy_content( 'Example Plugin', wp_kses_post( wpautop( $content, false ) ) );
}

add_action( 'admin_init', 'wporg_add_privacy_policy_content' );
```

---
categories: blog
title: 新型コロナウイルス接触追跡アプリのための倫理的指針
subtitle: 正しいアプリが正しく作られているかを評価するための16の問い
description: この4月にオックスフォード・インターネット研究所とアラン・チューリング研究所に所属する四人の研究者たちが共同で新型コロナウイルス接触追跡アプリのための倫理的指針（ガイドライン）を発表しました。共著者には情報倫理学で知られるルチアーノ・フロリディ教授がいます。
show_description: true
# thumbnail: /images/blog/2020-03-07-cyber-anti-ageism/thumbnail.jpg
---

> 失敗の繰り返しや高過ぎるコストが市民の信頼を裏切ることにつながる以上、政府には正しく介入するチャンスがただの一度しか与えられていないというべきです。
{:.big-quote}

## 訳者まえがき

COVID-19のパンデミックは当面収束の目処が立たず、第二波・第三波の到来も予見されている中で、各国は接触追跡アプリの開発に取り組んでいます。日本でも「接触確認アプリ」の開発が発表されました。安倍首相は5月25日に緊急事態宣言を全国で解除し、[記者会見](https://www.kantei.go.jp/jp/98_abe/statement/2020/0525kaiken.html)で接触確認アプリの利用を広く呼びかけました：

> 　こうした取組を重ねてもなお、感染者の増加スピードが再び高まり、最悪の場合には、残念ながら２度目の緊急事態宣言発出の可能性もあります。しかし、私は、外出自粛のような社会経済活動を制限するようなやり方はできる限り避けたいと考えています。市中感染のリスクを大きく引き下げていけば、それが可能となります。
> 
> 　そして、そのためには、感染者をできるだけ早期に発見するクラスター対策を一層強化することが必要です。その鍵は、接触確認アプリの導入です。スマートフォンの通信機能により、陽性が判明した人と一定時間近くにいたことが判明した方々、すなわち濃厚接触の可能性が高い皆さんに自動的に通知することで、早期の対策につなげるアプリです。
> 
> 　先月、オックスフォード大学が発表したシミュレーションによれば、このアプリが人口の６割近くに普及し、濃厚接触者の早期の隔離につなげることができれば、ロックダウンを避けることが可能となる大きな効果が期待できるという研究があります。我が国では、個人情報は全く取得しない、安心して使えるアプリを、来月中旬をめどに導入する予定です。どうか多くの皆さんに御活用いただきたいと思います。

このように接触追跡アプリの効果に期待が寄せられる一方、プライバシー上の問題が多くの専門家から指摘されています。この4月にオックスフォード・インターネット研究所とアラン・チューリング研究所に所属する四人の研究者たちは共同で新型コロナウイルス接触追跡アプリのための倫理的指針（ガイドライン）を発表しました。共著者には情報倫理学で知られるルチアーノ・フロリディ教授がいます[^fn-floridi]。この指針は、情報倫理上の様々な論点を含む包括的なフレームワークです。日本版「接触確認アプリ」の設計・実装・運用を市民が監視・検証する上でも、この指針が役に立つはずです。

[^fn-floridi]: フロリディ教授は[忘れられる権利](https://ja.wikipedia.org/wiki/%E5%BF%98%E3%82%8C%E3%82%89%E3%82%8C%E3%82%8B%E6%A8%A9%E5%88%A9)に関する[グーグル諮問委員会](https://archive.google.com/advisorycouncil/)のメンバーを務めた人物です。私は[2013年のブログ記事](/activity/2013/08/22/luciano-floridi-study-2013-08-20.html)や[2017年の書評](/activity/2017/05/12/floridi-talk.html)で彼のことを紹介したことがあります。今回は[英国版接触追跡アプリの倫理諮問委員会](https://nhsbsa-socialtracking.powerappsportals.com/EAB%20Letter%20to%20NHSx.pdf)の委員も務めています。


以下に掲載するのは、あくまでも抄訳かつ意訳です。訳出を省略した箇所もありますので、正確な内容については原文をあたってください。全体で6ページの短い論文です。訳出の底本としては5月24日付でフロリディ教授から直接ご提供頂いた版を用いました。現時点で公開されている版とは差異があるかもしれません。以上、ご了承ください。［追記：[5月28日付の別バージョンがNatureに掲載されました。](https://www.nature.com/articles/d41586-020-01578-0)］

なお、この論文で “Digital Tracking and Tracing (DTT) Systems” と呼ばれているものは、一般的には “contact tracing apps” （接触追跡アプリ）と呼ばれています。また、日本政府が開発中のものは「接触確認アプリ」と呼ばれています。各国の状況については[平和博氏の5月15日の記事](https://news.yahoo.co.jp/byline/kazuhirotaira/20200515-00178594/)で詳しく紹介されています。

［抄訳ここから］

Ethical Guidelines for SARS-CoV-2 Digital Tracking and Tracing Systems  
by Jessica Morley, Josh Cowls, Mariarosaria Taddeo, Luciano Floridi  
Available at SSRN: <https://ssrn.com/abstract=3582550> or <http://dx.doi.org/10.2139/ssrn.3582550>

# サマリー

世界保健機関は目下の新型コロナウイルス(SARS-CoV-2)が第二次世界大戦以来最大の世界的危機を引き起こしたとして2020年3月11日にCOVID-19のグローバル・パンデミックを宣言しました。この記事では、感染の可能性がある個人を追跡するデジタルシステムの使用が、単に合法であるだけでなく倫理的であるかどうか、およびどの程度まで倫理的なのかを評価するためのフレームワークを提示します。デジタル追跡システムは、基本的人権と自由を厳しく制限する可能性がありますが、それらが倫理的に正当化できること、つまり社会の期待や価値観と一致していることを保証するためには、なんら指針のないまま展開されるべきではありません。介入は特定の公衆衛生目標を達成するために**必要**でなければならず、公衆衛生上の脅威の深刻さに**比例**しなければならず、その有効性を支持するために**科学的に正しく**なければならず、**時限的**でなければなりません([1](#ref1), [2](#ref2))。それでもなお十分とは言えません。この論文では、倫理的なDTTシステムの設計と開発をガイドする12の要素を含む、より包括的なフレームワークを提示します。  

# COVID-19 DTTシステムの倫理的リスク

COVID-19パンデミックによって物質空間とデジタル空間の両方における政府の異常な介入が余儀なくされました。物質空間においては移動や集会の自由を制限し、デジタル空間においては大量のデータを収集して有効な対策を導き出すために。COVID-19 Digital Rights Trackerによると世界中で43の接触追跡アプリが利用可能となっています（4月20日時点）([3](#ref3), [4](#ref4))。これらのシステムの中には、位置情報や健康状態（症状、感染確認）などの個人情報や、他者との接触情報を収集しうるものも含まれます。危機の拡大に伴ってDTTシステムの開発を求める声も増え続けています。欧州だけでも、欧州データ保護監督当局が欧州統一アプリを呼びかけました([5](#ref5))。欧州委員会はDTTシステムの開発を支援する「ツールボックス」を定義しました([6](#ref6))。PEPP-PTやDP-3Tなどのプロトコルは欧州レベルで開発中です([7](#ref7))。イタリアは接触追跡アプリを開発中です([8](#ref8))。英国NHSXも同等のアプリを計画中です([9](#ref9), [10](#ref10))。一方、アップルとグーグルは、世界中での接触追跡を支援するAPIとOSレベルの技術に共同で取り組んでいます([11](#ref11))。

COVID-19の潜伏期間の長さと、無症状者からの感染拡大のリスクを踏まえれば、DTTシステムが潜在的感染者の自主隔離を促進することで、パンデミックの早期収束に貢献する可能性はあります([6](#ref6), [12](#ref12)-[14](#ref14))。この場合、ある程度の基本的人権や自由の制限も倫理的に正当化され得ます。同様に、DTTシステムを**使わないこと**が非倫理的となり得るかもしれません。しかし、それには個別具体的なDTTシステムの倫理的側面の入念な検討を要します。とは言え、状況が刻々と変わる中での分析は困難です。政府がパンデミックへの緊急対応に取り組む中、倫理的な考察など表面的で二の次だと見られてしまえば、より一層の困難につながります。ですが、倫理的に正当化し得ないDTTシステムの開発は、無駄なだけでなく、危険でさえあります。社会的混乱、ネットリンチ、政府や公衆衛生当局への信頼低下も、問題を深刻化します。さらには、接触追跡アプリにより収集されたパーソナル・データが、それ以外の非倫理的な用途に用いられることで、深刻かつ不可逆なインパクトをもたらす危険性もあります。したがって、このようなグローバル危機の時にあっても、倫理的リスクを考慮し、それらを回避・最小化するための適切な指標を持たなければなりません。

# 倫理的に正当化しうるDTTシステム設計開発指針

EUや国連の様々な原理原則[^fn-principles]が、感染症の拡大を抑えるための基本的人権の制限は**時限的**で、**必要性**・**比例原則**・**科学的正しさ**の基準を満たすべきだとしています。我々もまたDTTシステムはこれらの原理原則に依拠すべきだと考えます。これらの基礎の上に、DTTシステムの倫理的正当性を評価するための16の問いを開発しました。

[^fn-principles]: The European Convention on Human Rights、the United Nations International Covenant on Civil and Political Rights、the United Nations Siracusa Principles

フレームワーク（図1）は**高次原則**と**実現要因**に分かれています。高次原則は先述の4項目であり、「**正しい**DTTシステムが開発されていますか？」という問いになります（エンジニアリングでは製品の「妥当性確認」（バリデーション）として知られます）。一方、実現要因は、より具体的なDTTシステムについての、「**正しく**開発されていますか？」という問いになります（エンジニアリングでは製品の「検証」（ベリフィケーション）として知られます）。実現要因は、長年の普遍的な高次原則（**何を？**）を、DTTシステムの設計者と展開者のための実用的で現場的な配慮事項（**どのようにして？**）に翻訳します。実際のDTTがどの程度倫理的に正当化しうるものかの目安として、それぞれの問いへの回答に「＋」（より良い）と「ー」（より悪い）のマークを付けました。達成すべき倫理的基準が（理論的に、可変のものとして）存在しますが、達成度は単なる「＋」の数だけでなく、様々な状況（コンテキスト）を踏まえた上で評価されなければなりません。その判断は最終的には政治的なものとなります。DTTシステムの展開における様々なコンテキスト次第で倫理的正当性は変わりやすく、例えばシンガポールのようにデジタル・リテラシーが高い小国で正当化できるアプリを、人口が多くデジタル・デバイドが深刻な英国に持っていくことはできないでしょう。また、パンデミックの状況や人々の態度が変わることで、昨日は倫理的に正当化できたことが、明日には正当化できなくなってしまうかもしれません。したがって、この指針の問いは定期的に繰り返されるべきです。

図1. DTTシステムの倫理的設計を確認するためのフレームワーク

［図1ここから］

## DTTが倫理的に正当化できる範囲を決定するための質問

### 高次原則（質問に答えてください：正しいDTTシステムが開発されていますか？）   

#### 1) 必要な解決策ですか？

\+ はい、人命を救うためにアプリを開発する必要があります。

\- いいえ、より良い解決策が利用できます。

#### 2) それは問題に比例した解決策ですか？[^fn-prop]
[^fn-prop]: 達成されるべき目的とそのために取られる手段としての私権制限が釣り合っているかを問う比例原則のこと。

\+ はい、DTTシステムの潜在的な悪影響は、状況の深刻さによって正当化されます。

\- いいえ、DTTシステムの潜在的な負の影響は状況に不釣り合いです。  

#### 3) 科学的に正しいですか？

i) 効果的になりますか？  
ii) タイミングは「正しい」ですか？  
iii) 採用率は十分に高くなりますか？  
iv) 正確になりますか？

\+ はい、システムが機能し、タイムリーな解決策であり、十分な数の人々に採用され、正確なデータとインサイトをもたらすであろうとエビデンスが示しています。

\- いいえ、アプリはうまく機能せず、稼動は遅すぎるか早すぎて、広く採用されることはなく、（偽陽性や偽陰性が多すぎて）正確性において不十分なデータを収集しそうです。

#### 4) 一時的なものですか？

\+ はい、明示的かつ合理的なサンセット条項[^fn-sunset]があります。

[^fn-sunset]: サンセット条項とは、サービス終了やシステム廃棄に関する条項。

\- いいえ、終了日は定義されていません。  

### 実現要因（質問に答えてください：DTTシステムは正しく開発されていますか？）  

#### 5) 自発的ですか？

\+ はい、アプリのダウンロードとインストールは任意です。

\- いいえ、無駄に義務化されており、従わなければ制裁が適用されるかもしれません。

#### 6) 同意が必要ですか？

\+ はい、いつどのデータが共有されるかは完全にユーザーの選択に委ねられていますし、その選択はいつでも変更できます。

\- いいえ、アプリのデフォルトのデータ設定は「ずっとすべてを共有」ですし、この設定を変更することはできません。  

#### 7) データは非公開にされ、ユーザーの匿名性は保たれますか？

\+ はい、データは完全に匿名で、ユーザーの電話上にのみ保存されます。接触したとされる相手には、感染につながる恐れのある接触があったことのみが通知され、どこの誰かは通知されません。これを保証するため、差分プライバシーなどの手法が用いられます。サイバー・レジリエンスは高いです。[^fn-cyber-resilience]

[^fn-cyber-resilience]: サイバー・レジリエンスとは、サイバー攻撃を早期に検知し復旧する能力。

\- いいえ、データ収集レベルの問題で、データは完全に（再）識別可能であり、集中的に保存されています。接触場所も利用可能です。サイバー・レジリエンスは低いです。  

#### 8) ユーザーはデータを消去できますか？

\+ はい、ユーザーは自分の意思でデータを削除できますし、いずれにせよ全てのデータがサンセット時に削除されます。（問4参照）

\- いいえ、データを削除する手段はありませんし、データが削除される保証もありません。  

#### 9) 目的は定義されていますか？

\+ はい、明確に定義されています。感染が確認された人と接触した場合にのみ個人に通知されます。必須データ（確認された健康状態と接触時刻）のみが収集されます。

\- いいえ、利用規約は緩やかに定義されており、データが二次的な、ほとんど関連性がない目的に使用されないという保証はありません。収集されたデータは他のデータベースと組み合わされるかもしれません。ユーザーが制御できず、透明性もなく、複数のデータソースが収集されるかもしれません。

#### 10) 目的は限定されていますか？

\+ はい、アプリは感染の追跡という目的にのみ用いられます。

\- いいえ、アプリは定期的に更新され、機能追加される可能性があります。

#### 11) 予防のためだけに使用されますか？

\+ はい、このアプリは人々の自発的な拡散防止のためだけに使用されます。（「曲線の平坦化」）

\- いいえ、アプリは人々が福利厚生を申請したり、職場に戻ったりできるようにするためのパスポートとしても使用されます。（「第二波への備え」）

#### 12) 従わせるために使用されますか？

\- いいえ、アプリは人々に行動を強制するためには用いられません。

\+ はい、アプリは人々の行動を監視するために使用され、従わない人は罰せられる可能性があります。（罰金や勾留・禁固刑により）

#### 13) オープンソースですか？

\+ はい、アプリのソースコードは公開され、設計のすべての側面が検査でき、共有でき、コラボレーションによる改善が促進されます。

\- いいえ、アプリのソースコードは利用できません。また、アプリに関する情報が他の形式で提供されることもありません。  

#### 14) 平等に利用できますか？

\+ はい、アプリはダウンロードして使用したい人に無料で広く配布されています。

\- いいえ、アプリは選択されたユーザーにのみ恣意的に提供されます。  

#### 15) 平等にアクセスできますか？

\+ はい、アプリは技術に詳しくない人にもユーザー・フレンドリーであり、できる限り広汎な携帯電話で動作します。

\- いいえ、アプリを使用できるのは、特定の携帯電話を持ち、特定のデジタル・エコシステムの一部に属し、十分なデジタル教育を受けている人だけです。  

#### 16) システムを廃止する終末プロセスはありますか？

\+ はい、アプリの正式な廃止処理のための明確なロードマップがあります。

\- いいえ、アプリのライフサイクルの最終段階を管理するための適切なポリシーはありません。

［ここまで図1］

DTTシステムの倫理的正当性は状況に依存しますので、システムの（企画から廃棄までの）全ライフサイクルと、パンデミックの進展も考慮に入れる必要があります。例えば、状況によってはアプリの利用が任意であるという性質については一考の余地があります。科学的な有効性を獲得するためにはアプリの利用率が人口の60%に達しなければならないところ、人々の自発性に任せて利用率20%に止まったとしたら（アクセスしにくさや信頼不足などの理由で）。利用率の低さは、単にシステムの有効性を無くすだけでなく、間違った安心感を与えたり、個人特定のリスクを高めたり、プライバシーを毀損したり、ネットリンチの恐れを高めたりします。紙上の設計では倫理的に正当だと思えたものが、効果がないだけでなく、必要性もなければ、（比例性を満たさない）不釣り合いなものにもなるのです。同様に、アプリがサイバー攻撃に曝されれば、良くて効果がない、悪ければ危険なシステムに成り下がります。これらの理由から、DTTシステムがもはや必要でない、有用でない、倫理的に正当でない状況になったときのために、適切な出口戦略が必要です（問16）。システムが失敗したら、速やかにその出口戦略を実行しなければなりません。**いつまでに**するかという明確な期限と、**誰が**プロジェクト全体を評価し、必要なら停止したり、改善したり、刷新したりするのかの明確な取り決めも、極めて重要です。

# 上手くやるチャンスは一度だけ

普通でないときには普通でない手段が必要です。とは言え、深刻な危機が何もかもを正当化するわけではありません。フィジカルとデジタル両方の空間において、基本的人権と自由は依然として保護されるべきであり、その保護を確かなものにするためのガイダンスが速やかに必要です。

すでに見てきたように、必要性、比例性、科学的正しさ、時限性の4原則を満たすDTTシステムの倫理的正統性は、追加で定義した12個の実現要因をどの程度満たしたかにも依存します。たとえDTTシステムの方法論や、正当性や、理論的アプローチが［4原則において］妥当（バリッド）でも、実際の状況を鑑みて［12要因において］設計案の正しさを検証（ベリファイ）できないなら、そのシステムを使うべきではありません。というのも、DTTシステムを稼働させるか否かの選択において直面している状況とは、上手くいけば賞賛され、失敗すれば特に害はないといった「どちらに転んでも構わない」ような状況ではないからです。粗末な設計や限定的な検証にも関わらずDTTを稼働させようとする政府は、「なんでもやってみよう」の精神を示すためにそうしようとするのであり、それゆえ批判を無視し、あらゆる犠牲を払ってでもやりかねません。これは危機の時にあっては危険なことです。間違ったDTTシステムがもたらす外部性には、基本的人権や自由への害も含まれます。これは将来の政府にも禍根を残します。COVID-19状況においては、（あらゆる意味での）コストは高く、「外部性」として無視できません。それは現在の人口と政府を深く速く直撃し、問題全体を悪化させる恐れがあります。なぜなら、倫理的に正しくない類いのDTTシステムは、単に効果がないだけでなく、解決を模索している問題それ自体を劇化させるかもしれないからです。失敗の繰り返しや高過ぎるコストが市民の信頼を裏切ることにつながる以上、政府には正しく介入するチャンスがただの一度しか与えられていないというべきです。倫理的分析は、リスクと機会に光を当て、緊急の意思決定を、社会を支える長年の価値観と、統治の適切な領域設定に関する社会の期待に合わせるためのコンパスを提供します。ですから危機の時にあっても倫理的な慎重さが成功には不可欠なのです。

# 参考文献

1. <a name="ref1"></a>EDPB. Statement by the EDPB Chair on the processing of personal data in the context of the COVID-19 outbreak [Internet]. 2020 [cited 2020 Mar 30]. Available from: <https://edpb.europa.eu/news/news/2020/statement-edpb-chair-processing-personal-data-context-covid-19-outbreak_en>
2. <a name="ref2"></a>Ada Lovelace Institute. COVID-19 Rapid Evidence Review: Exit through the App Store? [Internet]. 2020 Apr [cited 2020 Apr 20]. Available from: <https://www.adalovelaceinstitute.org/our-work/covid-19/covid-19-exit-through-the-app-store/>
3. <a name="ref3"></a>Top10vpn. Covid Digital Rights Tracker [Internet]. Available from: <https://www.top10vpn.com/news/surveillance/covid-19-digital-rights-tracker/>
4. <a name="ref4"></a>Knight W. Phones Could Track the Spread of Covid-19. Is It a Good Idea? 2020 Mar 15; Available from: <https://www.wired.com/story/phones-track-spread-covid19-good-idea/>
5. <a name="ref5"></a>Wiewiórowski W. EU Digital Solidarity: a call for a pan-European approach against the pandemic Wojciech Wiewiórowski [Internet]. 2020 [cited 2020 Apr 20]. Available from: <https://edps.europa.eu/sites/edp/files/publication/2020-04-06_eu_digital_solidarity_covid19_en.pdf>
6. <a name="ref6"></a>European Commission. COMMISSION RECOMMENDATION of 8.4.2020 on a common Union toolbox for the use of technology and data to combat and exit from the COVID-19 crisis, in particular concerning mobile applications and the use of anonymised mobility data. Brussels; 2020 Apr. 
7. <a name="ref7"></a>Troncoso C, Payer M, Hubaux J-P, Salanthe M, Larus J, Bugnion E, et al. Decentralized Privacy-Preserving Proximity Tracing [Internet]. 2020 Apr [cited 2020 Apr 12]. Available from: <https://github.com/DP-3T/documents/blob/master/DP3T%20White%20Paper.pdf>
8. <a name="ref8"></a>Pollina E, Goodman D. Italy Tests Contact-Tracing App to Speed Lockdown Exit. New York Times [Internet]. 2020 Apr 17 [cited 2020 Apr 20]; Available from: <https://www.nytimes.com/reuters/2020/04/17/technology/17reuters-health-coronavirus-italy-technology.html>
9. <a name="ref9"></a>Downey A. NHSX working on coronavirus contact tracking app. Digital Health [Internet]. 2020 Mar 20 [cited 2020 Mar 30]; Available from: <https://www.digitalhealth.net/2020/03/nhsx-coronavirus-contact-tracking-app/>
10. <a name="ref10"></a>Keilon L. Coronavirus: UK confirms plan for its own contact tracing app. BBC News [Internet]. 2020 Apr 12 [cited 2020 Apr 16]; Available from: <https://www.bbc.co.uk/news/technology-52263244>
11. <a name="ref11"></a>Keyword team. Apple and Google partner on COVID-19 contact tracing technology [Internet]. Google. 2020 [cited 2020 Apr 11]. Available from: <https://blog.google/inside-google/company-announcements/apple-and-google-partner-covid-19-contact-tracing-technology/amp/>
12. <a name="ref12"></a>ECDC. Novel Coronavirus disease 2019 (COVID-19) pandemic: increased transmission in the EU/EEA and the UK - sixth update [Internet]. 2020 Mar [cited 2020 Mar 30]. Available from: <https://www.ecdc.europa.eu/sites/default/files/documents/RRA-sixth-update-Outbreak-of-novel-coronavirus-disease-2019-COVID-19.pdf>
13. <a name="ref13"></a>Ferretti L, Wymant C, Kendall M, Zhao L, Nurtay A, Abeler-Dörner L, et al. Quantifying SARS-CoV-2 transmission suggests epidemic control with digital contact tracing. Science [Internet]. 2020 Mar 31 [cited 2020 Apr 6];eabb6936. Available from: <https://www.sciencemag.org/lookup/doi/10.1126/science.abb6936>
14. <a name="ref14"></a>Keeling MJ, Hollingsworth TD, Read JM. The Efficacy of Contact Tracing for the Containment of the 2019 Novel Coronavirus (COVID-19). [Internet]. Public and Global Health; 2020 Feb [cited 2020 Mar 27]. Available from: <http://medrxiv.org/lookup/doi/10.1101/2020.02.14.20023036>

［抄訳ここまで］
<html lang="ja">
    <head>
        <meta charset="utf-8" />
    </head>
    <body>
        <h1><center>Trend Watching: Grokking</center></h1>
        <h2>なにものか？</h2>
        <p>
素人が野次馬的に Grokking の研究動向を眺めてみることにした。
        </p>
<h3>Grokking とは</h3>
<p>
機械学習モデルがトレーニングデータを暗記して、十分に一般化できないものの、長期間のトレーニング後に突然ほぼ完璧な一般化に移行する現象のこと。
</p>
<center><img src="images/grokking.png"></center>
</p><p>

日本語の「腑に落ちる」「腹落ちする」に該当するそうで、何故か興味がある。<br>
「Grokking」という用語は、ロバート・ハインラインのSF小説「異星の客」から借りてきたものとのこと(未読)<br>
</p>
<h3>動向</h3>
<p>
たぶん、こんな感じ。
</p> 
<center><img src="images/trend.png"></center>
</p><p>
<div class="styleBullet">
<ul><li>
ResNet-18でGrokkingを再現させるコードが公開されている。
<a href="https://github.com/Qihuai27/Grokking-Insight">https://github.com/Qihuai27/Grokking-Insight</a><br>
(私の環境だと学習済ResNet-18パラメータのダウンロードに失敗し動作未確認)
</li><br><li>
[7] 埋め込み層からの Grokking のメカニズム的洞察<br>
AIによる要約は<a href="https://www.alphaxiv.org/ja/overview/2505.15624v1">こちら</a><br>
機械的分析により、ニューラルネットワークにおけるグロッキング現象の主な要因が埋め込み層であることが明らかになりました。
本研究では、埋め込みパラメータに異なる学習率を適用するAdam-LRという改良されたオプティマイザを提案しており、これにより更新量のバランスを取り、初期化に対する感度を緩和することで、グロッキングを加速させます。
    
</li><br><li>
[6] GrokAlign: グロッキングの幾何学的特徴付けと高速化<br>
AIによる要約は<a href="https://www.alphaxiv.org/ja/overview/2506.12284v1">こちら</a><br>
グロッキングの遅延汎化とロバストネスという二重の側面を統一する、初のメカニズム的説明を提供します。
</li><br><li>
[4] Let Me Grok for You: Accelerating Grokking via Embedding Transfer from a Weaker Model (2025)<br>
AIによる要約は<a href="https://www.alphaxiv.org/ja/overview/2504.13292v1">こちら</a><br>
<br>
GrokTransferはまず、より小さく弱いモデルをトレーニングし、自明ではない（しかし最適には程遠い）テスト性能に到達させます。次に、この弱いモデルから学習された入力埋め込みを抽出し、ターゲットとなるより強力なモデルへの埋め込みを初期化するために使用します。<br>
<br>
<strong>弱いモデルから強いモデルへの知識伝達の原則に基づいており、より単純なモデルからの洞察が、より複雑なモデルの学習をブートストラップできます。</strong><br>
<br>
(「知識蒸留」は強いモデル(教師モデル)の知識を使って、弱いモデル(生徒モデル)の学習を支援するけど、その逆ってこと? 面白い。)
</li><br><li>
[5] Where to find Grokking in LLM Pretraining? Monitor Memorization-to-Generalization without Test (2025)<br>
AIによる要約は<a href="https://www.alphaxiv.org/ja/overview/2506.21551v1">こちら</a><br>
大規模言語モデル（LLM）の実用的な大規模事前学習において、グロッキングは発生するのでしょうか？
小規模モデルで見られたグローバルで同期的なグロッキングとは異なり、LLMのグロッキングは<strong>局所的かつ非同期</strong>であることを発見した。
</li><br><li>
[3] Grokfast: Accelerated Grokking by Amplifying Slow Gradients (2024)<br>
AIによる要約は<a href="https://www.alphaxiv.org/ja/overview/2405.20233v2">こちら</a><br>
Grokfastは、勾配の低周波成分を選択的に増幅することにより、グロッキングとして知られる遅延汎化現象を、さまざまな深層学習タスクにおいて最大50倍加速させる。

</li><br><li>
[2]Unified View of Grokking, Double Descent and Emergent Abilities: A Perspective from Circuits Competition　(2023)<br>
AIによる要約は<a href="https://www.alphaxiv.org/ja/overview/2402.15175v2">こちら</a>
    
</li><br><li>
[1] Bridging Lottery ticket and Grokking: Is Weight Norm Sufficient to Explain Delayed Generalization? (2023)　東大松尾研
日本語版は<a href="https://www.jstage.jst.go.jp/article/pjsai/JSAI2024/0/JSAI2024_1B4GS203/_pdf/-char/ja">こちら</a>

</li><br><li>
[0] Grokking: Generalization beyond overfitting on small algorithmic datasets (2022)<br>
最初に「グロッキング」現象を発見し、命名し、調査した論文<br>
AIによる要約は<a href="https://www.alphaxiv.org/ja/overview/2201.02177v1">こちら</a>
</li></ul></div>
</p>
    </body>
</html>

# ゲノム配列データベースの使い方 at AJACS千里

情報・システム研究機構 ライフサイエンス統合データベースセンター  
[坊農 秀雅](http://bonohu.jp/) bono@dbcls.rois.ac.jp  
2015年6月16日 大阪大学吹田キャンパス  

----

これは統合データベース講習会AJACS千里「ゲノム配列データベースの使い方」の資料です。   

----

## 概要

本講習は、だれでも自由に使うことができる公共データベース(DB)のうちゲノム配列に関してウェブツールを活用して、研究のさまざまな場面で使う方策について学びます。    

----

## 講習の流れ
今回の講習では、コンピュータを使って以下の内容について説明します。

- 研究現場で頻繁に使われるデータベースやツールを知る
- ゲノム配列を探す
	- NCBI
	- GOLD
- ゲノム配列から探す
	- Web上で
		- BLAST
		- GGGenome
	- Local BLASTで(今回はやらない)
- アノテーションを足して見る
	- UCSCのtrack
		- ENCODE TF Binding
		- TFBS Conserved
		- Resetのやり方
	- Ensemblへジャンプ
		- Synteny
		- Resequencing


----

##### 講習に際しての注意とお願い

- みんなで同時にアクセスするとサイトにつながりにくくなることが予想されます。
    - 資料を見ながら自力で進められそうな方はどんどん先に、そうでない方は講師と一緒にすすめていきましょう。
    - サイトの反応が悪い時はタイミングをずらして実行してみてください。
    - 反応が無いからと言って何度もクリックするとますます繋がらなくなってしまいます。おおらかな気持ちで臨みましょう。
- わからないことがあったら挙手にてスタッフにお知らせください。
    - 遠慮は無用です(そのための講習会です!)。おいてけぼりは楽しくありません。
- 質問や個別の相談がある方は講習時間が終わったあとでも講師を捕まえて話してください。
 
----

## 研究現場で頻繁に使われるデータベースやツールを知る
### [統合TV](http://togotv.dbcls.jp/)
- 生命科学分野の有用なデータベースやツールの使い方を動画で紹介するウェブサイト
    - http://togotv.dbcls.jp/
[![統合TVトップページ](http://i.gyazo.com/457d7a15c537adc10d9b99596447508f.png)](http://gyazo.com/457d7a15c537adc10d9b99596447508f)

    - YouTube版もあります　http://www.youtube.com/user/togotv/videos
[![統合TVYouTube支店](http://i.gyazo.com/4c4ffa07ba8a0ea1846a2e76be02284e.png)](http://gyazo.com/4c4ffa07ba8a0ea1846a2e76be02284e)
    - ウェブサイトへのアクセスから結果の見方まで、操作の一挙手一投足がわかります。
        - 講義・講習などの参考資料や後輩指導の教材として利用できます。
        - 本講習中、本家サイトが繋がらない時は、統合TVのYouTube版を見ればおおよその内容がわかるようになっています。
        - 今回の講習に関連する内容の多くは、[統合TV の発現制御解析 カテゴリー](http://togotv.dbcls.jp/ja/contents/category/expression)にあります。
        - 過去の講習会の内容はそのほとんどが[統合TVに収録](http://togotv.dbcls.jp/ja/contents/category/dbcls#%E7%B5%B1%E5%90%88%E3%83%87%E3%83%BC%E3%82%BF%E3%83%99%E3%83%BC%E3%82%B9%E8%AC%9B%E7%BF%92%E4%BC%9Aajacs-%E8%AC%9B%E6%BC%94%E3%83%BB%E8%AC%9B%E7%BF%92%E5%8B%95%E7%94%BB)されており、いつでもどこでも繰り返し復習できるようになっています。
    - お探しの動画が見つからない or 統合TV未掲載の場合は、[統合TV番組リクエストフォーム](https://docs.google.com/forms/d/15pxJHnsV_Cu8B55Xy0F3jg5S9FXupkbBqONrZsyUE7k/viewform)へどうぞ!!
    - 統合TVを作ってみたい方、募集中です。

----

## ゲノム配列を探す

さまざまな生物種のゲノム配列が解読されています。それを自らの研究に利用しない手はありません。その利用の第一歩としてそれを探してくる方法を学びます。

### NCBI
- NCBI(National Center for Biotechnology Information)
	- http://www.ncbi.nlm.nih.gov/
- アメリカ合衆国の予算による分子生物学情報のリソース
- いろんな調べ物、基本ここから

####【実習1】NCBIからゲノム配列を検索、取得する

1. **中東呼吸器症候群**の原因ウイルスのゲノム配列を取得しましょう。日本語しかわからない場合は、NBDCの[データベース横断検索](http://biosciencedbc.jp/dbsearch/)から英語名を調べましょう。その結果、出てくる``Middle East respiratory syndrome``でNCBIから検索します
[![Gyazo](http://i.gyazo.com/4b14584d8cae14de8717a5b1b31d21af.png)](http://gyazo.com/4b14584d8cae14de8717a5b1b31d21af)


2. 検索結果を見ましょう。それぞれのDBの横にある数字は、検索ヒット数です。ゲノム配列が得たいので、``Genome``の項目(ヒット数1件)をクリックして詳細を取得します 
[![Gyazo](http://i.gyazo.com/47eb9d97e16a18f02ee7930ed57a254a.png)](http://gyazo.com/47eb9d97e16a18f02ee7930ed57a254a)


3. Middle East respiratory syndrome coronavirusのゲノム構造と各種リンクが表示されます。``RefSeq``のところにあるIDをクリックするとRefSeq(リファレンス配列(Reference Sequence)のデータベース)のレコードが表示されます
[![Gyazo](http://i.gyazo.com/fcc3c14b8158238233cd4b6087866db8.png)](http://gyazo.com/fcc3c14b8158238233cd4b6087866db8)

4. 得られるRefSeqのレコードを見ましょう。ゲノムにコードされているタンパク質配列などを確認しましょう。
5. そのレコードの一番下にゲノム配列が記述されています。ゲノム塩基配列を抜き出すには、最上部の``FASTA``をクリックします
[![Gyazo](http://i.gyazo.com/cd454ae926b1299e37680aaa7dc1906f.png)](http://gyazo.com/cd454ae926b1299e37680aaa7dc1906f)


6. MERSコロナウイルスのゲノム配列が得られました!
[![Gyazo](http://i.gyazo.com/20fe76da0752e3b5abafcb632c3f69db.png)](http://gyazo.com/20fe76da0752e3b5abafcb632c3f69db)

### GOLD

- GOLD(Genomes Online Database)
	- https://gold.jgi-psf.org/
-  ゲノム塩基配列解読プロジェクトを集めたデータベース
- すでに終了したプロジェクトだけでなく、現在進行中のゲノムプロジェクトやメタゲノムプロジェクトについても調べることができます

####【実習2】GOLDでゲノム配列解読された生物種を検索する
(詳細な手順は統合TV([GOLD -Genomes Online Database- の使い方](http://togotv.dbcls.jp/20150515.html))にあります。それと同じ内容を以下の実習でやりますので、動画を見ながらやっていただくのも手です)

1. [GOLD(Genomes Online Database)](https://gold.jgi-psf.org/)にアクセスします
[![Gyazo](http://i.gyazo.com/cb4596511a204cdf873684bca2c8e7a2.png)](http://gyazo.com/cb4596511a204cdf873684bca2c8e7a2)

2. 上部のメニューバーの中のSearchをクリックします
3. NCBI BioProject Nameに``Thiobacillus``と入力して、下部にあるSearchをクリックします
[![Gyazo](http://i.gyazo.com/d71d28b4f10d846481dcc6d6cc5806c1.png)](http://gyazo.com/d71d28b4f10d846481dcc6d6cc5806c1)


4. ``Select Fields``をクリックして出てくるサブウィンドウで``Is Public``と``GC Percent``にチェックを入れて、そのウィンドウ最下部のSubmitをクリックします
[![Gyazo](http://i.gyazo.com/f52ab7595bf8f4cba9da750ccbcde6fa.png)](http://gyazo.com/f52ab7595bf8f4cba9da750ccbcde6fa)

5. こんな結果が出てきます。Project Statusでゲノム配列解読の状況がわかります
[![Gyazo](http://i.gyazo.com/e0c763b2341d254201242270a2ed2136.png)](http://gyazo.com/e0c763b2341d254201242270a2ed2136)


6. 出てくるテーブルの``GC Percent``をクリックするとGC含量でレコードがソートされます
[![Gyazo](http://i.gyazo.com/abb304ed59a039ab8d503949dea7fbc2.png)](http://gyazo.com/abb304ed59a039ab8d503949dea7fbc2)

7. 一番上に出てくる``Gp0003885``をクリックして出てくる詳細画面を眺めましょう。``Sequencing Information``,``Organism Information``, ``Organism Metadata``タブをクリックしてどういった情報が載せられているか確認しましょう
[![Gyazo](http://i.gyazo.com/a97df74b44377f1bc79d8eac4be2296c.png)](http://gyazo.com/a97df74b44377f1bc79d8eac4be2296c)

8. ``Project Information``タブに戻り、``NCBI BioProject ID``のリンクをクリック
[![Gyazo](http://i.gyazo.com/29bd21effb67cfcacb487a767872e762.png)](http://gyazo.com/29bd21effb67cfcacb487a767872e762)

9. リンク先は前述のNCBIのBioProjectのページで``SEQUENCE DATA``の数字をクリックすれば、前述同様、ゲノム配列が取得できます

[【復習用】GOLD -Genomes Online Database- の使い方(統合TV)](http://togotv.dbcls.jp/20150515.html)

----
##ゲノム配列から探す
ゲノム配列が得られてもその中から欲しい領域を目で見つけてくること(眼grep(「めグレップ」)と呼んでいます)は容易ではありません。そこで、コンピュータの力を借りることになります。

### Web上で
- BLAST(Basic Local Alignment Search Tool)
	- http://blast.ncbi.nlm.nih.gov/
	- 前世紀から使われている配列類似性検索のデ・ファクト・スタンダード
	- かつては遠縁の配列相同性を検出するためのツール
	- 今はほぼ完全一致を探すために用いられることも多い

[![Gyazo](http://i.gyazo.com/0805e3f1ea046192de5a52cac47dce58.png)](http://gyazo.com/0805e3f1ea046192de5a52cac47dce58)
(スライド出典: [「配列解析基礎」 by 坊農秀雅](http://www.slideshare.net/sayamatcher/140905bono))

####【余談】なぜ相同性じゃなく類似性か
- 遺伝学では、相同性という言葉はタンパク質のアミノ酸配列や遺伝子の塩基配列が共通の祖先をもつときに用いる
- バイオインフォマティクスでは、タンパク質やDNAでの相同性は、配列類似性に基づいて判断される
	- http://togetter.com/li/307635
	
[![Gyazo](http://i.gyazo.com/883c9871790d3a201513809d9eb38adc.png)](http://gyazo.com/883c9871790d3a201513809d9eb38adc)

- 現在(2015年6月)のBLASTウェブインターフェース
	- Assembled Genomesに対する生物種ごとのBLAST検索が上位に
	- Basic BLAST(以下に説明)が下の方に

[![Gyazo](http://i.gyazo.com/cf4ffab8417471c36c940d2c31fdbf40.png)](http://gyazo.com/cf4ffab8417471c36c940d2c31fdbf40)
(スライド出典: [「配列解析基礎」 by 坊農秀雅](http://www.slideshare.net/sayamatcher/140905bono))

- GGGenome
	- 「じぇじぇじぇのむ」と読みます(参考: [GGRNA](http:/ggrna.dbcls.jp/)(「ぐぐるな」))
	- http://gggenome.dbcls.jp/
	- 上記のAssembled Genomesに対する高速検索のツール
	
####【実習3】GGGenomeを使ってゲノム配列から探す

1. http://gggenome.dbcls.jp/ にアクセスします
[![Gyazo](http://i.gyazo.com/f0ffa1901878ade96d9f4274b235eb86.png)](http://gyazo.com/f0ffa1901878ade96d9f4274b235eb86)

2. ``CTGACGGTCA``(10塩基)を入力して「検索」ボタンを押します。この塩基配列がヒトゲノム中で何回出てくるか、簡単にわかります
[![Gyazo](http://i.gyazo.com/ca47196af2a9e98a291a7a68ff69177d.png)](http://gyazo.com/ca47196af2a9e98a291a7a68ff69177d)

3. 検索ボタンの右にある生物種を``S.cerevisiae``にして検索しなおしましょう。ヒット数はどう変化するでしょうか?
[![Gyazo](http://i.gyazo.com/0d519de6d1c0fa8982ff55d8e3b9eae3.png)](http://gyazo.com/0d519de6d1c0fa8982ff55d8e3b9eae3)

4. 染色体と位置のところにリンクがあり、これをクリックするとUCSC Genome Browserの該当箇所になります。その使い方は次節で説明します

- [【復習用】高速配列検索 GGGenome《ゲゲゲノム》の使い方(統合TV)](http://togotv.dbcls.jp/20131025.html) 
- English version available here -> [GGGenome: a fast and simple DNA sequence search engine(TogoTV)](http://togotv.dbcls.jp/20150514.html)

### (参考)LocalBLASTで
検索する質問配列の数が多くなると、いちいちウェブブラウザを開いて貼り付けてクリックして…が大変になります。それを克服する方法として、Local(自分のパソコン)にBLASTのプログラムをインストールしてBLASTを実行する方法(``LocalBLAST``)があります。[詳しくはこちらの資料](
http://motdb.dbcls.jp/?AJACS32%2Fbono#e17b6eed)を御覧ください。実際にセットアップする統合TVもそこから紹介しています。

----
## アノテーションを足して見る
ゲノム解読がなされて終わりではありません。どこに遺伝子がコードされているか、転写因子の結合領域はどこかなど、ゲノム上の座標に対して注釈付けがなされていきます。それが``ゲノムアノテーション``です。

### ゲノムブラウザ
それを見る方法としてゲノムブラウザが使われます。ここではウェブブラウザ上で使えるゲノムブラウザとして有名なUCSC Genome Browser(「ゆーしーえすしー げのむ ぶらうざー」)とEnsembl Genome Browser(「あんさんぶる」)の使い方を学びます。

####【実習4】UCSC & Ensembl Genome Browserに隠されたアノテーションを発掘する

1. http://genome.ucsc.edu/ にアクセスします  
2. 上部のメニューバーの``Genomes``をクリックします  
[![Gyazo](http://i.gyazo.com/c42463de567c3b5bda28531e0a3380a5.png)](http://gyazo.com/c42463de567c3b5bda28531e0a3380a5)

3. groupに``Mammal``、genomeに``Human``、assemblyに``Feb.2009 (GRCh37/hg19)``を選び、search termに``PPARG``と入力すると入力補完されるので、一番上の``PPARG``を選び、submitボタンを押しましょう  
[![Gyazo](http://i.gyazo.com/4c16a687c6335264a86ed83b5aa0d14d.png)](http://gyazo.com/4c16a687c6335264a86ed83b5aa0d14d)

4. PPARGがコードされたゲノム上の領域が表示されます
[![Gyazo](http://i.gyazo.com/cb2da09cca945ad0c5ab2b08828d3e30.png)](http://gyazo.com/cb2da09cca945ad0c5ab2b08828d3e30)

5. 上部のnavigationボタンでmoveやzoom in/out等できますが、遺伝子名検索でたどり着いた場合、mRNAの領域に拡大されて表示されるので、zoom out ``3x``しておきましょう  
[![Gyazo](http://i.gyazo.com/45bd00962f11674fcd909d3b1c35de74.png)](http://gyazo.com/45bd00962f11674fcd909d3b1c35de74)

6. 画面下の方にあるのがアノテーションです。Regulationカテゴリー中の``ENC TF Binding``が'hide'になっているのを``show``に変えて、``refresh``ボタンを押してみましょう  
[![Gyazo](http://i.gyazo.com/b64f914712159365bbf0065722e8ad34.png)](http://gyazo.com/b64f914712159365bbf0065722e8ad34)

7. そうすると、上部のゲノム領域にこのゲノムアノテーションが付加されて表示されます  
[![Gyazo](http://i.gyazo.com/d798bf4f493263393cf0a511a60d0daa.png)](http://gyazo.com/d798bf4f493263393cf0a511a60d0daa)

8. このゲノムアノテーションについて詳しく知りたい場合、さきほどshowに切り替えた選択画面の上にあったリンクをクリックしてみましょう  
[![Gyazo](http://i.gyazo.com/0d873a1a252a3a0e96e7a88f3a999961.png)](http://gyazo.com/0d873a1a252a3a0e96e7a88f3a999961)
ENCODE Transcription Factor Binding Tracks のようです  

9. いろいろいじってしまうと元に戻したい時があります。その場合は、``default tracks``ボタンを押すとResetされ、元のゲノムアノテーションに簡単に戻せます  
[![Gyazo](http://i.gyazo.com/45bd00962f11674fcd909d3b1c35de74.png)](http://gyazo.com/45bd00962f11674fcd909d3b1c35de74)

10. 上部のメニューのうち、Viewをクリックして出てくる``Ensembl``をクリックすると、今見ている領域のEnsembl Genome Browserの該当領域へジャンプします  
[![Gyazo](http://i.gyazo.com/f3dc8684bfcbf06b0b24245d927686dc.png)](http://gyazo.com/f3dc8684bfcbf06b0b24245d927686dc)

11. 【重要】ゲノム配列はバージョンが同じならどこのサイトでも同一ですが、 **アノテーションは提供サイトで異なります**  
[![Gyazo](http://i.gyazo.com/b111f980618046623d3bdaa21292f391.png)](http://gyazo.com/b111f980618046623d3bdaa21292f391)

12. 左カラムのメニュー中のComparative Genomicsの``Synteny``をクリックすると、ヒトとマウスの間のシンテニーマップが表示されます  
[![Gyazo](http://i.gyazo.com/b7724dbf44fb56a752baba81798c2880.png)](http://gyazo.com/b7724dbf44fb56a752baba81798c2880)

13. Genetic Variationの``Resequencing``をクリックします  
[![Gyazo](http://i.gyazo.com/653466a72e112bdebcd09d7479546a96.png)](http://gyazo.com/653466a72e112bdebcd09d7479546a96)

14. 指定した領域が広すぎる(Region too large)、と怒られました。そこで、ズームスライダー(右)を＋のほうに動かしてみます  
[![Gyazo](http://i.gyazo.com/45f10ed1cb940c23826061978f8a7d89.png)](http://gyazo.com/45f10ed1cb940c23826061978f8a7d89)

15. 無事、リシーケンスの代表格のWATSONとVENTERゲノムとリファレンスゲノムのアラインメントが表示されました  

- [【復習用】UCSC Genome Browserの使い方〜表示+ENCODE編〜 2012(統合TV)](http://togotv.dbcls.jp/20120528.html)


ここまで出来て時間のある方は、自分の興味のある遺伝子やtrackを試してみましょう。余裕のある方は、[ウイルスの持ち出した宿主の遺伝子配列がコードされている領域をアミノ酸配列レベルでゲノム中から探し当てる 2012(統合TV)](http://togotv.dbcls.jp/20121030.html)で説明されているラウス肉腫ウイルスゲノム配列を取得、その痕跡をニワトリゲノムから探してみるのをやってみましょう。

- [【発展編】UCSC genome browserの使い方～配列取得編～2013](http://togotv.dbcls.jp/20131113.html)
- [【発展編】UCSC Genome Browserの使い方〜wig形式のファイルをトラックとして追加する〜(統合TV)](http://togotv.dbcls.jp/20120116.html)

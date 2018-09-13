
aEstimation of engagement based on listener’s various behaviors
using hierarchical Bayes model
階層ベイズモデルを用いた聞き手の多様なふるまいに基づく対話エンゲージメントの推定
===

2016/10/05 井上 昂治  Divesh Lala 高梨 克也 河原 達也
京都大学 大学院情報学研究科
Graduate School of Informatics, Kyoto University

人工知能学会研究会資料
SIG-SLUD-B505-28

https://jsai.ixsq.nii.ac.jp/ej/?action=repository_action_common_download&item_id=1308&item_no=1&attribute_id=1&file_no=1

（まとめ：HisashiTakagi）

---

## どんなもの？

+ マンマシン対話中に観測される（聞き手）のふるまいから，エンゲージメントを測定したいが、
結果のバラつきが大きい。原因は、判断する人の特性によると推測される。
+ ここで扱う聞き手のふるまいとは、表情、頷き、相槌など非言語情報のみ
+ 階層ベイズモデルを用いて、キャラクタを考慮した推定を提案。
+ 実験の結果，キャラクタを考慮しない場合に比べて，提案モデルは高い精度を示した．

---

## どうやって有効だと検証した？

+ 実験で有効性を検証
    + 会話データ8セッションによる交差検定
    + 1セッションを評価用，残りの 7 セッションを学習用

---

## 技術や手法の肝は？

+ 各アノテータのキャラクタを潜在変数とする階層ベイズモデル
    + マルコフ連鎖モンテカルロ法（MCMC）により学習データから推定

---

## 議論はある？

+ 複数のふるまいが同時に生起した場合にはエンゲージメントの度合いが高いと判断す
る傾向がある（共通）
+ いくつかのふるまいに関しては異なる傾向があり，キャラクタ間での相違をモデル化でき
ていることがわかる
+ 視線や姿勢など他のふるまいも検討する余地がある
+ 各ふるまいの生起を人手によりアノテーションして用いたが，これらの自動検出手法も検討する必要がある



---

## 先行研究と比べて何がすごい？

+ これまでの推定モデルは，視線などの単一のふるまい，またはセンサから得られる信
号レベルの情報の利用にとどまっている．
---

## 次に読むべき論文は？

+ 18　Y. Nakano and R. Ishii. Estimating user’s engagement
from eye-gaze behaviors in human-agent conversations. In
Proce. IUI, pp. 139–148, 2010.
    + ユーザの視線対象物の N-gram 遷移から，エンゲージ
メントを推定する階層クラスタリングモデル
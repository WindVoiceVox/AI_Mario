# AI_Mario
OpenAI Gymとgym-super-mario-brosを使って、ファミコン(NES)のスーパーマリオブラザーズをAIがプレイします。強化学習の手法を用いてAIがだんだん上手なプレイを学習して最終的にはひとつのステージをクリアします。

## 内容

- AI_Mario_Challenge1_1.ipynb

AIマリオがステージ1-1をプレイします。なるべく簡潔に読みやすいように心がけています。Google Colaboratery環境、またはNVIDIA系のGPUが搭載されたPC環境(8GB以上のGPUメモリが必要)で動作します。

Jupyter Notebookで書かれており、基本的に上のセルから順に実行すれば動作します。学習のセルは7000エピソード（＝7000人のマリオ）が実行されますので、3時間～5時間程度かかります。Colab環境は途中で終了させられないように注意してください。途中終了した場合、学習途中の状態(mario_net_x.chkpt)が残っていれば、ロードして途中から学習を継続することができます。Colab環境を使用している場合、Google Driveをマウントしてそこに学習経過を保存します。100エピソード（＝100人のマリオ）ごとに1回、プレイ動画を生成して残すので、うまくいけばマリオの学習の成果が楽しめます。ただし、良いプレイ動画が残るかどうかはかなり運に左右されます。7000エピソードが終わるころにはクリアできるようになっているはずなので、学習後のセルでクリア動画を作成してください。

このJupyter Notebookでは、強化学習のアルゴリズムとしてDDQN(Double Deep Q Network)を使用しています。実装されていることが基本的にすべてコードに見えているので、がんばれば何をやっているか読めると思います（初心者向けとは言い難いですが）。「Q学習」の基本をまずは教科書などで学習したあと読むと理解しやすいかもしれません。


## 履歴

2023/05/03...AI_Mario_Challenge1_1.ipynb をGoogle ColabとローカルPCの両方で動作するようにしました。
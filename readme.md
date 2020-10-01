
#　カッコイイ感じのウィンドウにキャリアが出てくる

→　アメリカドラマにあるような近未来系


##　概要

##　詳細

##　開始期間

##　終了期間

##　カテゴリ

##　レーダーチャート

# プロダクトコンセプト
  # 履歴書を作れれば技術面合格
　　## 1.応募できる人＝履歴書を作れる人になって、「やりたいこと」や「会社との相性」に面接の時間を使える
　　## 2.応募者は履歴書を作るだけでアプリ作成の知識が身につく
　　## 3.コードや実装、モデルの触り心地をみんなで見る組織
      ## 4.自己紹介してって言われたときにHMDをかぶせるだけ
   ## 「アプリ確認するわ」といって、開発環境を開くチームへ   

以下は個人的目標

作品集(2020年９月追加作業)

各作品ごとの「技術者の趣向」を可視化

https://twitter.com/sakuriver/status/1301663765969149953?s=20

ロードマップ
2020年10月　ゲーム廃人の可視化機能を追加予定
対象シート
カテゴリ列を集計
https://docs.google.com/spreadsheets/d/1I8TV2l-UcwWR5whEZT24nBveiK999qlD8ngEuhkaVzk/edit#gid=2082144090

2020年10月    積み兼推しリストの可視化
対象シート
https://docs.google.com/spreadsheets/d/1I8TV2l-UcwWR5whEZT24nBveiK999qlD8ngEuhkaVzk/edit#gid=20430199

2020年11月    VR用にビルド予定
趣味で作ったものでレゴブロックとカでお城がたつ

https://docs.google.com/spreadsheets/d/1I8TV2l-UcwWR5whEZT24nBveiK999qlD8ngEuhkaVzk/edit#gid=0

2020年 12月  見ているアニメを表現
以下のシートを改修予定
「あー、それならわかりますー」を応募時点でもらう
https://docs.google.com/spreadsheets/d/1I8TV2l-UcwWR5whEZT24nBveiK999qlD8ngEuhkaVzk/edit#gid=915064199

NDAの内容を技術的領域で新しく作ったもの


2020/09 v0.1を「スプリント成果物をVR空間で見るー」リリース


目標
　「表計算ソフト」での「仕様書」と「タスク管理」限界マンをなくす
   空間やアプリ特有の「うーん、実際に見ないとわからないなぁ」をぶっ壊す


以下、初期構造として設定
https://twitter.com/sakuriver/status/1310088647241134081?s=20





画像オブジェクト
　imageを追加


学習部屋
     ページオブジェクト
      image

機能
　オブジェクト確認コメント
　VRオブジェクト確認ステータス
   完了時の表示オブジェクト


展示場オブジェクト
　部屋ごとのBGM
    現時点では、3Dサウンドを利用

2020/09時点のコード



public class SprintCreateObject : MonoBehaviour
{
    private string ownerComment;
    private int ownerCheckCode;
    public GameObject completeObject;


    public SprintCreateObject()
    {
        ownerComment = string.Empty;
        completeObject.SetActive(false);
    }


    public void Apply(string ownerComment)
    {
        this.ownerComment = ownerComment;
        completeObject.SetActive(ownerCheckCode == 3);
    }

    public string GetOwnerComment() { return this.ownerComment; }
    public int GetOwnerCheckCode() { return this.ownerCheckCode; }
    public void SetOwnerCheckCode(int ownerCheckCode) { this.ownerCheckCode = ownerCheckCode; }

}

2020年10月
　エフェクト成果物を表現する機能の実装
　VRによる視野移動に対応する

2020年11月
    bot*アニメーション
      ノーコーディングによる「線を繋げて、アニメーションや動きを作る」

おまけ

MR系
2020年内
　カードゲームアップデート
　bot*MRTKアプリ　
   

勉強会で聞いたことをアプリやゲームにする会
    やろうとしていること
　　みんなで勉強会参加しようぜから「こんな話聞いていた気がするわー」を配信する
　過去のリリース作品
　　https://drive.google.com/file/d/1rezngkgT7Nrzb3NSN_TFnEAzv7aI_fL8/view?usp=sharing
　　https://drive.google.com/file/d/1sb5UdH-fGxa41SnKkqmTV9nuBwAry8M0/view?usp=sharing
　2020年10月以降のリリース
　　札幌cedec報告レポート
        decode2020(初心者一周漫画）　

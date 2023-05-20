---
title: "人型のVRMモデルを作る"
description: "シンプルな人型のVRMモデルを作ります。"
images: ["images/humanoid.gif"]
---

シンプルな人型のVRMモデルを作ります。

![](../../images/humanoid.gif)

Blenderを起動したら、3Dビューポートにマウスカーソルを置き、 `n` キーを押してください。

![](../images/humanoid1.png)

すると右側からサイドバーが開くので `VRM` のタブを選択し `VRMモデルを作成` ボタンを押してください。

![](../images/humanoid2.png)

するとVRM出力に適したアーマチュアが自動で作られます。アーマチュアとは3Dモデルのボーンの構造を
表すデータで、このアドオンではVRMの人型の骨格を表すためにアーマチュアを使います。

![](../images/humanoid3.png)

デフォルトで置いてある立方体を胴体にします。ただこのままでは胴体とするには大きすぎるので小さくします。
まずは3Dビューポートで立方体を選択します。次に右下の「<img src="../../images/object_property_tab_icon.png">」アイコンのタブを選び
`トランスフォーム` から `スケール` の値を全て `0.2` にします。これで胴体として使えそうな大きさになります。

![](../images/humanoid4.png)

胴体をアーマチュアのボーンに関連付けます。`関係` から `ペアレント` を `アーマチュア` または `Armature` にし、 `親タイプ` を`ボーン` とし、`親ボーン` を `spine` に設定してください。胴体が3Dモデルの腰あたりに移動します。

![](../images/humanoid5.png)

次は頭を作ります。3Dビューポート内にカーソルを置いた状態で、キーボードの `Shift` キーを押したまま `a` キーを押してください。するとオブジェクトの追加メニューが表示されるため `メッシュ` → `UV球` を選択してください。

![](../images/humanoid6.png)

`球` あるいは `Sphere` が追加されます。

![](../images/humanoid7.png)

これを頭として使いたいのですが、大きすぎるので縮小します。追加された球を選択し、右下の「<img src="../../images/object_property_tab_icon.png">」アイコンのタブを選び`トランスフォーム` から `スケール` の値を全て `0.25` にします。

![](../images/humanoid8.png)

この球をアーマチュアのボーンに関連付けます。`関係` から `ペアレント` を `アーマチュア` または `Armature` にし、 `親タイプ` を`ボーン` とし、 `親ボーン` を `head` に設定してください。球が3Dモデルの頭あたりに移動します。

![](../images/humanoid9.png)

次は手足を追加します。3Dビューポート内にカーソルを置いた状態で、キーボードの `Shift` キーを押したまま `a` キーを押してください。するとオブジェクトの追加メニューが表示されるため `メッシュ` → `ICO球` を選択してください。

![](../images/humanoid10.png)

`ICO球` あるいは `Icosphere` が追加されますが、同時に3Dビューポート左下に `> ICO球を追加` という表示が出ます。こちらをクリックします。

![](../images/humanoid11.png)

すると、新しく追加するICO球の設定をすることができます。半径が大きすぎると感じたので、半径の値を `0.1 m` に変更します。

![](../images/humanoid12.png)

ICO球をアーマチュアの左手上腕のボーンに関連付けます。ICO球を選択し、右下の「<img src="../../images/object_property_tab_icon.png">」アイコンのタブを選び、 `関係` から `ペアレント` を `アーマチュア` または `Armature` にし、`親タイプ`を `ボーン` とし、`親ボーン` を `upper_arm.L` に設定してください。ICO球が3Dモデルの左ひじあたりに移動します。

![](../images/humanoid13.png)

先ほどと同様にICO球を追加し、次は `hand.L` ボーンに関連付けます。左手あたりにICO球が配置されます。

![](../images/humanoid14.png)

同様に、今度は `upper_arm.R` ボーンに関連付けます。

![](../images/humanoid15.png)

同様に `hand.R` ボーンに関連付けます。

![](../images/humanoid16.png)

同様に `upper_leg.L` ボーンに関連付けます。

![](../images/humanoid17.png)

同様に `lower_leg.L` ボーンに関連付けます。

![](../images/humanoid18.png)

同様に `upper_leg.R` ボーンに関連付けます。

![](../images/humanoid19.png)

最後に `lower_leg.R` ボーンに関連付けます。

![](../images/humanoid20.png)

このモデルをVRMとして保存します。メニューの `ファイル` → `エクスポート` → `VRM (.vrm)` を選択します。

![](../images/simple2.png)

ファイル保存用のウィンドウが出るので、ファイル名と保存先を入力し `Export VRM` を押します。

![](../images/humanoid21.png)

成功するとVRMファイルが指定された場所に保存されます。

![](../../images/humanoid.gif)

こちらのページで動作確認ができます。

- https://hub.vroid.com/characters/6595382014094436897/models/1372267393572384142

## 関連リンク

- [トップページ]({{< ref "/" >}})
- [シンプルなVRMモデルを作る]({{< ref "create-simple-vrm-from-scratch" >}})
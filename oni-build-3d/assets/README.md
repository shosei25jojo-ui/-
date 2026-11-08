# キャラクターモデル

`models.json` にキャラごとのGLBファイルの場所を書くと、ゲーム開始時に読み込んで差し替えます。

```json
{ "oni": "assets/oni.glb", "tiger": "assets/tiger.glb" }
```

- キー: `oni`(赤鬼=モンスター) / `tiger`(虎=肉食動物)
- GLBにアニメーションが入っていれば、名前に `idle` / `run`(walk) / `attack` を含むものを AnimationMixer で再生します。
- 高さは自動でゲーム内の大きさに合わせます。
- ファイルがない・読み込めないときは、コード製のローポリモデルで動きます。
- `index.html` 単体で開いたとき(file:// や Artifact)は `models.json` を読めないので、コード製モデルになります。

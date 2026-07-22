# onnxruntime-builder
VOICEVOX COREで利用するonnxruntimeのビルドを行うリポジトリ

## ビルド

[`build`ワークフロー]をworkflow_dispatchで起動。

## リリース

1. [`build`ワークフロー]を`release=true`で起動してdraft releaseを作成。
2. releaseのdraftを解除する。

## 再リリース

1. リリースのときと同様、[`build`ワークフロー]を`release=true`で起動してdraft releaseを作成。
2. 古いリリースをdraft化。
3. 古いタグを削除。
4. リリースのときと同様、releaseのdraftを解除する。
5. 問題なさそうであれば、2.でdraft化した古いリリースを削除する。

[`build`ワークフロー]: https://github.com/VOICEVOX/onnxruntime-builder/actions/workflows/build.yml

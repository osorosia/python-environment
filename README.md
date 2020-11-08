# Pythonの環境構築
Dockerを使ってPython環境を構築します。  
VS Code拡張機能のRemote-Containersを使うことで、VS Code上でimportも読み込みます。

## 環境
- VS Code
- Docker

## 使い方
### コンテナ作成
```
docker-compose up -d
```
### Remote-Containers
1. VScodeの左下にある[><]をクリックする
2. [Remote-Containers: Reopen in Container]を選択する


## その他
### コンテナ上に新しいVScode拡張機能を入れたい
手動で入れるとDockerコンテナを作り直したときにリセットされる。  
-> devcontainer.jsonを修正する。
```json
"extensions": [
        "ms-python.python",
        // ここに追加する
	]
```

### pythonのライブラリを追加したい
1. requirements.txtを修正する。
```
numpy
// ここに追加する
```
2. ターミナルで下記コマンドを実行する。
```bash
docker-compose build
```


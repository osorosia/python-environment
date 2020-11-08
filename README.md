# Pythonの環境構築
Dockerを使ってPython環境を構築します（自分仕様）。  
VSCode拡張機能のRemote-Containersを使うことで、VSCode上でimport文に赤線が出なくなります。

## 環境
- VSCode
- Docker

## 使い方
### コンテナ作成
```
docker-compose up -d
```
### Remote-Containers
1. VSCodeの左下にある[><]をクリックする
2. [Remote-Containers: Reopen in Container]を選択する


## その他
### コンテナ上に新しいVSCode拡張機能を入れたい
手動で入れるとDockerコンテナを作り直したときにリセットされる。  
1. devcontainer.jsonを修正する。
```
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


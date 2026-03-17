# みんなのマキバ
## 概要
紙に描いた馬を撮影してアップロードし，バーチャル空間に放牧.

画面上の馬をなでなですると鳴き声+エフェクトが出るインタラクション.

## DB構成
| 名前 | タイプ | 照合順序 | デフォルト値 | その他 |  
| -------- | -------- | ------------------ | ----------------- | -------------- |
|    id    |   int    |  　|  | AUTO_INCREMENT |
|   path   |   text   | utf8mb4_general_ci |  |  |
|   name   |   text   | utf8mb4_general_ci |  |  |
|   cmt   |   text   | utf8mb4_general_ci |  |  |
|   date   | datetime |  | CURRENT_TIMESTAMP |  |
|   lfrt    |   text   | utf8mb4_general_ci |  |  |
* lfrt: 描かれた馬の進行方向

## 操作
1. 紙に描いた馬をスマートフォンで撮影
2. スマートフォンの切り抜き機能で背景透過のpng化
3. horse-upload.phpからアップロード（馬の名前, コメントも付与）
4. minna-no-makiba.phpをリロードするとアップロードした馬が表示される
- makiba-ichiran.phpで過去にアップロードされた馬の鑑賞も可能

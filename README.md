# robosys2024ROS2
ロボットシステム学のROS 2のパッケージ格納用のリポジトリです.
## このパッケージの概要
このパッケージは接続しているネットワークの通信速度を, 60秒ごとに計測して表示させます.  
計測する通信速度は以下のものです.
- ダウンロード
- アップロード
- Ping(通信の応答速度)
## ノード
- network_speed_measurement
    - このノードは以下の3つのパブリッシャを持ちます.
        - ダウンロードの通信速度をdownload_speedというトピックに送ります.
        - アップロードの通信速度をupload_speedというトピックに送ります.
        - Pingをpingというトピックに送ります.
- network_speed_receive
    - このノードは以下の3つのサブスクライバを持ちます.
        - download_speedというトピックからダウンロードの通信速度が送られます.
        - upload_speedというトピックからアップロードの通信速度が送られます.
        - pingというトピックからPingが送られます.
# ライセンス
- このパッケージはsivelが公開している[speedtest-cli](https://github.com/sivel/speedtest-cli/?tab=readme-ov-file)を利用しています.
    - speedtest-cliはApache License, Version 2.0に基づき公開されています.
- このパッケージはApache License, Version 2.0に基づき公開されています.
- © 2024 Tomoya Tsuji

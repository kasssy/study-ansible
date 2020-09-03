# study-ansible

ansibleを用いた、Webサーバ設定例です。


## docker環境
- container立ち上げ。
  ```bash
  $ cd docker
  $ docker-compose up -d
  ```

- server接続。設定前のサーバ状態を確認。（vim未インストール、nginx未インストール＆未起動）
  ```bash
  $ docker exec -it study-server_1 /bin/bash

  # vim
    -> bash: vim: command not found

  # systemctl status nginx
    -> Unit nginx.service could not be found.
  ```

- ansible-version確認
  ```bash
  $ docker exec -it study-ansible ansible --version
  ```

- ansible実行
  ```bash
  $ docker exec -it study-ansible /bin/bash
  # cd /var/data
  # ansible-playbook -i hosts.ini web.yml
  ```

- 実行結果の確認
  - 対象サーバ（2台）で同じ結果となることを確認。
    - <http://localhost:8081/hello.html>
    - <http://localhost:8082/hello.html>


## AWS環境




# environment
環境設定メモ用プロジェクト

- VirtualBox にUbuntuを入れる手順

  http://qiita.com/ykawakami/items/4bae371932110b2e25e3
  
  Ubuntuとのクリップボード共有設定  
  1:ゲストOSを選択 
  2:[設定]→[一般]をクリックし、順次以下を選択 
  3:高度 
  4:クリップボードの共有 
  5:双方向 
  
ホストOSからゲストOSへsshで接続する設定
■ゲストOS  
    `$ sudo apt-ge install openssh-server`  
    `$ ps -ef | grep ssh`


■ホストOS
  $ ssh 127.0.0.1 -p 3333 -l ユーザ名

■VM設定(ゲストOS停止状態で実施)
  1:ゲストOSを選択
  2:[設定]→[ネットワーク]をクリックし、順次以下を選択
  3:アダプタ1
  4:割り当て：NAT
  5:高度な設定
  6:ポートフォワーディング
  7:名前：ssh
    プロトコル：TCP
    ホストIP：127.0.0.1
    ホストポート：3333
    ゲストIP：未入力
    ゲストポート：22
  
- Githubにsshでgitコマンドを叩くための準備

  http://chie.hatenablog.com/entry/2012/04/24/011052
  
- ブラウザでログイン時のパスワードと、各環境からのssh実行時のパスワードは異なる。ややこしい


- AWS接続のための準備  
    `$ sudo -E apt-get install python-setuptools`  
    `$ sudo -E apt-get install python-pip`  
    `$ sudo su -`  
    `# pip install awscli`  
    `# exit`  
    `$ aws configure`  
    
使用するAWSアカウントの
AccessKey、
SecretAccessKeyなどを設定
  
- 入れておくアプリ  
  
  サクラエディタ  
  WinMerge  
  WinSCP  
  
- 作っておくもの  
  
  ポモドーロxlsx  
  日付作成ディレクトリ  

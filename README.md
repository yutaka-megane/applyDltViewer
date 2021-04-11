# applyDltViewer

# DltViewerのビルド
## 環境
WSLのUbuntuでビルドします。
```
$ cat /etc/os-release
NAME="Ubuntu"
VERSION="18.04.5 LTS (Bionic Beaver)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 18.04.5 LTS"
VERSION_ID="18.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=bionic
UBUNTU_CODENAME=bionic
```

## 手順
下記を実行
※参考：[Markdown記法（VSCode） チートシート](https://qiita.com/takeoverjp/items/d7a9ad4e5f0b778308be)
※参考：[DLT Viewer - Installation](https://github.com/GENIVI/dlt-viewer/blob/master/INSTALL.md)

```
git clone --depth=1 --branch=v2.18.0 http://github.com/GENIVI/dlt-viewer.git
cd dlt-viewer
sudo apt install build-essential
sudo apt install qtcreator
sudo apt install qt5-default
sudo apt install libqt5serialport5-dev
mkdir build
cd build
qmake ../BuildDltViewer.pro
make
sudo make install
sudo ldconfig
release/dlt_viewer
```

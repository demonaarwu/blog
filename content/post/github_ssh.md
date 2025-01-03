+++
title = '設定 GitHub SSH 連線公鑰'
date = 2024-07-22T21:24:40+08:00
draft = false
+++

## 1. 利用 `ssh-keygen` 產生金鑰

在 terminal 底下輸入以下指令：

```
ssh-keygen -t ed25519 -C "youremail@example.com"
```

其中的 `youremail@example.com` 要換成你註冊 GitHub 時所用的 email。

`ssh-keygen` 會讓你設定金鑰儲存的地方，預設會在 `~/.ssh/id_ed25519` ，若不想變更按 `Enter` 鍵即可。

接著它還會讓你設定 passphrase ，一樣按 `Enter` 鍵跳過就行。

## 2. 複製剛剛設定的金鑰

在 terminal 底下輸入以下指令輸出給 GitHub 的公鑰，並將其複製：

```
cat ~/.ssh/id_ed25519.pub
```

## 3. 將金鑰新增至 GitHub

打開 [GitHub 設定金鑰的頁面](https://github.com/settings/keys)，按下畫面中的 **New SSH key**，貼上剛剛複製的公鑰，按下確定後即設定完成。

此時你可以用 `ssh` clone 隨意一個 repo 看看，如果 clone 的了就是設定成功了。

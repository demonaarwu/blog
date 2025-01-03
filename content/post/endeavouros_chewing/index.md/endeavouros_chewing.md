+++
title = 'EndeavourOS 安裝 fcitx5 中文輸入法'
date = 2024-07-21T22:32:03+08:00
draft = false
+++

![](/img/endeavouros.png)

## 1. 安裝 fcitx5 全家桶

```
sudo pacman -S fcitx5-im fcitx5-chewing fcitx5-qt fcitx5-gtk fcitx4-chinese-addons

```

## 2. 將注音加入 fcitx5 的輸入法中

在應用程式裡找到並開啟 **Fcitx 5 Configuration** （或直接在終端機輸入 **fcitx5-config-qt**）。

打開後在右側尋找並單擊 **chewing** 的選項（如圖），按下中間 **<-** 的選項後，注音便被加入到 fcitx5 中了。

![](/img/fcitx5-config.png)

## 3. 編輯 /etc/environment 並重開機

在 `/etc/environment` 下加入以下幾行，並重開機：

```
GTK_IM_MODULE=fcitx
QT_IM_MODULE=fcitx
XMODIFIERS=@im=fcitx
SDL_IM_MODULE=fcitx
GLFW_IM_MODULE=fcitx

```

重開機後按下 `Ctrl+Space` ，就能使用 fcitx5 輸入中文了。

（完。）

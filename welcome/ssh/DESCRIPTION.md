当前挑战关卡将教你如何使用 `SSH` 。
请使用 `Start` 按钮启动当前挑战关卡，等待确认它已启动，然后执行以下步骤！

1. 首先在终端程序中输入 `ssh-keygen -f ~/.ssh/key -N ''`或用其他软件生成 `key` 和 `key.pub` 公私钥对；
2. 执行 `cat key.pub` 或者 `notepad key.pub` 将公钥复制出来；
3. 点击导航栏右侧的“设置”选项，点击左边`SSH 公钥`，将复制的公钥填写进去，点击 `Update` 保存自己的公钥；
4. 输入 `ssh -i ~/.ssh/key hacker@pwn.hust.college`，即可连接到挑战关卡容器，然后运行挑战程序；

本次挑战，像所有其他挑战一样，位于 `/challenge` 目录中。
在这种情况下，挑战程序是 `/challenge/solve`。
只需在 `SSH` 中运行它，你就会得到 `flag`，将其复制粘贴到 `flag` 提交框中然后提交！

当然，你也可以使用 SSH config 连接挑战关卡容器，推荐使用如下配置。

```
Host challenge
  HostName pwn.hust.college
  User hacker
  IdentityFile ~/.ssh/key
```
当前挑战关卡将教你如何使用 VM 连接挑战关卡中的 QEMU 虚拟机，并利用提前准备好的内核模块来获取 `flag`。请使用 Start 按钮启动当前挑战关卡，等待确认它已启动。解决该关卡的步骤如下所示：

- 在 VS Code 终端中输入 `vm -h` 查看 `vm` 脚本的使用方法(connect,exec,start,stop,restart,logs,debug,build)。你可以通过 `vm connect` 进入正在运行挑战关卡的虚拟机，可以使用 `vm logs` 获取日志，也可以在练习模式中使用 `vm debug` 调试内核。
- 随后输入 `vm connect` 连接启动的 QEMU 虚拟机；
- 进入 QEMU 虚拟机后，查看 `/proc/machoke` 文件即可获得 `flag`；

本次挑战，像所有其他挑战一样，位于 `/challenge` 目录中，挑战程序是 `/challenge/solve`。
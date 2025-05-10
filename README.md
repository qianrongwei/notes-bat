# notes-bat
常用的 .bat（Windows 批处理）命令速查表
# ✅ 常用 `.bat` 批处理命令速查表

| 命令             | 功能说明                                             | 示例                                                                                     |
|------------------|------------------------------------------------------|------------------------------------------------------------------------------------------|
| `@echo off`      | 关闭命令回显（隐藏每行命令本身的输出）              | `@echo off`                                                                               |
| `echo`           | 显示文本或变量                                       | `echo Hello World`                                                                       |
| `rem`            | 添加注释，不会被执行                                 | `rem 这是注释`                                                                           |
| `pause`          | 暂停执行，等待用户按任意键继续                       | `pause`                                                                                  |
| `pause >nul`     | 同上，但不显示提示文字                               | `pause >nul`                                                                             |
| `start`          | 启动程序或打开文件/网址                              | `start "" "notepad.exe"` 或 `start "" chrome.exe https://example.com`                   |
| `call`           | 调用另一个批处理脚本并返回继续执行                   | `call other_script.bat`                                                                  |
| `if exist`       | 判断文件或目录是否存在                               | `if exist "C:\file.txt" (echo 存在) else (echo 不存在)`                                  |
| `goto`           | 跳转到脚本中某个标记（`:label`）                     | `goto END`                                                                               |
| `for`            | 遍历文件、字符串、命令输出等                         | `for %%f in (*.jpg) do echo %%f`                                                         |
| `set`            | 设置或读取变量                                       | `set NAME=ChatGPT`；`echo %NAME%`                                                        |
| `setlocal` / `endlocal` | 设置局部变量作用域                         | `setlocal enabledelayedexpansion`                                                        |
| `exit`           | 退出脚本或终端窗口                                   | `exit` 或 `exit /b 0`                                                                    |
| `copy`           | 复制文件                                             | `copy source.txt dest.txt`                                                               |
| `xcopy`          | 递归复制文件夹及内容                                 | `xcopy C:\src D:\dest /E /I`                                                             |
| `del`            | 删除文件                                             | `del /Q *.log`                                                                           |
| `md` / `mkdir`   | 创建新目录                                           | `mkdir logs`                                                                             |
| `rd` / `rmdir`   | 删除目录（可递归删除）                               | `rmdir /S /Q logs`                                                                       |
| `timeout`        | 延时等待指定秒数                                     | `timeout /T 5 /NOBREAK`                                                                  |
| `choice`         | 提供用户选项（如 Y/N）并返回错误码                  | `choice /C YN /M "是否继续？"`                                                           |
| `ping`           | 利用 ping 实现延时或网络测试                         | `ping 127.0.0.1 -n 3 >nul`                                                               |

> 💡 `%%f` 用于 `.bat` 脚本中 `for` 循环，若在命令行（cmd）中测试，需改成 `%f`

---

## 📌 示例：基本结构模板

```bat
@echo off
rem 初始化脚本
echo 正在执行...
pause

# 编译与运行

## 1. 打开项目

双击：

```text
远程控制.sln
```

## 2. 确认组件

Visual Studio 安装器中建议包含：

- 使用 C++ 的桌面开发
- MSVC C++ 编译工具
- Windows 10/11 SDK
- ATL

## 3. 编译

选择：

```text
x64
Debug
```

然后：

```text
生成 -> 生成解决方案
```

## 4. 修改服务器 IP

打开：

```text
Client/client.cpp
```

修改：

```cpp
#define SERVER_IP "服务器虚拟机IPv4"
```

## 5. 运行

先运行 Server，再运行 Client。

## 6. 如果项目提示平台工具集不存在

例如本机没有 `v143`，在项目属性中选择本机安装的 MSVC 工具集，或者让 Visual Studio 自动升级项目。

## 7. 如果提示 ATL/CImage 找不到

说明 Visual Studio 安装时没有安装 ATL。打开 Visual Studio Installer，给“使用 C++ 的桌面开发”补装 ATL 相关组件。

## 8. 最后测试

严格按照：

```text
docs/08_虚拟机测试手册.md
```

执行，不要直接在真实电脑上测试未经验证的远程输入程序。

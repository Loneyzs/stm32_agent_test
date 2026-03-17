### 项目概况：

这是一个个人用于测试coding agent单片机开发能力的验证工程。

使用STM32f407ZGT6，仓库初始为cubemx生成的最小工程模板，后续部分均需手写完成（包括硬件配置和应用层开发）。



### 文档说明：

开发板原理图和引脚配置说明位于/Docs下，按需自行查阅。



### 版本管理说明：

每次成功开发新功能后，修改按照正常git流程git push origin main即可。



### 编译说明：

使用cmake + ninja + openocd进行构建编译烧录，具体命令如下：

在根目录下 

cmake -B build -G Ninja

cmake --build build

openocd -s "D:/Software/MSYS2/mingw64/share/openocd/scripts" -f interface/cmsis-dap.cfg -f target/stm32f4x.cfg -c "program C:/Users/a7743/Desktop/stm32_agent_test/build/stm32_agent_test.elf verify reset exit"
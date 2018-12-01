### Windows自带MD5 SHA1 SHA256命令行  
  `certutil -hashfile gpg4win-3.1.5.exe sha256`

### 批处理 对某目录循坏下所有js文件执行某操作  
```
@echo off
:: 设置目录，脚本会自动按树层次查找
SET JSFOLDER="目录"
echo 正在查找xx
chdir /d %JSFOLDER%
for /r . %%a in (*.js) do (
    @echo 执行到 %%~a ...
    :: 此处是操作 比如uglifyjs %%~fa  -c -m -o %%~fa
)
echo 完成!
pause & exit
```

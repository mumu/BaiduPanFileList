# BaiduPanFileList
### 介绍
统计百度盘文件（夹）数量大小，导出文件路径和大小，支持子文件夹，用于校验文件（夹）一致性

### 安装
https://greasyfork.org/help/installing-user-scripts

### 使用方法
* 点击 統計檔案 按钮或使用快捷键Q（不分大小写）统计当前文件夹，若同时按住CTRL键将同时统计所有子文件夹
* 浏览器提示文件（夹）数量，所有文件大小，剪切板会复制该提示信息和所有文件（夹）路径和大小

### 注意事项
1. 如果界面无法显示按钮，尝试使用快捷键
2. 请注意保存剪切板原内容

### 示例
[点击查看](https://raw.githubusercontent.com/icgeass/BaiduPanFileList/master/resources/demo.txt)

### 本次更新后使用方法
1. 在网盘首页，按住Ctrl键+点击統計檔案按钮。
2. 如果出现错误，重复第一步，直到显示网盘总共大小。
3. 点击test按钮
4. 按F12打开开发者工具，到console里复制打印出的内容，保存到txt。
5. 打开excel，导入保存的txt，按Tab分隔。会显示三列：文件路径，文件md5（文件夹显示undefined），文件大小Byte（文件夹显示0）
6. 按文件md5可以显示相同文件。可以使用excel公式：=COUNTIF(B:B,[@Column2])   。该值为该文件出现的次数。当该值>=2时，可以依据文件路径删除重复的文件。
7. 文件大小可以显示为MB，利用excel公式：=[@Column3]/1024/1024

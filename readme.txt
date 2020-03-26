运行方式：

.\bin\webengine.exe --register-pepper-plugins=".\\testpages\\pepflashplayer64_32_0_0_344.dll;application/x-shockwave-flash" "--ppapi-flash-path=testpages\\pepflashplayer64_32_0_0_344.dll"



注意：如果需要支持播放mp4需要自己编译，https://doc.qt.io/qt-5/qtwebengine-platform-notes.html。


编译qwebengine步骤：
1.安装需要的工具在windows下安装flex和bison、gperf、python
http://gnuwin32.sourceforge.net/packages/flex.htm
https://sourceforge.net/projects/gnuwin32/files/bison/2.4.1/bison-2.4.1-setup.exe/download?use_mirror=jaist
https://sourceforge.net/projects/gnuwin32/files/gperf/3.0.1/gperf-3.0.1.exe/download?use_mirror=jaist&download=
https://www.python.org/ftp/python/2.7.5/python-2.7.5.msi
http://strawberryperl.com/download/5.30.2.1/strawberry-perl-5.30.2.1-32bit.msi


2.设置上述路径到环境变量
3.查看环境变量
perl -version
python --version
gperf -v
bison --version
flex --version


4.启动VS 2017的 x64_x86 交叉工具命令提示符
启动 “VS 2017的 x64_x86 交叉工具命令提示符“ （必须是该进程）

cd C:\Qt\Qt5.12.1\5.12.1\Src\qtwebengine
"C:\Qt\Qt5.12.1\5.12.1\msvc2017\bin\qmake.exe" -- -webengine-proprietary-codecs



"C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.16.27023\bin\Hostx86\x86\nmake.exe"

"C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.16.27023\bin\Hostx86\x86\nmake.exe" install



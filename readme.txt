这是一个64bit下编译的库。
里面包含glfw,glew,glut，

在VS新建一个win32控制台应用程序。
然后再新建一个属性表，然后
在VC++目录-->包含目录-->添加F:\build\GLFW;F:\build
在VC++目录-->库目录-->添加F:\build
在链接器-->输入-->附加依赖项-->添加glew32.lib;glfw3.lib;opengl32.lib;glut32.lib
然后就可以用啦！


这是在vs2013下编译的lib，所以我在vs2015下跑的时候出现了以下错误：
1>LINK : warning LNK4098: 默认库“MSVCRT”与其他库的使用冲突；请使用 /NODEFAULTLIB:library
1>glfw3.lib(init.obj) : error LNK2019: 无法解析的外部符号 __imp_vsnprintf，该符号在函数 _glfwInputError 中被引用
1>MSVCRTD.lib(vsnprintf.obj) : error LNK2001: 无法解析的外部符号 __imp_vsnprintf
1>glfw3.lib(context.obj) : error LNK2019: 无法解析的外部符号 __imp_sscanf，该符号在函数 parseVersionString 中被引用
1>MSVCRTD.lib(vsnprintf.obj) : error LNK2001: 无法解析的外部符号 __imp__vsnprintf
1>F:\gl_code\CAMP6\x64\Debug\CAMP6.exe : fatal error LNK1120: 3 个无法解析的外部命令 

solution： 链接器-->输入-->附加依赖项-->添加 legacy_stdio_definitions.lib


这里面有个opencv310_install_x64_debug.props：这里面还包含了opencv的配置，所以如果电脑上没有opencv就自己重新新建属性表。

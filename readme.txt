����һ��64bit�±���Ŀ⡣
�������glfw,glew,glut��

��VS�½�һ��win32����̨Ӧ�ó���
Ȼ�����½�һ�����Ա�Ȼ��
��VC++Ŀ¼-->����Ŀ¼-->���F:\build\GLFW;F:\build
��VC++Ŀ¼-->��Ŀ¼-->���F:\build
��������-->����-->����������-->���glew32.lib;glfw3.lib;opengl32.lib;glut32.lib
Ȼ��Ϳ���������


������vs2013�±����lib����������vs2015���ܵ�ʱ����������´���
1>LINK : warning LNK4098: Ĭ�Ͽ⡰MSVCRT�����������ʹ�ó�ͻ����ʹ�� /NODEFAULTLIB:library
1>glfw3.lib(init.obj) : error LNK2019: �޷��������ⲿ���� __imp_vsnprintf���÷����ں��� _glfwInputError �б�����
1>MSVCRTD.lib(vsnprintf.obj) : error LNK2001: �޷��������ⲿ���� __imp_vsnprintf
1>glfw3.lib(context.obj) : error LNK2019: �޷��������ⲿ���� __imp_sscanf���÷����ں��� parseVersionString �б�����
1>MSVCRTD.lib(vsnprintf.obj) : error LNK2001: �޷��������ⲿ���� __imp__vsnprintf
1>F:\gl_code\CAMP6\x64\Debug\CAMP6.exe : fatal error LNK1120: 3 ���޷��������ⲿ���� 

solution�� ������-->����-->����������-->��� legacy_stdio_definitions.lib


�������и�opencv310_install_x64_debug.props�������滹������opencv�����ã��������������û��opencv���Լ������½����Ա�

# Some notes of Latex

注：采用**overleaf**在线编辑更为快捷，~~省略选择恐惧症患者安装各式Tex的问题~~

1. 如需分段，输入**两个**回车；单个换行起空格作用；段前不需要空格，尤其不要全角的汉字空格；空行只起分段作用，使用多个空行不能起增大段间距作用；使用多个空格不能起增大字符间距作用

2. overleaf输入中文：

   1. 在\document后添加代码行 **\usepackage[UTF8]{ctex}** 
   2. 左上角的Menu -> Setting -> Compiler -> XeLatex

3. %开头的行是注释

4. 公式输入：夹在行文中的公式用一对$括起来

5. 在文档中另起一行不会在输出中产生新的段落，如需另起一段，插入空白行。如需在一个段落内另起一行，在前一行的末尾输入反斜杠\\\（注意和第一点表述的区别）

6. 在引子中加入指令 **\usepackage[utf8]{inputenc}**，![image-20220120210235411](C:\Users\86183\AppData\Roaming\Typora\typora-user-images\image-20220120210235411.png)

   若某些标识符出现乱码，可通过在标识符后加一对空括号解决

   7. **\textbf{text}**输出**黑体**字，**\textit{text}**输出*斜体*字，**\texttt{text}**输出等宽字体，如需要整段打印等宽字体（如程序代码），则输入verbatim（注意输入黑体数学符号的指令是**\mathbf{math}**

   8. **\usepackage{amsmath,amssymb}** 数学功能包（在\documentclass**后**加入功能包以防报错）

      希腊字母、一些数学符号及二元运算符在键盘上没有对应输入时，需在数学模式下用对应指令输入

      ​                                                                                                  表格如下

      ![image-20220120213609609](C:\Users\86183\AppData\Roaming\Typora\typora-user-images\image-20220120213609609.png)

      {}是Latex功能符，输入时要加\

      在括号前后加\left和\right, 自动产生大小适当的括号

      上标^ 	 下标_		\frac 分数 	\binom 二项式系数 	\sum 连加	\prod 连乘	\int 积分	\lim 极限
      
      单行排列公式可**编号**，在equation 环境下输入，如无需编号，则在equation*环境输入（示例：begin{\equation} \end{equation})
      
      **注：在equation环境下无需加$ $符号**
      
      如需在表达式内加文字（包括空格）指令是\text{text}
      
      引用指令 在表达式前插入\label{Label}，引用时采用\eqref{Label}	（此处的引用是指引用编号）
      
      等式/不等式组的对齐：在每个等式需要对齐的符号（如等号）前加一个**&**，在每一行的结尾加 \\ \ （也可用这个方法让拖式（连等号或其它（在对应符号对齐））
      
      **矩阵**应**先在equation环境**再在matrix环境下输入（为产生矩阵符号，用pmatrix（圆括号），bmatrix（方括号），vmatrix（竖线）环境）
      
      定义新指令与C语言的define用法类似，即简单替换。指令格式：**\newcommand{command}{definition}**
      
      注：格式里的command一定要记得加\
      
      新指令还可以带参数**\newcommand{command}[n]{definition}**, n表示参数个数
      
      
      
      


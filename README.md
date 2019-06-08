# cextern
    c++克服 extern 函数，用main,cpp中的int add,“骗”过编译器，使编译链接成功 
    编译步骤：
    1.gcc -c func.c 
    2.g++ -c main.cpp 
    3. g++ -o”main” ./main.o ./func.o
    在c++中，只能用int add，而不能用int add(int,int)，也不能用先定原型int add(int,int)然后实现的方式，都会报undefined reference 'add'
    在c中，可以用定义add函数也可用c++那种不给出函数体或把add当一般变量，编译是不会出问题的，运行另外一回事。
    用cmake也可以直接编译链接，不需要生成中间文件.o，再链接的方式，cmake自己会处理。

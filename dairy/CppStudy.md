# c/c++ 入门
- C++ primer 开始学习 2018/09/08
    - ::作用域操作符,::xxx时,因为全局作用域没有名字,所以为空,该操作就是显示的从全局作用域访问xxx这个变量
    - 引用/指针 &是取地址符 取的是变量的地址
        - 大前提,变量本身也是一个对象
        - 引用 不是对象,只能引用存在的对象(变量),与变量不同,不能赋值和拷贝,初始化即绑定对象,之后不再变化
            - int &b是定义一个引用;int &&b是定义引用的引用.
        - 指针 是对象,可以赋值和拷贝,指针用于存放对象的地址,一般来说就是变量的地址.
            - 定义后没有初始化的指针,将拥有不确定的值.
            - 同理 int *p是定义一个指针;int **p是指针的指针
    - '&'紧随类型名出现是定义引用;'&'在表达式中出现是取地址符
    - '*'紧随类型名出现是定义指针;'*'表达式中出现是解引用符
        - 解引用用于访问指针指向的对象
    - const 常量限定符
        - *const 代表指针本身是一个常量 (const int *const ptr 指向常量类型的常量指针)
        - 顶层const
        - 底层const
    - C++左值和右值：右值使用的是对象的值,左值则使用对象的身份(地址)

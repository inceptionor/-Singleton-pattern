class 类名:

    __instance = None   # 记录创建好的实例对象
    __has_init = False   # 标记实例对象是否已经初始化

    def __new__(cls, *args, **kwargs):
        if cls.__instance is None:
            cls.__instance = object.__new__(cls)  # 创建并返回一个购物车的实例对象

        return cls.__instance

    def __init__(self):
        if 类名.__has_init is False:
            self.属性 = 200
            类名.__has_init = True

class ClassExample():

    __instance = None   # 记录创建好的实例对象Record the created instance object
    __has_init = False   # 标记实例对象是否已经初始化Record Whether the instance object has been initialized

    def __new__(cls, *args, **kwargs):
        if cls.__instance is None:
            cls.__instance = object.__new__(cls)  # Create and return an instance object of a ClassExample

        return cls.__instance

    def __init__(self):
        if ClassExample.__has_init is False:
            self.test = 200
            ClassExample.__has_init = True

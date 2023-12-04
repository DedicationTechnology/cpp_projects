# 想编译一个person应用程序，依赖于main.o和person.o【分别由main.cpp和person.cpp生成】
person: main.o person.o
	# 这里就是使用 g++ 进行编译 $@ 表示 person $^表示 main.o 和 person.o
	g++ -o $@ $^
# 用%通配符来表示所有的.o文件和.cpp文件。例如：main.o:main.cpp 表示 main.o文件依赖于main.cpp
%.o : %.cpp
	# <表示第一个依赖，这里也可以用^
	g++ -c -o $@ $<
# 上面的通配符可以用下面两段代码代替
# main.o:main.cpp
	# 注意，本页面中所有的都是tab键，不是空格，这里的<就表示第一个依赖，也就是main.cpp，并且这里只有一个依赖
# 	g++ -c -o $@ $<
# person.o:person.cpp
# 	g++ -c -o $@ $<
# 删除所有的.o文件和person应用程序文件
clean:
	rm -f *.o person	

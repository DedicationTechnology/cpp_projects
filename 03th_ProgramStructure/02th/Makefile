# 想编译一个person应用程序，依赖于main.o和person.o【分别由main.cpp和person.cpp生成】
person: main.o person.o
	g++ -o $@ $^

%.o : %.cpp
	g++ -c -o $@ $<

clean:
	rm -f *.o person	

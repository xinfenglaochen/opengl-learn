vpath %.c ../glad/src ../public
vpath %.cpp ../public ../public/glfw
# vpath %.h ../glad/include ../public
vpath %.hpp ../glm

cxxflag = -std=c++11

obj=main.o glad.o texture.o 

a.out:$(obj)
	g++ $(cxxflag) -framework OpenGL -lglfw -lfreetype \
				-o a.out $(obj)

texture.o:texture.cpp
	g++ $(cxxflag) -c -I../glad/include $<

glad.o:glad.c
	g++ -c -I../glad/include $<

glwindow.o:glwindow.cpp
	g++ -c -I../public/glfw $<

main.o:main.cpp
		g++ $(cxxflag) -c -I../glad/include \
			-I/usr/local/include/freetype2 \
			-I../\
				$<

.PHONY:clean
clean:
		-rm a.out $(obj)

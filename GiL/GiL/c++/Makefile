all: wvs

wvs:
	 cl.exe /DNDEBUG /EHsc /MD /wd4355  /D "WIN32" /D_USRDLL /D_WINDLL -I "C:\Program Files\Gecode\include" gecode_wrapper.cpp space_wrapper.cpp /link /LIBPATH:"C:\Program Files\Gecode\lib" /DLL /OUT:../sources/gil.dll

so:
	g++  gecode_wrapper.cpp space_wrapper.cpp -std=c++11 -dynamiclib -fPIC -F/Library/Frameworks -framework gecode -o ../sources/libgecode.so  -ffast-math -O3 

dylib: gecode_wrapper.cpp
	g++  gecode_wrapper.cpp space_wrapper.cpp -std=c++11 -dynamiclib -fPIC -F/Library/Frameworks -framework gecode -o ../sources/libgecode.dylib  -ffast-math -O3

# CGAL_essentials
Notes/Commands to build cgal programs 

# [Environment Setup 11] Build CGAL-based programs using CMake

* Make a new directory for CGAL and navigate to it

`$ mkdir cgal`

`$ cd cgal`

* Copy the downloaded CGAL tarball and extract it

`$ cp ~/Downloads/CGAL-5.2.2.tar.xz .`

`$ tar -xvf CGAL-5.2.2.tar.xz`

* Copy the downloaded Boost tarball and extract it

`$ cp ~/Downloads/boost_1_76_0.tar.gz .`

`$ tar -xzvf boost_1_76_0.tar.gz`

* Make another directory for the test case and navigate to it

`$ mkdir test`

`$ cd test/`

* Copy the sample code

`$ cp ~/Dir_name/file_name.cpp .`

* Generate the required CMake files using the provided script

`$ $HOME/cgal/CGAL-5.2.2/scripts/cgal_create_CMakeLists`

* Install missing prerequisites (GMP and MPFR libraries)

`$ sudo apt install libgmp-dev`

`$ sudo apt install libmpfr-dev`

* Run CMake with appropriate parameters for configuring CGAL and Boost

`$ cmake -DCGAL_DIR=/home/cgal/CGAL-5.2.2 (basically add the path for cgal library wherever it is) -DCMAKE_BUILD_TYPE=Release -DBOOST_ROOT="path for boost library"`

* Build the source code using GNU Make

`$ make`

* Run the compiled program

`$ ./file_name`

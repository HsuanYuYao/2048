# TD(0) with Replay Buffer for Game 2048

Temporal Difference Learning (SARSA) with Replay Buffer for Game 2048 

### To run the program:

 * #### Install CMake
> In command line
>
>     sudo apt install cmake
>
 * #### Git Clone
> 
> under your workspace folder
>
>     git clone https://github.com/HsuanYuYao/2048.git --recurse-submodules 
>
> go to the folder 2048/ under your workspace and create a new folder build/
> 
>     cd 2048/ && mkdir build
>
> go to the folder build/ and create two new folders Debug/ and Release/
>
>     cd build/ && mkdir Debug Release
>
 * #### Run CMake

We have already create a CMakeLists.txt file under 2048/ for you. 
>
> under the folder 2048/build/Debug 
>
>     cmake ../../ -DCMAKE_BUILD_TYPE=Debug && make && ./2048_rp 0.1 100000 0 1
>
> or 2048/build/Release (depend on your build-type)
> 
>     cmake ../../ -DCMAKE_BUILD_TYPE=Release && make && ./2048_rp 0.1 100000 0 1
>
> where the arguments from left to right are -alpha -total -seed -buffersize
 

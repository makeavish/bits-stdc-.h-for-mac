# bits-stdc-.h-for-mac
Include bits/stdc++.h on mac

bits/stdc++ is a GNU GCC extension, whereas OS X uses the clang compiler. However, you can install gcc and make it work by manually adding the header file.

## Steps
- Install xcode command line tools using this command ```xcode-select --install```
- Install [Homebrew](https://brew.sh/) (if not installed)
- Instal gcc with this command: ```brew install gcc```
- Now open terminal and navigate: ```cd /usr/local/bin```
- Now link g++-10 to g++ using this command: ```ln -s g++-10 g++```
- Now log out and log back in
- Now copy stdc++.h file using this command: ```cp ~/Path-to-file/stdc++.h /usr/local/Cellar/gcc/10.1.0/include/c++/10.1.0/bits``` (Exact path of the bits folder may change according to your installed gcc version/Mac OS version)

Now it should compile as expected

I have also included "using namespace std;" in this file.
So, from now on you dont need to write it everytime you create a cpp file.

NB:
- If you are facing compile issue with gcc after installing then uninstall gcc and use this command to build gcc from source: ```brew install --build-from-source gcc```
- I tested this version on Mac OS Catalina and gcc 10.1.0, if you are facing any issues then feel free to create an issue.

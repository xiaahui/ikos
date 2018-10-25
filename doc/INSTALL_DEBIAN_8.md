Install IKOS dependencies on Debian Jessie
==========================================

Here are the steps to install the required dependencies of IKOS on **[Debian 8 (Jessie)](https://www.debian.org/releases/jessie/)**.

First, make sure your system is up-to-date:

```
$ sudo apt-get update
$ sudo apt-get upgrade
```

Now, you will need to add the LLVM repositories to your apt `sources.list`:

```
$ echo "deb http://apt.llvm.org/jessie/ llvm-toolchain-jessie-4.0 main" | sudo tee -a /etc/apt/sources.list
```

Then, run the following commands:

```
$ sudo apt-get update
$ sudo apt-get install gcc g++ cmake libgmp-dev libboost-dev libboost-filesystem-dev \
    libboost-test-dev python python-pygments libsqlite3-dev libz-dev libedit-dev \
    llvm-4.0 llvm-4.0-dev clang-4.0
```

Now, add the LLVM directory to your `PATH` (consider adding this in your `.bashrc`):

```
$ PATH="/usr/lib/llvm-4.0/bin:$PATH"
```

You are now ready to build IKOS. Go to the section [Build and Install](../README.md#build-and-install) in README.md
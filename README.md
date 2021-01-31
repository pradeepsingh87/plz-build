# plz-build
Please is a cross-language build system with an emphasis on high performance, extensibility and reproducibility. 
It supports a number of popular languages and can automate nearly any aspect of your build process.
# How it is so fast 
https://github.com/thought-machine/please#how-is-it-so-fast

# Why Please, and not Maven, pip, or go build?
https://github.com/thought-machine/please#why-please-and-not-maven-pip-or-go-build

# Why Please, and not make?
https://github.com/thought-machine/please#why-please-and-not-make

# Why Please, not Bazel, Buck or Pants?
https://github.com/thought-machine/please#why-please-not-bazel-buck-or-pants

# Installation . 
Supports linux based system only . The below command installs and add plz to $PATH environment variable . 
I had to manually add it to $PATH when using ec2 instance .

```
curl -s https://get.please.build | bash
```

Check plz version 
```
plz --version
Please version 15.13.0
```

# Getting Started 
Run plz init  to create a .plzconfig file at the root of your project . 
.plzconfig also helps please understand the root path fo


```
[ec2-user@ip-172-12-23-123 main]$ plz init
Would you like to setup Go in this repository: y█
Warning: go is not found on the default path. Please configure gotool, or goroot under [go] in your .plzconfig
Please doesn't use the host machines $PATH variable. Instead the path is configured in .plzconfig with a default of

[build]
path= /usr/local/bin:/usr/bin:/bin

You may also add {GOROOT}/go/bin to the path if you prefer
Import path (i.e. go module): █
Wrote config template to /home/ec2-user/plz-bld/main/.plzconfig, you're now ready to go!

Also wrote wrapper script to pleasew; users can invoke that directly to run Please, even without it installed.
Also marking plz-out to be ignored by your SCM.

Pleasings are a collection of auxiliary build rules that support other languages and technologies not present in the core please distribution.
For more information visit https://github.com/thought-machine/pleasings

Would you like to add pleasings to your project? You may also do this later with `plz init pleasings` if you wish.: y█
[ec2-user@ip-172-12-23-123 main]$ 
```
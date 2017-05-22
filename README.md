Mono (C#) Docker image
======================

This image is based on Alpine Linux image, which is only a 5MB image, and contains
[Mono](http://www.mono-project.com/).

Usage Example
-------------

```bash
$ echo -e 'using System; class MainClass { public static void Main (string[] args) { Console.WriteLine ("Hello World"); } }' > qq.mono
$ docker run --rm -v `pwd`:/tmp frolvlad/alpine-mono sh -c 'mcs -out:/tmp/qq.exe /tmp/qq.mono && mono /tmp/qq.exe'
```

Once you have run these commands you will have `qq.exe` mono-executable in your
current directory, and you will get printed 'Hello World' from Mono!

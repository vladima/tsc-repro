Clone the repo, switch to the local repro folder and fetch submodules
```
git submodule init
git submodule update
```

Run repro code
```
node tsc/tsc.js -p vscode/src
```

Test OS: Ubuntu 16.04 64 bit
```
vladima@vladima-HP:~/Sources/play/test2/tsc-repro$ node --version
v6.2.1
vladima@vladima-HP:~/Sources/play/test2/tsc-repro$ node -e "console.log(process.versions.v8 + \" - \" + process.arch)"
5.0.71.52 - x64
vladima@vladima-HP:~/Sources/play/test2/tsc-repro$ time node tsc/tsc.js -p vscode/src

real	0m7.377s
user	0m7.840s
sys	0m0.332s
vladima@vladima-HP:~/Sources/play/test2/tsc-repro$ ~/Tools/node-v6.2.1-linux-x86/bin/node --version
v6.2.1
vladima@vladima-HP:~/Sources/play/test2/tsc-repro$ ~/Tools/node-v6.2.1-linux-x86/bin/node -e "console.log(process.versions.v8 + \" - \" + process.arch)"
5.0.71.52 - ia32
vladima@vladima-HP:~/Sources/play/test2/tsc-repro$ time ~/Tools/node-v6.2.1-linux-x86/bin/node tsc/tsc.js -p vscode/src

real	0m11.974s
user	0m13.792s
sys	0m0.316s

```

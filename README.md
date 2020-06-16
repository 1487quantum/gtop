
# gtop
Martin Kersner, <m.kersner@gmail.com>, 2017

## Description
`gtop` is CPU, GPU and memory viewer utilizing information provided by `tegrastats` (terminal utility for [NVIDIA<sup>&reg;</sup> JETSON<sup>&trade;</sup>](http://www.nvidia.com/object/embedded-systems-dev-kits-modules.html) embedded platform). It requires `ncurses` and its output resembles [`htop`](https://github.com/hishamhm/htop).

<p align=center>
<img src="http://i.imgur.com/oMHuVSX.png" align="center"/>
</p>

## Prerequisites
```
sudo apt-get install libncurses5-dev libncursesw5-dev
```

## Installation instruction
Git clone the repository:
```bash
$ git clone https://github.com/1487quantum/gtop.git
```
Enter the directory and compile the code:
```bash
$ cd gtop
$ make
```
Copy the "fake" bin & `gtop` to `/usr/local/bin`: 
```bash
$ sudo cp tegrastats_fake /usr/local/bin
$ sudo chown root: gtop
$ sudo mv gtop /usr/local/bin
```
Run gtop:
```bash
sudo gtop --tx2
```
> Reference: [https://github.com/martinkersner/gtop/issues/8](https://github.com/martinkersner/gtop/issues/8)

It is recommended to create alias for `gtop` so it can be used from any directory. Add following line to your *.bashrc* file
```bash
alias gtp="sudo gtop --tx2"
```

## License
GNU General Public License, version 3 (GPL-3.0)

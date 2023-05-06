# java-install
Download the java-package:
https://www.oracle.com/java/technologies/downloads/
> select the debian one

Go to the downloaded directory where package is downloaded:
```bash
sudo dpkg -i jdk-20_linux-x64_bin.deb
```
if it throws error of `libc6-x32` , then run this command:
```bash
sudo apt-get install libc6-x32
```
```bash
sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk-20/bin/java 1
```
> select the version and type it accordingly: Like in my case it is `jdk-20`

Similarly
```bash
sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk-20/bin/javac 1
```
now check java and javac
```bash
java --version
javac --version
```
Recheck the alternative versions are there or not
```bash
sudo update-alternatives --config java
```

```bash
sudo update-alternatives --config javac
```

Note: Now if you want, then you can create `$JAVA_HOME`
```bash
sudo vim /etc/profile
```
Enter this thing at the last: `JAVA_HOME=/usr/lib/jvm/jdk-20`
and then save and exit

```bash
source /etc/profile
```

Check now:
```bash
echo $JAVA_HOME
```

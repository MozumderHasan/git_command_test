# Linux Basic Command

## Linux
### User Create
```
sudo useradd jihad -g 1003
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/1.user%20cretae%20with%20user%20group.png?raw=true)
### Create Directory
```
mkdir os-concepts
mkdir ubuntu-is-the-best
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/create%20directory.png?raw=true)


#### Create two files on each directory
```
touch os.txt
touch os1.txt
touch ubuntu.txt
touch ubuntu1.txt
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/3%20create%20file.png?raw=true)
#### List the files with detailed information ( including file permission )
```
ls -l
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/4.1%20file%20details.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/4.2%20file%20details.png?raw=true)
![Alt text]()
![Alt text]()
#### Update file permission so that owner can read,write and group can only read and others can not do anything
```
sudo chmod 640 os1.txt os.txt
sudo chmod 640 ubuntu.txt ubuntu1.txt
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/5.1%20file%20permission.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/5.2%20file%20permission.png?raw=true)


#### Create another group
```
sudo groupadd miraz
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/6.1%20create%20group.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/6.2%20group%20name.png?raw=true)
#### Update file ownership to the newly created group
```
sudo chown hasan:miraz ubuntu.txt
sudo chown hasan:miraz ubuntu1.txt
sudo chown hasan:miraz os.txt
sudo chown hasan:miraz os1.txt
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/7.1%20ownership%20change.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/7.2%20ownership%20change.png?raw=true)
#### Add the user to the new group
```
sudo usermod hasan -g 1004
```
![Alt text]()
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/8.1%20add%20user%20to%20new%20group.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/8.2%20info%20of%20changes.png?raw=true)
#### Create a file called crash.in ( File should contain the word crash in it ) in different directories and then find the file in all the locations using find command
```
touch crash.in (Desktop,os-concepts,ubuntu-is-the-best)
find ~ -type f -name "crash.in"
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/9.1%20crash%20file%20create.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/9.1%20found%20crash%20file.png?raw=true)
#### Then, replace the lines with crash to broken to all files ( use sed, xargs )


```
##### this command run specific directory wise run
sed -i 's/crash/broken/g' crash.in

##### This command find the location of file and change the specific text

find . -name "crash.in" -exec sed -i 's/crash/broken/g' {} \;
```
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/10.1%20change%20.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/10.2.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/10.3.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/10.4.png?raw=true)
![Alt text](https://github.com/MozumderHasan/Linux-basic-command/blob/main/assignment%20images/10.5%20find%20sed.png?raw=true)
## Windows
### Install Python Requirements
```pip install -r requirements.txt```
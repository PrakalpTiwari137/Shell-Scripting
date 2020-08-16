# Unix/Linux Shell scripting
Before you add anything else to your script, you need to alert the system that a shell script is being started. This is done using the shebang construct.
```
#!/bin/sh
```
Save the content and make the script executable:
```
$chmod +x test.sh
```
To execute the script:
```
$./test.sh
```
</br>
### Shell variables
**Variable names** </br>
By convention, unix shell variables will have names in UPPERCASE. </br></br>
**Defining variables** </br>
```
variable_name=variable_value
```
For example : `NAME="Prakalp Tiwari` </br>
Variables of this type are called scalar variables and these can hold one value at a time. </br></br>
**Accessing values** </br>
Variable values are accessed using dollar sign `$`
```
#!/bin/sh
NAME = "Prakalp Tiwari"
echo $NAME
```
</br>
**Special Variables** </br>
`$0` : The filename of the current script.</br>
`$n` : Correspond to arguments with which the script was invoked. First argument is $1, second argument is $2 and so on. </br>
`$#` : Number of arguments supplied to the script. </br>
`$$` : The process number of the current shell. </br>
`$*` : All arguments are double quoted. </br>
```
#!/bin/sh
echo "File Name: $0"
echo "First Parameter : $1"
echo "Second Parameter : $2"
for TOKEN in $*
do
   echo $TOKEN
done
```
Sample output: 
```
$./test.sh Prakalp Tiwari
File Name: ./test.sh
First Parameter : Prakalp
Second Parameter : Tiwari
Prakalp
Tiwari
```

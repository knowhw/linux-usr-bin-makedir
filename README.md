
# makedir
~~~python
from sys import argv
from os import mkdir as makedir

from collections import deque 


import os


de = deque() 
push=de.append

directorys=chr(32).join(argv[1:]).split(chr(47))
for subdir in directorys:
	push(subdir)
	
	
	pwd = os.path.join(os.getenv("PWD"), chr(47).join(de))
	
	
	if os.path.exists(pwd):
		os.chdir(pwd)
	else:
	
		makedir(subdir); os.chdir(pwd)
~~~
		
	
	
	
<br/>

## Installation
~~~
git clone https://github.com/knowhw/linux-usr-bin-makedir.git
sudo cp -R linux-usr-bin-makedir/makedir /usr/bin

chmod +x /usr/bin/makedir
~~~

## Usage
~~~
cd /home/linux
makedir documents/works
~~~


	
	

	
	
	

	
	









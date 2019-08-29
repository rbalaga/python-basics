threading allows us to run multiple processes parallel.
`threading` module allows us to create threads and work with it.

Lets see a simple example
```py
import threading
import time

def myPrintFunc():
	print('Starting a thread')
	time.sleep(3)
	print('Ending a thread')

threads = []

for i in range(5):
	th = threading.Thread(target=myPrintFunc)
	th.start()
	threads.append(th)

for th in threads:
	th.join()
```
Output
```
Starting a thread
Starting a thread
Starting a thread
Starting a thread
Starting a thread
Ending a thread
Ending a thread
Ending a thread
Ending a thread
Ending a thread
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI2ODczMzgyOSwtMTA1MDU4NTU5Nl19
-->
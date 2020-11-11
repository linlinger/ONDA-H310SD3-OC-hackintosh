#  NVRAM fix up guide 

Go to BIOS settings by pressing del.

Go to Advanced ---> RAM disk configuration 

set Disk Memory type to Boot Service Data. That what we extractly need for macOS NVRAM.

Select Create raw, Create and exit. You will see RAM disk 0 , it's disabled by defaullt. Go and enable it .

Save setting and restart. It's good to go.

If you dont konw how to do just follow instruction in pictures.

# Tips for check NVRAM working or not.

Type "sudo -s" for root access for the next steps.

Type "nvram -p" you will see this 



![Screen Shot 2020-11-11 at 12.06.46 PM](/Users/linlinger/Library/Application Support/typora-user-images/Screen Shot 2020-11-11 at 12.06.46 PM.png)

If there's nothing,NVRAM probably not functioning . Try apply NVRAM fixes.

If you don't know just type nvram -c to clear entire NVRAM ![Screen Shot 2020-11-11 at 12.09.24 PM](/Users/linlinger/Library/Application Support/typora-user-images/Screen Shot 2020-11-11 at 12.09.24 PM.png)

Maybe you will meet some error.Just ignore it and type nvram -p again.  Much less.

Go and type nvram myvar=test to create a variable named myvar with a value test.

Go and restart you computer. Open terminal and type nvram -p | grep myvar to found a variable you perviously defined . 

![Screen Shot 2020-11-11 at 12.14.29 PM](/Users/linlinger/Library/Application Support/typora-user-images/Screen Shot 2020-11-11 at 12.14.29 PM.png)

When you see this , congratulations for a  working NVRAM.


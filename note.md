#第一部分linus

###cd
   change directory
###pwd
   print name of CurrentWorking Directory
###mkdir
   make  a directory or use -p for farther‘s directory
###rm
   remove files or use -r(f) to remove directories with its contents

   rm -r dir1(/)  rm -r dir1/* to retain a empty directory
###ls
   list directory contents
###cp
   copy files or use -r for copy directory
###chmod
   change file mode bits

   ten numbers for one to style,three to user,three to group,three to others

   r:read 
 
   w:writer 
 
   x:layout
###tar
 压缩和解压两种格式:  

        tar zcvf dir.tar.gz. dir 

        tar zxvf dir.tar.gz    

and:

	tar jcvf dir.tar.gz. dir

	tar jxvf dir.tar.gz

#vim/vi
        i:insert  
    
        o:open  # a new line to inputo sth    
    
        qiut: :wq/q/q!/ shift+zz
  
        search: /***   __ "n"__ for next*** __"N__" for last ***
  
        set number/nonumber

        ~/vim .vimrc set number
                    
		        /hidden
###setting the bash

first back to the home directiry 
     
        ~$ vim .bashrc

second find the last line and input

        #alias for apt-get

        alias aaa='sudo apt-get install'

then  back to the home directory

       1、~$ source .bashrc

       2、close the bash and open a new bash 

after one of them we can use 'aaa'to instead 'sudo apt-get install' then to download sth

###download a plugin to use Tab in vim
       search 'snipMate'in the web then download the snipmate.zip

       unzip the file:~$ unzip snipmate.zip -d ~/.vim     #download in the directory of .vim

added a order for test

       ~$ cd .vim/sinpmate

       vim c.snipmate

      (input) # added for test

               snippnet dog

      (use 'Tab')        I love dog       
__ annotation(注释)__:in the content of c.snipmate includes some numbers means the location of cursor(光标)

###buffer
open one vim to another

	   eg : vim a.c b.c

	      :bn  # buffer next

	      :bp  #buffer previous

	      :bd  #buffer delete one vim

	      :e b.c   #to edit b.c
###different
find the differce from two files

	diff -u a.c a1.c ( > a.diff)    #output the differce between the two files(hold to a.diff ) 

	patch a.c < a.diff              # add a.diff to a.c

	patch -R a.c < a.diff

###git

	  mkdir a                            

	  cd a                              

	  vim a.c                            

	  ls -a                                 #find no a directory called .git

	  git init                              #add the .git

	  git add a.c                           #follow a.c

	  git commit -a -m "m"              #the first modify a.c for message

	  tig                               use d to find diff

	__If__ modify the a.c  then    "git commit -a -m "message"" 

	  then continue use "tig" and "d"

git reset --hard HEAD             #resume the last modify

git reset --hard HEAD^            #resume the last <git commit -a -m "**">

###download
	  git clone http:/********          # download the webpage content

	  git pull                          #renew the origin things from webpage

	(also use "tig" to find the new contents)
###uploading
(www.github.com)
 
 first sig in an account number
 
 second build a new resp.
 
 account the ssh-key:
        
	   ~$ ssh-keygen

    	   input enter 3 times

           ~$ cd .ssh
	
	   .ssh$ vim .id_rsa.pub
	
then copy the contents of them and paste them in account ssh-key 

(this is mean that we have set up the line to  connect user and the web    

###markdown
(which is based on the language of HTML)
	  vim a.md 

	  markdown a.md > a.html

	  firefox a.html 

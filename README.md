Introduction:
-------------
Getting started with vim could be a really difficult and boring task. Although vim is a really fun and easy tool, it is so different from Geany or Cloud9. This pre-configured vim package is something that hopefully can help anyone who just started to use vim like it as much as we do. 

In the package, there are a pre-configure .vimrc with all the configurations that can help coding faster. Wonder why? Download it and you can see the result. 

As for the nine selected plugins, each are popular ones that every vim users should know. Want to jump between folders with a few keys? Want to comment a whole paragraph with just a snap? The nine selected plugins have features that make programming easier than ever. 

Installation:
--------------
Before installng, make sure you have git and vim.

Type the command below to download .vimrc and all the included plugins.

	sh <(curl https://github.com/atan009/vimrc/raw/master/download.sh -L)

If the user already has .vim and .vimrc files, this installation will create a new directory called "old_vim_config" and move all the old files into it. 

vim :neckbeard::zzz:
-----------------------
Vim is a text editor that many programmers love to use. Not only is vim acailable on almost every Unix system, it also has a lot of powerful shortcuts that allows the users to do almost everything on the home tow. For instance, the user can jump to any line by typing `<linenumber> g`. Learning vim usually proves to be convenient and efficient.

To see what other programmers think about vim, go to [Stackoverflow: Is learning VIM worth the effort?](http://stackoverflow.com/questions/597077/is-learning-vim-worth-the-effort) 

To see what shortcuts other programmers love to use, go to [Stackoverflow: What is your most productive shortcut with Vim?](http://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim)

To learn more about what vim can do, go to [The Vim Editor: What Vim Can Do] (http://www.vim.org/about.php)

.vimrc :no_mouth::question:
-----------------------------
After reading vimtutor, the first thing the users should do is to edit their .vimrc file. .vimrc is a file that allows user to configure personal settings in vim. Although vim comes with many shortcuts, there are some features that users can only unlock with configuring their .vimrc file. For instance, to make vim shows line number, the user needs to add `set number` in the .vimrc file. 

The .vimrc in this pre-configured vim package contains a lot of configuration that are commonly used. Some of the configurations are commented out. If after looking at the .vimrc file and the user decides to use some of the configurations that was not included, just take out the comments. 

Remember, it is always good to understand what each line of the configuration does before leaving it in the .vimrc file.

Plugin:
-------
Even with vim and .vimrc, there are some features that users would wish vim could do. Simple tasks like commenting a paragraph or jumping between folders within a file are something that many programmers would love to be able to do. As a result, a lot of programmers started to write their own vim script file and enable these features. The vim script file that they write are called Plugin.Using plugins not only makes it easier and faster to code in vim, but it also personalizes the text editor for the programmer. 

In this pre-configured vim package, there are nine plugins that are popular amonog the vim-lovers:
	
	Pathogen	   simple plugin installation package
	NERDtree	   easily browse and access files and directories in tree form
	SuperTab	   fast typing filled-in aid
	Solarized	   stylish colorscheme
	Syntasitic	   best syntax error detector
	NERDcommenter  commenting helper
	Surround	   mapping tool
	EasyMotion	   fast searching/jumping tool
	Gundo		   simplistic undo tree
	Fugitive	   git wrapper

#####Modifications:
If the user wants to remove a plugin, just remove the directory of that plugin in the bundle directory. If the user wants to add a plugin, the first thing to do is to check whether the new plugin is compatible with the other plugins. If it is, simply install it by following the installation directions given by the creator. Depending on the plugin, the user may need to modify the .vimrc file to fit the plugins needs.

###Plugin #0 - Pathogen:
--------------------------
Pathogen is a plugin that will make installing other plugins easier. It also allows runtime files to be installed in their own private directories. Pathogen is not the only plugin manager, but it is the only one included here. There are many other plugin managers, but Pathogen appeared to be the most basic one.

Alternate Plugin Manager include [Github MarcWeber/vim-addon-manager] (https://github.com/MarcWeber/vim-addon-manager)
, [Github gmarik/Vundle.vim] (https://github.com/gmarik/Vundle.vim)
, [Github Shougo/neobundle.vim] (https://github.com/Shougo/neobundle.vim)

More info at: [Github tpope/vim-pathogen] (https://github.com/tpope/vim-pathogen)

###Plugin #1 - NERDtree:
-------------------------
NERDtree allows you to view your files and directories in the form of a tree. You can easily access your files by using the mouse or arrow keys this way. NERDtree allows the users to bookmark directories/files, open selected file within a file, checkout different folders, etc. 

After installing NERDtree, first the user will need to add `map <C-n> :NERDTreeToggle<CR>` in .vimrc. This enable the shortcut ctrl-n to open up NERDtree and view all the files in a tree form :+1:. 

User can navigate between files and firectories with the arrow keys. To read the files or directories, press `<ENTER>`. To close NERDtree type `NERDTreeClose`. 

![NT2](http://i.imgur.com/3OCe5YM.gif)

For more infomation about the creater, check [Github scrooloose/nerdtree] (https://github.com/scrooloose/nerdtree)

For more tips on NERDtree, go to [tuts+: Vim Essential Plugin: NERDTree](http://code.tutsplus.com/tutorials/vim-essential-plugin-nerdtree--net-19692)

###Plugin #2 - SuperTab:
--------------------------
SuperTab aids the user in quickly typing in strings of characters, but only pre-existing ones. This is useful for users that enjoy automatic text filling. By typing a few characters and pressing `<TAB>` the word will be filled automatically, unless there is more than one existing string with the same characters typed. In this situation, a list of words will be shown in which the user can choose the correct one by type `<TAB>` to alternate between different words.

![ST1](http://i.imgur.com/i12YWak.gif)

More info at: [Github ervandew/supertab] (https://github.com/ervandew/supertab)

###Plugin #3 - Solarized:
-------------------------
Solarized changes the colorscheme of the vim editor. Often times, the default is not the best. It can be extremely irritable when you cannot differentiate between different types of files in vim as well as the variety of things within source code. It is possible to change the font and customize the colors to your own
preference.

In the .vimrc file, type in below configuration to enable solarized colorscheme:

	"for light background
	syntax enable
	set background=light
	colorscheme solarized

	"for dark background
	syntax enable
	set background=dark
	colorscheme solarized

![Solarized2](http://i.imgur.com/HRqwlqz.png) ![Solarized3](http://i.imgur.com/sQKfCbm.png)

More info at: [Github altercation/vim-colors-solarized] (https://github.com/altercation/vim-colors-solarized)

Alternate color scheme: [Github sjl/badwolf] (https://github.com/sjl/badwolf/)
					, [Github tomasr/molokai] (https://github.com/tomasr/molokai)

###Plugin #4 - Syntastic:
---------------------------
Syntastic is a plugin which will save all programmers time. It detects for syntax errors BEFORE you even compile. As all programmers know, these errors happen by mistake all the time and can be annoying after receiving those thousands of other logic errors. A highly recommended plugin for anyone who hates searching through their code for one syntax error. Errors are identified only after everytime the file is saved. When highlighting a line of error, the error will be displayed at the bottom of the terminal. A line of error will be show with `>>` next
to it.

![Syntastic](http://i.imgur.com/LPHf6U7.gif)

More info at: [Github scrooloose/syntastic] (https://github.com/scrooloose/syntastic)

###Plugin #5 - NERDcommenter:
-----------------------------
NERDcommenter is a plugin that makes commenting easier. It also makes removing comments easier. All of the commands should be done in either visual or normal mode. Type `\cc` to comment out the line highlighted by the cursor. 

	\ci  toggle the state of the highlighted lines. 
	\cu  uncomment the line that the cursor is highlighting. 
	\cs  comment the highlighted using /* and */ rather than the ordinary //

![NC1](http://i.imgur.com/BU8Ffmg.gif) ![NC2](http://i.imgur.com/C7ZMtP7.gif)

More info at: [Github scrooloose/nerdcommenter] (https://github.com/scrooloose/nerdcommenter)

###Plugin #6 - Surround:
------------------------
Surround aids the user in adding, changing or deleting mappings. This includes parentheses, brackets and more. 

	cs[first character][second character] 
			replace occurences of the first character with the second character 
			on the highlighted string of characters 
	
	ds" 
			remove the delimiters

	yssb or yss)
			surround an entire line with parentheses 

![Surround1](http://i.imgur.com/7BjSTfR.gif) ![Surround2](http://i.imgur.com/upeOBA1.gif)

![Surround3](http://i.imgur.com/Ep8zeqz.gif) ![Surround4](http://i.imgur.com/VdIhp6T.gif)

More info at: [Github tpope/vim-surround] (https://github.com/tpope/vim-surround)

###Plugin #7 - EasyMotion:
--------------------------
EasyMotion helps you make large jump within a buffer easier and faster. It allows you to make jumps by searching up your destination. 

For one character search, enter `<leader><leader>w` (in vim, `<leader>` means `\`). A word `Target:` will appear in the commadn bar .Enter any character you want to search and EasyMotion will highlight all the appearances of the character in the buffer. Enter the one you want to jump to and EasyMotion will take you there.

![EasyMotionW](http://i.imgur.com/OuA4tDm.gif)

EasyMotion also supports word search. To do this, add two configurations to your .vimrc file. 
	
	map / <Plug>(easymotion-sn)
	omap / <Plug>(easymotion-tn)

After adding the configurations, you can search up word the way you do it in vim and EasyMotion will highlight the word for you.

![EasyMotionN] (http://imgur.com/DVc9xzl.gif)

For more EasyMotion configuration and explanation, go to [Github Lokaltog/vim-easymotion] (https://github.com/Lokaltog/vim-easymotion)

###Plugin #8 - Gundo:
---------------------
In vim, all the changes you make to your file are save as a tree. Gundo is a plugin that graph your vim undo tree for you so you can easily see the differences between the changes you made and jump back to any old version. 

To use Gundo, first you have to add a mapping to your .vimrc file. Here we use `<F5>` as example. 

	nnoremap <F5> :GUndoToggle<CR>

Now when we press `<F5>` in a file, Gundo will show us a graph of the tree of changes. Our current position in the undo tree is the one marker with `@`. To move between the graph, use `j` and `k` keys. Like vim, `gg` jumps to top of the file while `G` brings you ot the bottom of the file.  

Press `return` on a state to revert the content of the file and use `p` to make the preview window show the differences between current state and selected state. 

![Gundo](http://imgur.com/CJcWY8a.gif)

To quit the undo tree, press `q`. 

For more explanation on Gundo, go to [Gundo: Graph your Vim undo tree in style.] (http://sjl.bitbucket.org/gundo.vim/)

###Plugin #9 - Fugitive:
------------------------
As a git user, fugitive is probably the most useful plugin in this tutorial. It is a Git wrapper that collects and creates a lot of shortcuts of git. With fugitive, user can add, push, commit, checkout status or branches, and do any other things that they can do with `git`, but a lot faster. 

To make it easier, here are a list of fugitive commands:
	
	:Gstatus	git status
	:Gwrite		git add (filename)
	:Gcommit	git commit
	:Gblame		git blame
	:Gmove		git mv
	:Ggrep		git grep
	:Gread		git checkout --filename

The gif belows demonstrates how I check the status using :Gstatus, add my README.md using :Gwrite, commit the file using :Gcommit, and push the file to my repo using :Gpush.

![fugitive](http://imgur.com/Vqxu02C.gif)

For more explanation on `Fugitive`, go to [Github tpope/vim-fugitive] (https://github.com/tpope/vim-fugitive)



#Write your abe tags very easy with vim-plugin-for-abecms

##Install for INTELLIJ/PHPSTORM
Download ideaAbecms.jar and add it as a plugin in Preferences -> Plugins -> Install plugin from disk

##Install for vim
Add abecomplete.vim to .vim/autoload folder then add 

    setlocal completefunc=abecomplete#Complete

to your .vimrc file. 

##Use it
Start by taping one of the following letters for the corresponding type :
  
* t => text  
* i => image  
* tt => textarea  
* I => import  
* f => file  
* l => link  
* d => data  
* s => slug  

Then tape <Ctrl-X><Ctrl-U> or <Ctrl-RIGHT><Ctrl-RIGHT> for intellij/phpstorm, it will generate the tag.  
If you want it to autofill the key, description and tab, follow the letter with ":" and the key.


Example :

    i:header_cover_image

will give


    {{abe type='image' key='header_cover_image' desc='Cover image' tab='Header'}}

The description generated will be the key without the first word with spaces instead of dashes and a capital letter at the beginning.   
The tab will be the first word of the key with a capital letter.

If you do not put anything then a simple tag will be generated
Example :

    i

will give

    {{abe type='image' key='' desc='' tab='default'}}

By default the text type is generated.


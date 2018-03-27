# Imagebuilder for ar71xx generic  

## System Requirement  

- x86_64 platform  
- ubuntu or other linux  
- You need to install necessary software  

```bash  
$ sudo apt-get update
$ sudo apt-get install subversion build-essential git-core libncurses5-dev 
zlib1g-dev gawk flex quilt libssl-dev xsltproc libxml-parser-perl mercurial 
bzr ecj cvs unzip git wget
```  

## Download the Source  

```bash  
$ git clone https://github.com/gl-inet/lede-imagebuilder-ar71xx-nand.git
$ cd lede-imagebuilder-ar71xx-nand
```  

## Configuration  

You can change images.json file to install or remove packages for your  
preference. Note that "-pkgname" in the package list means remove "pkgname"  
from the package list.

## Create Image  

We can use gl_image utility to create image quickly. You can issue  
`gl_image --help` for help.  

For GL-AR300MD of v2.27:  
```bash  
Stoke firmware:  
$ ./gl_image -i v1 -p GL-AR300MNAND -v 2.27

Clean firmware:
$ ./gl_image -i clean -p GL-AR300MNAND -v 2.27
```  

We can use ourselves files with -f option, value is files directory name.  

Available image or profile is listed in images.json.  



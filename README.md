# NiiStat     
NiiStat for Octave     
     
## Installation     
1) Download Octave 4.4.1 and install it     
MacOS: https://octave-app.org/Download.html     
Linux: https://www.gnu.org/software/octave/download.html     
Windows: https://ftpmirror.gnu.org/octave/windows/     
Source: https://ftpmirror.gnu.org/octave        
          
2) Run Octave and install the io package       
In the Octave Command Window, run the following command:       
+ `pkg install -forge io`       
          
3) Download NiiStat     
Pick __one__ of the following methods:
a) Press the green "Clone or Download" button on the [GitHub](https://github.com/AnthonyAndroulakis/NiiStat) page. Extract the downloaded zip file. Renamed the extracted folder (NiiStat-master) to NiiStat. This is the easiest method to install the software.     
__OR__
b) From the command line, type `git clone https://github.com/AnthonyAndroulakis/NiiStat`. This requires you to have the git software installed. The advantage of this method is that the software will be kept up-to-date automatically.      
         
4) Download SPM and Compile it     
In the Octave Command Line,        
__cd into the NiiStat folder (that you just downloaded)__
__Download SPM12 r4787__       
+ `unzip('https://github.com/spm/spm12/archive/r7487.zip',pwd);`         
__Patch SPM12__      
+ `urlwrite('https://raw.githubusercontent.com/spm/spm-docker/master/octave/spm12_r7487.patch','spm12_r7487.patch');`     
+ `system('patch -p3 -d spm12-r7487 < spm12_r7487.patch');`      
__Compile MEX files__      
+ `cd spm12-r7487/src`      
+ `system('make PLATFORM=octave');`      
+ `system('make PLATFORM=octave install');`      
__Go back 2 levels to access NiiStat__         
+ `cd ../../`
           
5) Run NiiStat
+ `NiiStat`

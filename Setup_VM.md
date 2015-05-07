

## NGS course May 2015

## Setup Virtual Machine 

### Stefan Wyder

Ubuntu 14.04.2 LTS Desktop
wget http://mirror.switch.ch/ftp/mirror/ubuntu-cdimage/trusty/ubuntu-14.04.2-desktop-amd64.iso

Import into VirtualBox with 2GB Ram and 40GB dynamic extendable disk

student
NGS$2015


### 
opened terminal
locked terminal window in launcher:
cmd+click | <Lock from Launcher>


### Update Packages & System

sudo apt-get update
sudo apt-get dist-upgrade


### Helpers
sudo apt-get install samtools bedtools vcftools igv tabix fastqc sra-toolkit


cd
mkdir software
cd software
mkdir SOURCES


#### Picard
\#http://broadinstitute.github.io/picard/
cd ~/software
wget https://github.com/broadinstitute/picard/releases/download/1.130/picard-tools-1.130.zip
unzip picard-tools-1.130.zip
mv picard-tools-1.130.zip SOURCES/

#### IGV
\# Install Oracle java
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java7-installer

\# Get binary distribution from
\# https://www.broadinstitute.org/software/igv/download


### Mappers

sudo apt-get install tophat bowtie2


#### bwa
wget http://sourceforge.net/projects/bio-bwa/files/latest/download?source=files
mv "download?source=files" bwa.tar.bz2
bunzip2 bwa.tar.bz2
tar xf bwa.tar
bzip2 bwa.tar
mv bwa.tar.bz2 SOURCES/




###Variant Callers 

#### Freebayes
sudo apt-get install git cmake

cd ~/software
git clone --recursive git://github.com/ekg/freebayes.git
cd freebayes
make

#### GATK



### RNA-seq

#### HT-seq
sudo apt-get install python-htseq

#### R
\# installs latest R version
\# #for Ubuntu 12 LTS: sudo add-apt-repository 'deb http://stat.ethz.ch/CRAN/bin/linux/ubuntu precise/'
sudo add-apt-repository 'deb http://stat.ethz.ch/CRAN/bin/linux/ubuntu trusty/'
sudo apt-get update
sudo apt-get install r-base

\# installs dependencies for R
sudo apt-get install libxml2-dev
sudo apt-get install libcurl4-gnutls-dev

\# installs necessary R packages for URPP Tutorial on RNA-Seq
sudo R
source("http://bioconductor.org/biocLite.R")
biocLite("DESeq")
biocLite("DESeq2")  # DESeq is outdated, last version from spring 2013
biocLite("edgeR")
biocLite(c("RCurl","biomaRt"))
biocLite("goseq")
biocLite("GenomicFeatures")
biocLite("GO.db")
biocLite("org.Mm.eg.db")
quit()

## Stuff for Masa & co for Part 1
sudo apt-get install fastqc trimmomatic abyss
sudo apt-get install soapdenovo


## Installing Guest Additions (for copy&pasting and drag'n'drop betweeen host and VM)

see https://www.virtualbox.org/manual/ch04.html#idp96641072
(Guest is Linux so we have to follow the instructions for Linux)

sudo apt-get install dkms

Choose from the VMware menu while Ubuntu is running: Devices | Insert Guest Additions CD Image...


##
Use Right <Alt> for special characters like ~, | etc



ideas: Galaxy
Golden rules of bioinformatics




abmachen mit Heidi: Gene Ontology aufteilung
add download link for data



Installed software: 
Mo Heidi: HT-seq, R, Biconductor, edgeR, ???
Mo Stefan: topGO, GSEA, roast?
Tu Stefan: samtools, (mapper), BAM preprocessing (Picard?), GATK, Freebayes, samtools, bedtools, vcftools, IGVviewer, tablet

Galaxy?
 

Resize VM to 40 GB
widis-MacBook-Pro:~ swyder$ /Applications/VirtualBox.app/Contents/MacOS/VBoxManage modifyhd "/Users/swyder/VirtualBox VMs/NGS2_Course/NGS2_Course.vdi" -$




Dear all,

hereby we confirm your registration for the course "Next-Generation Sequencing 2: assembly, annotation and transcriptomes" on May 18/19 2015. 

The course will consist of lectures and computer exercises. For the computer exercises every student should bring a laptop (Mac, Windows or Linux) with at least 4 GB RAM and 10 GB free disk space. We will provide a virtual machine with all the necessary software installed. If you have questions or will not be able to bring a laptop send me an email.

We will meet at 9.30 am on the Irchel Campus Y42-K80 (for directions check 
http://www.plaene.uzh.ch/?z=4&lon=951701.77134833&lat=6007067.2835621&f=showAll&w=938&h=416&m=marker_building_Y42 ).

Looking forward to the course,
Best regards,
Stefan Wyder

# binaries
Some important binaries that I use quite often

**Note** - This GitHub repository contains two shell scripts that can be run as binaries on a UNIX based system only that is MacOS or Linux. All you need to do is download the raw format of the binaries or clone the github repo and then change the ownership of the scripts (for Linux only.) to use the command globally and then copy and paster the scripts in the user binary folder(ensure that the user bin is in the $PATH) or the system binary folder.

```console
foo@bar:~$ sudo chown -R root:root pdf2doi
```
and

```console
foo@bar:~$ sudo chown -R root:root doi2bib
```

If the files are not executable then use the following commands-

```console
foo@bar:~$ chmod +x pdf2doi
foo@bar:~$ chmod +x doi2bib
```

Then to paste it in the system binary folder do the following from the directory where you downloaded the scripts to- 

```console
foo@bar:~$ sudo cp pdf2doi /usr/bin
foo@bar:~$ sudo cp doi2bib /usr/bin
```
_____________________________________________________________________________________________________________________________

## PDF2DOI

The given script extracts the DOI or [Digital Object Identifier](https://www.doi.org/) from a given PDF file. For any research paper in PDF format the following is the usage -

```console
foo@bar:~$ pdf2doi <insert name of file>.pdf
10.xxxx/xxxxxxxxxxxx
```

## DOI2BIB

The DOI obtained from the pdf2doi script can then be plugged into the doi2bib binary script to obtain the [bibtex](http://www.bibtex.org/) Metadata and can be used in `References.bib` files for adding bibliography to your TeX or Markdown documents.

The following is a usage of both the binaries on a very intriguing paper on the Three Body problem and Machine Learning -

```console
foo@bar:~$ pdf2doi magnetic\ resonance.pdf
10.1007/BF01386092
foo@bar:~$ doi2bib 10.1007/BF01386092
@article{Cookson_2019,
	doi = {10.1119/1.5135797},
	url = {https://doi.org/10.1119%2F1.5135797},
	year = 2019,
	month = {dec},
	publisher = {American Association of Physics Teachers ({AAPT})},
	volume = {57},
	number = {9},
	pages = {633--635},
	author = {Esther Cookson and David Nelson and Michael Anderson and Daniel L. McKinney and Igor Barsukov},
	title = {Exploring Magnetic Resonance with a Compass},
	journal = {The Physics Teacher}
}
```

The paper which I am talking about is this one - [Exploring Magnetic Resonance with a Compass](https://arxiv.org/abs/1810.11141) by Esther Cookson et. al.

This will hopefully help in reducing the time it takes to get access of the bibtex of a file especially if you mostly keep your research articles locally on your maching and don't like using and maintaining personal online libraries like [Mendeley](https://www.mendeley.com/?interaction_required=true)

**Happy Coding!!**
_____________________________________________________________________________________________________________________________

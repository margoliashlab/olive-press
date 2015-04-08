# olive-press
Copies data in an [arf](https://github.com/melizalab/arf) file to new file with no chunking and gzip compression.
Data integrety is checked, then the original file is replaced, if the `--replace` flag is included.

The program `olive-press` improves both the size of data on disk (75% to 40% of original size)  and speed of analysis by removing
"chunking" in the storage of arrays.

![compression][compression.png]

## installation
`python setup.py install`


##usage
For usage help, type `olive-press -h`


    usage: unchunk [-h] [-c COMPRESSION] [-v] chunked_arf [chunked_arf ...]
    
    Copies data in arf file to new file with no chunking
    
    positional arguments:
      chunked_arf           input Arf file[s]
    
    optional arguments:
      -h, --help            show this help message and exit
      -c COMPRESSION, --compression COMPRESSION
                            compression level, 0 = none (fast), 9 = high (slow),
                            default: 9
      -v, --verbose
      --replace             replaces old arf file with new, compressed arf file

# olive-press
Copies data in arf file to new file with no chunking and gzip compression.
Data integrety is checked twice, then the original file is replaced.

olive-press improved both the size of data on disk (75% to 40% of original size)  and speed of analysis by removing
"chunking" in the storage of arrays.

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

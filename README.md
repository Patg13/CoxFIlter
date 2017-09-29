# CoxFIlter

CoxFIlter is a C++ program specially designed to efficiently 
detect and remove sequences containing an abnormal count of stop codons 

USAGE: 
   ./CoxFIlter  -f <fasta> -o <filename> [-s <filename>] -l < [integer >= 0] > [-t < [integer > 0] >] [-d] [--] [--version] [-h]
   
Where: 

   -f <fasta>,  --fasta_in <fasta>     (required)  Fasta file input (REQUIRED)
   
   -o <filename>,  --fasta_out <filename>     (required)  Fasta output name (REQUIRED)
   
   -s <filename>,  --scrap_out <filename>     Scrap fasta output name (Sequences rejected) (OPTIONAL)
   
   -l < [integer >= 0] >,  --stop_thr < [integer >= 0] > (required)  Stop codon count threshold ( everything greater is rejected, must be greater or equal then 0  ) (REQUIRED)
   
   -t < [integer > 0] >,  --num_threads < [integer > 0] > Number of threads to use (Default: 1)
   
   -d,  --debug     Display debug messages
   
   --,  --ignore_rest     Ignores the rest of the labeled arguments following this flag.
   
   --version     Displays version information and exits.
   
   -h,  --help     Displays usage information and exits.
   
   This program filter Cox sequences and reject those where the protein translation contain multiple stop codon
   
   WARNING : This program has been designed to be use with invertebrae mitochondria genetic code ONLY

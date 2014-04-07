---
layout: index
---
### What is the Kmerthon?

Kmerthon is a programming contest open to everyone. The goal is to write the fastest software to perform k-mer counting, a simple but extremely useful operation in bioinformatics.

### Problem Statement

K-mer counting consists of finding all the distinct DNA strings of length k inside a DNA data set, and reporting the number of times each of them occur. 

Two extra conditions must be satisfied. A k-mer and its [reverse complement](http://rosalind.info/problems/revc/) must be considered to be identical. K-mers containing the character N must be discarded.

Here is an example, where a toy value of k (3) is used.
Input (in the [FASTA](http://rosalind.info/glossary/fasta-format/) format):

    >seq1
    ACTGNTT
    >seq2
    CCTG

Output:

    ACT 1
    CAG 2
    AGG 1

This is a simple algorithmic problem. No knowledge in bioinformatics or biology is necessary to solve it.

### Why a Kmerthon?

K-mer counting is an important problem in bioinformatics. It is the first step of hundreds of tools (e.g. DNA/RNA assemblers). Designing fast k-mer counters remains an active area of research. Current solutions either need a lot of RAM or are disk-intensive. We hope that this contest will bring fresh algorithmic ideas. 


### Rules

* Participants will submit each entry as a .tar.gz package containing a k-mer counting program. See the section "How to Participate" for more details.
* Entries will be evaluated on the following Linux [EC2 instances](http://aws.amazon.com/ec2/pricing/):
 * m1.small (1 CPU, 1.7 GB RAM, 160 GB mechanical disk), the cheapest Amazon instance
 * r3.4xlarge (16 CPUs, 122 GB RAM, 320 GB SSD), a high-performance cluster node

<!---
 * c3.4xlarge (8 CPUs, 30 GB RAM, 320 GB SSD), a typical bioinformatics cluster node 
-->


* Entries will be evaluated by k-mer counting two datasets that will be unknown to the participants:
 * a RNA-seq experiment
 * a mammalian DNA-seq experiment
* Entries will be evaluated with k=32 and k=81.
* The only evaluation criteria will be the wall-clock running time, as measured by the Unix time command. Although we may also report other metrics for information purposes.
* Entries are not allowed to use any network interfaces.
* Entries can use as much RAM or disk space as available on an instance.
* Evaluation instances will be regenerated after each run of an entry.

### How to Participate

No registration is required. To enter the contest, submit a Github pull-request to `XXXX`. The pull-request has to be in a certain format. We provide a template here: XXX.

To facilitate evaluation, we enforce the following constraints:

* The k-mer counter needs to read its input from a FASTA file that will reside in the current directory and be named `input.fa` (see the Problem Statement for an example of the input format).
* The results must be written to `output.txt`, in the following format: a k-mer sequence, a space, then the number of times this k-mer occurs in the dataset (see the Problem Statement for an example of the output format).
* The k-mer counter must be executable via the following command line, where `<k>` specifies k: `./program <k>`


### Important Dates

* XXX: Contest begins
* XXX: Round 1 ends, Round 1 results published
* XXX: Round 2 ends, Round 2 results published
* XXX: Final Round ends, end of contest, final results published


### Organizers

* Name 1
* Name 2

### Contact

Please submit a ticket to `Github issues url` to ask any question regarding this contest.

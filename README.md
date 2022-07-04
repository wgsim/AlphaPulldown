# AlphaPulldown

## Pre-installation
Check if you have downloaded necessary parameters and databases(e.g. BFD, MGnify etc.) as instructed in [AlphFold's documentation](https://github.com/deepmind/alphafold) and you should have a directory like below:
 ```
 alphafold_database/                             # Total: ~ 2.2 TB (download: 438 GB)
    bfd/                                   # ~ 1.7 TB (download: 271.6 GB)
        # 6 files.
    mgnify/                                # ~ 64 GB (download: 32.9 GB)
        mgy_clusters_2018_12.fa
    params/                                # ~ 3.5 GB (download: 3.5 GB)
        # 5 CASP14 models,
        # 5 pTM models,
        # 5 AlphaFold-Multimer models,
        # LICENSE,
        # = 16 files.
    pdb70/                                 # ~ 56 GB (download: 19.5 GB)
        # 9 files.
    pdb_mmcif/                             # ~ 206 GB (download: 46 GB)
        mmcif_files/
            # About 180,000 .cif files.
        obsolete.dat
    pdb_seqres/                            # ~ 0.2 GB (download: 0.2 GB)
        pdb_seqres.txt
    small_bfd/                             # ~ 17 GB (download: 9.6 GB)
        bfd-first_non_consensus_sequences.fasta
    uniclust30/                            # ~ 86 GB (download: 24.9 GB)
        uniclust30_2018_08/
            # 13 files.
    uniprot/                               # ~ 98.3 GB (download: 49 GB)
        uniprot.fasta
    uniref90/                              # ~ 58 GB (download: 29.7 GB)
        uniref90.fasta
 ```

## Installation: via pip or singularity 

### Option1 (recommended): pip
This option is suitable for the users who have already installed and compiled [HMMER](http://hmmer.org/documentation.html) and [HH-suite](https://github.com/soedinglab/hh-suite)

**Firstly**, create a conda environment and gather necessary dependencies 
```bash
conda create -n <env_name> -c omnia python==3.7 openmm pdbfixer
````
**Secondly**, activate the environment and install AlphaPulldown
```bash
source activate <env_name>
pip install alphapulldown
```
### Option2 : singularity
For users who don't want to install [HMMER](http://hmmer.org/documentation.html) and [HH-suite](https://github.com/soedinglab/hh-suite) themselves, the programme can also be run via singularity. Simply download AlphaPulldown singularity image from [here](https://oc.embl.de/index.php/s/KR8d4m8ASN9p3gs)

------

## Manual
AlphaPulldown supports four different modes of massive predictions: ```pulldown```, ```all_vs_all```, ```homo-oligomer```, and ```custom```.

We have provided two examples:

Example 1 is a case where ```pulldown``` mode is used. Manual: [example_1](./example_1.md)

Example 2 is a case where ```custom``` and ```homo-oligomer``` modes are used. Manuals: [example_2_for_pip_user](./example_2_for_pip_user.md) or [example_2_for_singularity_user](./example_2_for_singularity_user.md)

```all_vs_all``` mode can be viewed as a special case of the ```pulldown``` mode thus the instructions of this mode are aded as Appendix in all the manuals mentioned above. 

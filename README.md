# 2017_melltrop_GBS

These are some quick notes about de-multipexing the mellotrop GBS data from a family.  These data were collected on two lanes that also included data from XB. Both lanes have the same samples with the same barcodes.  Both lanes are single end GBS data.  The file names are `C6GKHANXX_1_fastq.gz` and `C6GKHANXX_2_fastq.gz`.

Working directory on info: `/net/infofile4-inside/volume1/scratch/ben/2017_mellotropGBS_from_2015`

# Demultiplex:

```
/usr/local/bin/process_radtags -f C6GKHANXX_1_fastq.gz -i gzfastq -b barcodes_without_names -o ./samples_first_lane/ -e ecoT22I -r -c -q --filter_illumina
```
```
/usr/local/bin/process_radtags -f C6GKHANXX_2_fastq.gz -i gzfastq -b barcodes_without_names -o ./samples_second_lane/ -e ecoT22I -r -c -q --filter_illumina
```

```
mv sample_AACT.fq 3896_dad1.fq
mv sample_CTGCCA.fq 3896_dad2.fq
mv sample_TTCGACA.fq 3896_dad3.fq
mv sample_CTGCACA.fq 3896_dad4.fq
mv sample_ATACAAG.fq 3896_dad11.fq
mv sample_GTTGTCCA.fq 3896_dad22.fq
mv sample_GTGGCACA.fq 3896_dad33.fq
mv sample_AGTGTGCA.fq 3896_dad44.fq
mv sample_CCAG.fq 3897_mom1.fq
mv sample_ATCGCA.fq 3897_mom2.fq
mv sample_GATTACA.fq 3897_mom3.fq
mv sample_TACAGCA.fq 3897_mom4.fq
mv sample_GGTCCGA.fq 3897_mom11.fq
mv sample_AGAATACA.fq 3897_mom22.fq
mv sample_AGACCTCA.fq 3897_mom33.fq
mv sample_GTAACGCA.fq 3897_mom44.fq
mv sample_AACCA.fq 3727_boy.fq
mv sample_CGCTCA.fq 3728_boy.fq
mv sample_ATTAGCA.fq 3729_boy.fq
mv sample_AGTGACA.fq 3730_boy.fq
mv sample_AATGCCG.fq 3731_boy.fq
mv sample_CCTCCGCA.fq 3732_boy.fq
mv sample_CACTAGCA.fq 3733_boy.fq
mv sample_CACCGTCA.fq 3734_boy.fq
mv sample_CCACG.fq 3735_boy.fq
mv sample_TAACCG.fq 3736_boy.fq
mv sample_GCATCCA.fq 3737_boy.fq
mv sample_CTAGTCA.fq 3924_boy.fq
mv sample_CCAATGA.fq 3925_boy.fq
mv sample_TTCGGCCA.fq 3926_boy.fq
mv sample_TCTGTACA.fq 3927_boy.fq
mv sample_TCGTACCA.fq 3928_boy.fq
mv sample_TATAA.fq 3929_boy.fq
mv sample_ACTAGA.fq 3930_boy.fq
mv sample_CGCCTCA.fq 3931_boy.fq
mv sample_GCTCGCA.fq 3932_boy.fq
mv sample_TTCTGAA.fq 3971_boy.fq
mv sample_GAGTAACA.fq 3973_boy.fq
mv sample_TGGAGCCA.fq 3976_boy.fq
mv sample_ATCGTACA.fq 3940_girl.fq
mv sample_GAGCG.fq 3941_girl.fq
mv sample_GAATCA.fq 3942_girl.fq
mv sample_TCTGTCA.fq 3943_girl.fq
mv sample_GACTCAA.fq 3944_girl.fq
mv sample_GTGGACG.fq 3945_girl.fq
mv sample_AGATACCA.fq 3946_girl.fq
mv sample_GAACATCA.fq 3947_girl.fq
mv sample_GATAAGCA.fq 3948_girl.fq
mv sample_ACATA.fq 3949_girl.fq
mv sample_CCTAAG.fq 3950_girl.fq
mv sample_ATGTCCA.fq 3951_girl.fq
mv sample_AAGATCA.fq 3952_girl.fq
mv sample_AGAATCG.fq 3953_girl.fq
mv sample_CCGATGCA.fq 3955_girl.fq
mv sample_ACCTCGCA.fq 3956_girl.fq
mv sample_CCTGGTCA.fq 3957_girl.fq
mv sample_CTCAG.fq 3958_girl.fq
mv sample_TGGCAA.fq 3959_girl.fq
mv sample_CATGGCA.fq 3960_girl.fq
mv sample_CCTGCAA.fq 3961_girl.fq
mv sample_CACTGGA.fq 3962_girl.fq
mv sample_TGTCCACA.fq 3965_girl.fq
mv sample_CTTAGACA.fq 3966_girl.fq
mv sample_TTGTTACA.fq 4169_girlSp.fq
mv sample_GCTCCA.fq 4178_girlSp.fq
mv sample_GTAGCG.fq 4180_girlSp.fq
mv sample_TGACACA.fq 4177_girlSp.fq
mv sample_TTATACG.fq 4182_girlSp.fq
mv sample_TCTCAAG.fq 4183_girlSp.fq
mv sample_GTCGAGCA.fq 4184_girlSp.fq
mv sample_AAGGTCCA.fq 4185_girlSp.fq
mv sample_GGACTCCA.fq 4170_girlSp.fq
mv sample_CATGCA.fq 4172_boySp.fq
mv sample_GTTGCCA.fq 4173_boySp.fq
mv sample_GTCATCA.fq 4174_boySp.fq
mv sample_TGCACAA.fq 4181_boySp.fq
mv sample_CTGGCGA.fq 3810_boySp.fq
mv sample_AATAGCCA.fq 3799_dad1Sp.fq
mv sample_GGAAGTCA.fq 3799_dad2Sp.fq
mv sample_AATGCACA.fq 3799_dad3Sp.fq
mv sample_ACGTCA.fq 3800_mom1Sp.fq
mv sample_TGTTCCA.fq 3800_mom2Sp.fq
mv sample_TCGACCA.fq 3800_mom3Sp.fq
mv sample_GACCTCG.fq 3799_dad11Sp.fq
mv sample_CTAGACCA.fq 3800_mom11Sp.fq
mv sample_CCATGCCA.fq 4175_girlSp.fq
mv sample_CCGTCACA.fq 4171_boySp.fq
mv sample_CCGCATCA.fq 4176_boySp.fq
mv sample_TGAACA.fq 4179_boySp.fq
mv sample_TAAGCCA.fq 3799_dadPSp.fq
mv sample_AGATGCA.fq 3800_momPSp.fq
mv sample_CCGTGCA.fq 3896_dadP1.fq
mv sample_TCCTGACA.fq 3896_dadP2.fq
mv sample_TTCCTGCA.fq 3897_momP1.fq
mv sample_TGCCACCA.fq 3897_momP2.fq
mv sample_TTATGGCA.fq blank.fq
```

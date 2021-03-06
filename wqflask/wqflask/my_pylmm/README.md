# Genenetwork2/pylmm RELEASE NOTES 

## 0.51-gn2 (April 19, 2015)

- Improved GN2 integration
- Less matrix transposes
- Able to run pylmm standalone without Redis again (still requires
  the modules)

## 0.50-gn2 (April 2nd, 2015)

- Replaced the GN2 genotype normalization

## 0.50-gn2-pre2 (March 18, 2015)

- Added abstractions for progress meter and info/debug statements;
  Redis perc_complete is now updated through a lambda

## 0.50-gn2-pre1 (release, March 17, 2015)

- This is the first test release of multi-core pylmm into GN2. Both
  kinship calculation and GWAS have been made multi-threaded by
  introducing the Python multiprocessing module. Note that only
  run_other has been updated to use the new routines (so human is
  still handled the old way). I have taken care that we can still run
  both old-style and new-style LMM (through passing the 'new_code'
  boolean). This could be an option in the web server for users to
  select and test for any unexpected differences (of which there
  should be none, naturally ;).

- The current version can handle missing phenotypes, but as they are
  removed there is no way for GN2 to know what SNPs the P-values
  belong to. A future version will pass a SNP index to allow for
  missing phenotypes.


  
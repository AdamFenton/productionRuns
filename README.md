### Production Run Generation
---
First, run the `generate_production_run_table.py` script. This constructs a
table of all of the possible combinations of the parameter space using the
functions defined in `calculate_barotropic_EOS.py`. <br>

Then run `write_in_files.sh` which reads the values for ρc1, ρc2, ρc3, γ1, γ2,
γ3 and H/R from the `run_parameters.dat` file and then uses the IC template files
(disc_template.in and disc_setup_template.setup) to generate the disc.in and
disc.setup files for each of the runs. The script uses seq to find and replace
the placeholder values in the template files with the values from the
`run_parameters.dat` file.

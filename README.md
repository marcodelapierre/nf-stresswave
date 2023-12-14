## nf-stresswave

Basic pipeline to stress test Wave service 

Run using this command:

```
nextflow run marcodelapierre/nf-stresswave -r marco/config_aws -profile awsbatch,wave-stage --times <how many jobs to run>
```

Real case stress test:
```
for i in 1 2 4 8 16 32 60 ; do
  date
  nextflow run marcodelapierre/nf-stresswave -r marco/config_aws --times=$((i*100)) -profile awsbatch,wave-stage
  date
done
```

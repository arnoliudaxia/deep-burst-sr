# Deep-Burst-SR

## Environment
environment setting refer to `install.sh`
```
conda activate env-dbsr
export PYTHONPATH=$PYTHONPATH:$(pwd)
```

## Generate LR burst dataset

```
python util_scripts/generate_synthetic_dataset.py
# in data/synthetic_burst_generation.py change Bayerpattern
```

## Inference

```
python evaluation/synburst/save_results.py dbsr_default
python evaluation/synburst/compute_score.py dbsr_default --load_saved

```

## Visiulize

```
python evaluation/synburst/visualize_results.py dbsr_default
python util_scripts/visualize_synburst_val.py --mode srgb
```


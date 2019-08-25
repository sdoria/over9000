# Optimizers and tests 

## 5 epochs, 128px






Every result is avg of 20 runs. Optimizer uses a "flat and anneal" learning rate scheduler unless specified (e.g. "OneCycle")

| Dataset  | Baseline: Adam + OneCycle | Over9000 (RAdam + LARS + LookAHead) | Ralamb (RAdam + LARS) | Ranger (RAdam + LookAHead)| Novograd | Radam | Over9000 + OneCycle |
| ------------- | ------------- | --|-- | -- | -- | -- |
| Imagenette size 128, 5 epochs | 0.8577  | 0.8746 | 0.8657 | 0.8616 | 0.8724 | 0.8483 | 0.8692 |
| Imagewoof size 128, 5 epochs  | 0.6250  | 0.6539 | 0.5851 | 0.6086 | 0.6189 | 0.542 | TBD |


### Baseline (Adam)


Our learning rate and lr scheduler for the baseline is based on the best results from below: 

| Dataset | Learning Rate | lr Scheduler | Epochs | Accuracy |
| --- | --- | --- | --- | --- | 
| Imagenette | 2e-3 | OneCycle | 5 | 0.8517 |
| Imagenette | 3e-3 | OneCycle | 5 | 0.8577 |
| Imagenette | 4e-3 | OneCycle | 5 | 0.8553 |
| Imagenette | 6e-6 | OneCycle | 5 | 0.8535 |
| Imagenette | 1e-2 | OneCycle | 5 | 0.8461 |
| Imagenette | 3e-3 | flat_and_anneal | 5 | 0.8419 |



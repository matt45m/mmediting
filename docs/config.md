# Config System

We use python files as our config system. You can find all the provided configs under `$MMEditing/configs`.

## Config Name Style

We follow the below style to name config files. Contributors are advised to follow the same style.

```
{model}_[model setting]_{backbone}_[refiner]_[norm setting]_[misc]_[gpu x batch_per_gpu]_{schedule}_{dataset}
```

`{xxx}` is required field and `[yyy]` is optional.

- `{model}`: model type like `faster_rcnn`, `mask_rcnn`, etc.
- `[model setting]`: specific setting for some model, like `without_semantic` for `htc`, `moment` for `reppoints`, etc.
- `{backbone}`: backbone type like `r50` (ResNet-50), `x101` (ResNeXt-101).
- `[refiner]`: refiner type like `pln` (Plain Refiner).
- `[norm_setting]`: `bn` (Batch Normalization) is used unless specified, other norm layer type could be `gn` (Group Normalization), `syncbn` (Synchronized Batch Normalization).
- `[misc]`: miscellaneous setting/plugins of model, e.g. `dconv`, `gcb`, `attention`, `albu`, `mstrain`.
- `[gpu x batch_per_gpu]`: GPUs and samples per GPU, `8x2` is used by default.
- `{schedule}`: training schedule, `20k`, `100k`, etc.
`20k` means 20,000 iterations.
`100k` means 100,000 iterations.
- `{dataset}`: dataset like `places` (for inpainting), `comp1k` (for matting), `div2k` (for restoration) and `paired` (for generation).

## Config File Structure

Please refer to the corresponding page for config file structure for different tasks.

[Inpainting](config_inpainting.md)

[Matting](config_matting.md)

[Restoration](config_restoration.md)

[Generation](config_generation.md)


## FAQ

### Ignore some fields in the base configs

[TODO]

### Use intermediate variables in configs

[TODO]
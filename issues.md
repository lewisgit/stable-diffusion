# cannot import name 'autocast' from 'torch'
solution: https://www.reddit.com/r/StableDiffusion/comments/x79mfm/cannot_import_name_autocast_from_torch/

Replace
```sh
 from torch import autocast
```
with
```sh
from torch.cuda.amp import autocast
```
and change precision_scope("cuda") to precision_scope(True) in webui.py on line 820
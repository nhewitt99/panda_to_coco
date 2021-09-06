# panda_to_coco
Tools for annotating a PANDA dataset with HRNet and generating a COCO dataset.

# Usage
1. cd into hrnet submodule, follow install instructions, download 384x288 model
2. Modify deep-high-resolution-net.pytorch/demo/inference-config.yaml line 115 to include the deep-high-resolution-net.pytorch/ path prefix.
3. Run panda_decode.py to automatically annotate the PANDA dataset
4. Run panda_crop.py to create a cropped COCO dataset from the annotations
5. Run measure_bboxes.py to assess whether the output dataset fits expectations, if not, modify settings in panda_crop and try again

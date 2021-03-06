# panda_to_coco
Tools for annotating a PANDA dataset with HRNet and generating a COCO dataset.

# Usage
1. cd into hrnet submodule, follow install instructions, download 384x288 model
    * If make fails (i.e. if someone breaks nvcc), you can just copy the lib folder from an existing hrnet install.
2. Modify deep-high-resolution-net.pytorch/demo/inference-config.yaml line 115 to include the deep-high-resolution-net.pytorch/ path prefix.
3. cd back into panda_to_coco root directory
4. Run panda_decode.py to automatically annotate the PANDA dataset
5. Run panda_crop.py to create a cropped COCO dataset from the annotations
6. Run measure_bboxes.py to assess whether the output dataset fits expectations, if not, modify settings in panda_crop and try again

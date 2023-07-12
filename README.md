## Depth Estimation using DNN Architecture and Vision-Based Transformers

This repository contains code and models for our [paper](https://www.researchgate.net/publication/371233086_Depth_Estimation_using_DNN_Architecture_and_Vision-Based_Transformers):

> Depth Estimation using DNN Architecture and Vision-Based Transformers

### Setup 

1) Download the model weights and place them in the `weights`  create the folder if it's not there in the code folder:
   
Monodepth:
- [dpt_hybrid-midas-501f0c75.pt](https://github.com/intel-isl/DPT/releases/download/1_0/dpt_hybrid-midas-501f0c75.pt), [Mirror](https://drive.google.com/file/d/1dgcJEYYw1F8qirXhZxgNK8dWWz_8gZBD/view?usp=sharing)
- [dpt_large-midas-2f21e586.pt](https://github.com/intel-isl/DPT/releases/download/1_0/dpt_large-midas-2f21e586.pt), [Mirror](https://drive.google.com/file/d/1vnuhoMc6caF-buQQ4hK0CeiMk9SjwB-G/view?usp=sharing)

  
2) Set up dependencies: 

    ```shell
    pip install -r requirements.txt
    ```

   The code was tested with Python 3.7, PyTorch 1.8.0, OpenCV 4.5.1, and timm 0.4.5

### Usage 

1) Place one or more input images in the folder `input`.

2) Run a monocular depth estimation model:

    ```shell
    python run_monodepth.py
    ```
3) The results are written to the folder `output_monodepth` and `output_semseg`, respectively.


**Additional models:**

- Monodepth finetuned on KITTI: [dpt_hybrid_kitti-cb926ef4.pt](https://github.com/intel-isl/DPT/releases/download/1_0/dpt_hybrid_kitti-cb926ef4.pt) [Mirror](https://drive.google.com/file/d/1-oJpORoJEdxj4LTV-Pc17iB-smp-khcX/view?usp=sharing)
- Monodepth finetuned on NYUv2: [dpt_hybrid_nyu-2ce69ec7.pt](https://github.com/intel-isl/DPT/releases/download/1_0/dpt_hybrid_nyu-2ce69ec7.pt) [Mirror](https\://drive.google.com/file/d/1NjiFw1Z9lUAfTPZu4uQ9gourVwvmd58O/view?usp=sharing)

Run with 

```shell
python run_monodepth -t [dpt_hybrid_kitti|dpt_hybrid_nyu] 
```

### Evaluation

Hints on how to evaluate monodepth models can be found here: https://github.com/intel-isl/DPT/blob/main/EVALUATION.md


### Citation

Please cite our papers if you use this code or any of the models. 
```
@article{article,
author = {Kulkarni, Uday and Devagiri, Shreya and Devaranavadagi, Rohit and Pamali, Sneha and Negalli, Nishanth and Prabakaran, V.},
year = {2023},
month = {06},
pages = {02010},
title = {Depth Estimation using DNN Architecture and Vision-Based Transformers},
volume = {53},
journal = {ITM Web of Conferences},
doi = {10.1051/itmconf/20235302010}
}

### Acknowledgements

Our work builds on and uses code from [timm](https://github.com/rwightman/pytorch-image-models) and [PyTorch-Encoding](https://github.com/zhanghang1989/PyTorch-Encoding). We'd like to thank the authors for making these libraries available.

### License 

MIT License 

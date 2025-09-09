1. 克隆仓库

    ```bash
    git clone git@github.com:cucu9999/minimind-v.git
    # just4use
    git clone https://github.com/cucu9999/minimind-v.git
    ```

2. 下载模型

    ```bash
    1. clip模型
    # 下载clip模型到 ./model/vision_model 目录下
    git clone https://huggingface.co/openai/clip-vit-base-patch16
    # or
    git clone https://www.modelscope.cn/models/openai-mirror/clip-vit-base-patch16

    2. llm模型
    # 下载纯语言模型权重到 ./out 目录下（作为训练VLM的基座语言模型）
    https://huggingface.co/jingyaogong/MiniMind2-V-PyTorch/blob/main/lm_512.pth
    # or
    https://huggingface.co/jingyaogong/MiniMind2-V-PyTorch/blob/main/lm_768.pth

    3. /minimind-v 下载模型
    git clone https://huggingface.co/jingyaogong/MiniMind2-V
    ```

3. 环境配置

    ```bash
    conda create -n minimind-v python==3.10.16
    pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
    ```

4. 数据集准备

    ```bash
    https://huggingface.co/datasets/jingyaogong/minimind-v_dataset/tree/main
    ```
    > 1. 预训练阶段：pretrain_data.jsonl 、pretrain_images.zip   解压位于./dataset目录下 
    > 2. 微调阶段：sft_data.jsonl 、sft_images.zip   解压位于./dataset目录下


- 模型训练

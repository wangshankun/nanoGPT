
# nanoGPT 唐诗续写

The simplest, fastest repository for training/finetuning medium-sized GPTs. It is a rewrite of [minGPT](https://github.com/karpathy/minGPT) that prioritizes teeth over education. Still under active development, but currently the file `train.py` reproduces GPT-2 (124M) on OpenWebText, running on a single 8XA100 40GB node in about 4 days of training. The code itself is plain and readable: `train.py` is a ~300-line boilerplate training loop and `model.py` a ~300-line GPT model definition, which can optionally load the GPT-2 weights from OpenAI. That's it.


安装依赖Dependencies:
```
pip install transformers tiktoken tqdm

pyorch 和 numpy也需要安装:

pip install torch numpy
```

- [pytorch](https://pytorch.org) <3
- [numpy](https://numpy.org/install/) <3
-  `transformers` for huggingface transformers <3 (to load GPT-2 checkpoints)
-  `tiktoken` for OpenAI's fast BPE code <3
-  `tqdm` for progress bars <3

## quick start

```
生成训练和测试数据: ./0_vocab_tokenizer.sh
开始训练: ./1_train.sh
开始测试唐诗续写: ./2_test.sh

```

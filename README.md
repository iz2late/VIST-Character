# VIST-Character
This repository contains the dataset and accompanying code presented in the AAAI 2023 paper: [Detecting and Grounding Important Characters in Visual Stories](https://arxiv.org/abs/2303.17647).

## Dataset Description
VIST-Character dataset augments the test split of [VIST dataset](https://aclanthology.org/N16-1147/) with rich character-centric annotations, including visual and textual co-reference chains and importance ratings for characters.

## Data Format
The dataset is contained in a single JSON file, with each data point represented as a JSON object. The structure of a sample JSON object is as follows:
```
{
  "story": "the original VIST story",
  "meta_date": {
    "story_id": "the original VIST story id",
    "img_id": [
      "img_1",
      "img_2",
        ...,
      "img_5"]
  },
  "gt_char": {
    "C1"{
      "coref": [
        {
          "start":
          "end":
          "text":
          "labels":
        },
      ],
      "plural": "yes" or "no",
      "bboxes": {
        "img1" : [
        {
        "x": float,
        "y": float,
        "width": float,
        "height": float,
        },
        ...
        ]
        }
    }
    ...,
    "Cn"
  },
  "quality": the story quality on a scale of Great/Acceptable/Unacceptable.
}
```
## Citation

The purpose of this repository is to facilitate reproducibility and encourage further research using the dataset and code provided. If you use this dataset or code in your work, please cite our paper:
```bibtex
@article{liu2023detecting,
  title={Detecting and Grounding Important Characters in Visual Stories},
  author={Liu, Danyang and Keller, Frank},
  journal={arXiv preprint arXiv:2303.17647},
  year={2023}
}
```

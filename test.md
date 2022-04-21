---
title: "Object Detection과 Segmentation"
author: "Written by Aaron"
date: "2022-04-21"
output:
  html_document:
    #variant: markdown_github
    toc: true
    toc_depth: 2
    keep_md: true
---



## Dependancy

-   CNN
-   feature extractor network(convolution, kernel(filter), pooling, feature map)
-   VGG, rasnet etc

---

- 2012년도에 AlexNet이 ImageNet compatition에서 DL기반의 CNN을 사용
- 이 시점을 기준으로 DL에 대한 performance 등 여러 가능성이 증가함

<br><br>

## 1. Definition

<br>

#### Classification

- feature map과 label 등의 정보를 이용하여 이미지 분류

#### Localization

- 이미지 안에서 특정 영역을 한정 짓는 것
- 하나의 이미지에 하나의 object를 boundary box로 지정하여 예측


#### Detection

- 하나의 이미지에 다수의 Object
- 각 objectfmf boundary box로 구분하여 예측
- Region proposal과 classification
  - 동시에 진행되면 1stage detector
  - region proposal > classification이 순차적으로 진행되면 2stage detector
  - 포인트는 성능과 수행 시간이 반비례


#### Segmentation

- Detection에서 boundary box단위가 아니라 pixel 단위로 구분

<br><br>

## 2. Overview of Object Detection

- Region proposal
- DL network
  - Feature extractor network
  - FPN
    - feature extractor와 prediction network를 연결
    - 작은 object들에 대한 정보를 체계화시켜 분류
    - Object가 크다는 전제조건이 있다면 무시할 수도 있을지도..
  - Object Detection network
- 기타 요소
  - **IoU**
  - **NMS**
  - **mAP**
  - Anchor Box
  - etc ...




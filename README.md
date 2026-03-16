# SceneHMR-human-scene-reconstruction

## Overview

SceneHMR is a framework for aligning human meshes recovered from monocular images with reconstructed 3D scene geometry.

Traditional human mesh recovery models estimate pose and shape in the camera coordinate frame, which leads to ambiguous global scale and inconsistent placement in reconstructed scenes.

SceneHMR resolves this issue by aligning recovered human meshes to a metric scene coordinate system reconstructed from the same video.

## Method

The pipeline consists of four stages:

1. Scene reconstruction using VGGT and UniDepthV2
2. Person detection and segmentation using YOLO and SAM
3. Human mesh recovery using PromptHMR
4. Visibility-aware rigid alignment using ICP

This process produces scene-consistent human meshes that agree with reconstructed geometry.

## Pipeline

1. Monocular RGB video
2. Dense 3D scene reconstruction
3. Human detection and segmentation
4. SMPL mesh recovery
5. Visible surface extraction
6. ICP-based alignment

## Results

SceneHMR improves the global placement of human meshes within reconstructed environments.

Aligned meshes preserve correct scale, orientation, and human–scene interaction.

## Future Work

- Improve robustness under heavy occlusion
- Replace ICP with learning-based alignment
- Integrate memory-based reconstruction models

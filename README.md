# Dream Journey to the West — AI Video Generation Experiment

## 1. Project Overview

### Objective
用Google的Gemini Omni Flash Preview分段生成一条约 60 秒的视频，并考察不同分镜之间的连续性。

由于preview暂时无法修改分辨率、帧速率，而且没有实装multi-shots、运镜技巧等高级功能，因而在本次实验中无法进行这些操作。本次实验我会通过文生图模型来

aspect ratio: auto

thinking level: high

---

## 2. Storyboard

原始 8 个镜头表格

---

## 3. Workflow Design

### 3.1 Workflow Basis

This project adopts a keyframe-conditioned generation workflow inspired by the official Google Flow filmmaking guidance.

Google Flow recommends separating visual asset creation from video generation through:
- detailed prompts,
- reusable visual ingredients,
- Frames to Video,
- and scene-level assembly.

For this project, each shot is therefore designed around explicit visual keyframes before video generation.

### 3.2 Overall Pipeline

Storyboard
→ Character / Visual Design
→ Keyframe Generation
→ Keyframe Validation
→ Start + End Frame Conditioning
→ Motion Prompt Design
→ Video Generation
→ Shot Evaluation
→ Final Assembly
→ Continuity Evaluation

## 4. Keyframe Generation

### 4.1 Model Selection

Keyframes are generated using a high-performing text-to-image model selected based on the Artificial Analysis Text-to-Image Leaderboard.

Artificial Analysis evaluates image-generation models using blind pairwise human preference comparisons and Elo-based rankings.

Selection criteria:

1. Image quality
2. Prompt adherence
3. Character rendering quality
4. Cinematic composition
5. Availability
6. Cost

### 4.2 Selected Model

Model:
Artificial Analysis Elo:
Rank:
Cost:
Reason for selection:

### 4.3 Keyframe Strategy

Each video shot contains:

- Start Frame
- End Frame

The two frames define the desired spatial states of the shot, while the video model is responsible for generating the temporal transition between them.
# Dream Journey to the West — AI Video Generation Experiment

## 1. Project Overview

### Objective
Use Google's Gemini Omni Flash Preview to generate a video of approximately 60 seconds in separate shots and evaluate continuity across those shots.

The preview currently does not support custom resolution or frame rate, and advanced features such as multi-shot generation and explicit camera techniques are not yet available. This experiment therefore uses a text-to-image model to create explicit start and end keyframes for each shot before video generation.

Aspect ratio: auto

Thinking level: high

---

## 2. Storyboard

See the complete eight-shot plan in [storyboard/storyboard.md](storyboard/storyboard.md).

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

Keyframes are generated using a high-performing text-to-image model selected based on the Artificial Analysis Text-to-Image Leaderboard (choose the most suitable high-performing model).

Artificial Analysis evaluates image-generation models using blind pairwise human preference comparisons and Elo-based rankings.

Selection criteria:

1. Image quality
2. Prompt adherence
3. Character rendering quality
4. Cinematic composition
5. Availability
6. Cost

### 4.2 Selected Model

Model: GPT Image 2 (high)
Artificial Analysis Elo: 1370
Rank: 1
Cost: ChatGPT Plus
Reason for selection: Reachable and powerful

### 4.3 Keyframe Strategy

Each video shot contains:

- Start Frame
- End Frame

The two frames define the desired spatial states of the shot, while the video model is responsible for generating the temporal transition between them.

## 5. Prompt Design

### 5.1 Keyframe Prompt

Scene
→ Character
→ Composition
→ Pose / State
→ Camera
→ Lighting
→ Mood
→ Style
→ Continuity Constraints

### 5.2 Motion Prompt

Action
→ Character Motion
→ Camera Motion
→ Environmental Motion
→ Timing
→ Mood
→ Audio

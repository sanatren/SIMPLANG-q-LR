

<h1>Text Simplification with Deep Reinforcement Learning</h1>
Overview
This repository contains an implementation of a neural text simplification model that combines sequence-to-sequence learning with reinforcement learning and lexical-semantic loss. The model aims to simplify complex text while maintaining meaning and grammatical correctness.

<h1>Architecture</h1>
The model consists of several key components:
Encoder-Decoder with Attention: Uses LSTM layers with Bahdanau attention
Reinforcement Learning Agent: Optimizes for SARI score
Lexical-Semantic Loss: Maintains semantic meaning during simplification

<h1>Research Findings</h1>
Model Performance
1.Successfully combines supervised learning with RL

2.SARI score optimization through RL rewards

3.Effective semantic meaning preservation
Training Insights
Batch Size Impact
Larger batch sizes (128-256) show better convergence
Memory requirements increase significantly
Hardware Considerations
A100 GPUs provide optimal performance
H100 GPUs can reduce training time by 3-4x
Optimization Techniques
Mixed precision training
Gradient accumulation
Distributed training support
Future Work
[ ] Implement beam search for inference
[ ] Add support for multiple reference simplifications
[ ] Explore transformer-based architectures
[ ] Implement dynamic batch sizing
[ ] Add multi-GPU training support

under work... for more hypertuning


<h1>Performance Analysis</h1>
Training Metrics
Dataset: WikiLarge
Training pairs: 296,402
Validation pairs: 992
Test pairs: 359
Hardware Requirements
For optimal performance:
| GPU Model | VRAM | Batch Size | Training Time (50 epochs) |
|-----------|------|------------|---------------------------|
| A100 80GB | 80GB | 256 | ~1-1.5 days |
| A100 40GB | 40GB | 256 | ~ days |
| V100 32GB | 32GB | 128 | ~ days |
| T4 16GB | 16GB | 128 | ~ days |
Advanced Hardware Options
For faster training:
| GPU Model | VRAM | Batch Size | Est. Training Time |
|-----------|------|------------|-------------------|
| H100 80GB | 80GB | 512+ | ~ hours |
| 8x H100 | 640GB| 2048+ | ~ hours |
| 8x A100 | 640GB| 1024+ | ~ hours |


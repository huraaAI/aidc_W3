
# Model lock (team record)

Fill every field. This is your team's record of the model you serve for the rest of the course.

## The locked model

- Model id: Qwen/Qwen2.5-1.5B-Instruct-AWQ
- Quantisation: awq
- Why this one: It passed the function-calling smoke test 10/10 and provides the memory/capacity benefits of AWQ quantisation.

## The launch flags

The exact vLLM flags your team runs:

--model Qwen/Qwen2.5-1.5B-Instruct-AWQ --dtype half --max-model-len 4096 \
--gpu-memory-utilization 0.85 --quantization awq \
--enable-auto-tool-choice --tool-call-parser hermes

- Tool-call parser: hermes

## The smoke score

- Score (valid behaviours out of 10): 10
- Distractor stayed call-free in the majority: yes
- Passed the gate (>= 8/10 and distractor majority clean): yes
- Measured against: both — AWQ 10/10, fp16 10/10

## Quality spot check note

- AWQ showed some degradation on a few qualitative prompts, including awkward or unnecessary wording, but it remained functional and achieved a perfect 10/10 function-calling smoke score.

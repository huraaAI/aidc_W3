# Capacity note (team, one page)

## The numbers

- Locked model: `Qwen/Qwen2.5-1.5B-Instruct-AWQ`
- Target p95 end-to-end latency (your SLO today): `5.0 seconds`
- Knee concurrency (highest concurrency whose p95 is still under target):
  `16 (sweep-bounded)`
- Tokens per second at the knee: `723.8 tokens/s`
- Max sustainable request rate at the target p95: `7.2 req/s`

## The limiting family
- Memory-bound is the likely limiting family: decode repeatedly streams model weights from GPU memory, although this sweep did not yet reach the memory-bandwidth ceiling because throughput was still rising at concurrency 16.

## Why the knee, not the peak

- I report the knee at the SLO because it represents the highest concurrency I can sustainably promise while meeting the latency target, whereas peak throughput may occur after latency has become unacceptable.

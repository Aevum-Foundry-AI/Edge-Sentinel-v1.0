# Aevum Edge Sentinel backend — copy to .env and fill in. NEVER commit real secrets.

# Qwen Cloud (Alibaba Cloud Model Studio). OpenAI-compatible endpoint is set in code:
#   https://dashscope-intl.aliyuncs.com/compatible-mode/v1
DASHSCOPE_API_KEY=sk-your-qwen-cloud-key-here

# Model ids — confirm the exact strings in the Qwen Cloud console (they evolve).
QWEN_MODEL=qwen3.7-plus
QWEN_FAST_MODEL=qwen3.6-flash

# Consent token signing secret (fail-closed). Use a long random value in production.
CONSENT_SECRET=change-me-to-a-long-random-string

# Baseline store: "file" (dev / single instance) or "memory" (ephemeral).
# In production, swap for Alibaba Cloud Table Store or Redis behind memory.BaselineStore.
BASELINE_STORE=file
BASELINE_PATH=/tmp/edge_sentinel_baselines.json

# Set FORCE_MOCK=1 to run the deterministic offline agent (no API key needed).
# FORCE_MOCK=1

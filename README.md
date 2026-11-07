# Finper Julia

The on-device decision model used by Finper's voice assistant. It reads a short spoken phrase in Spanish and classifies it into an action of the app. It does not generate text.

- **File:** `finper-decide-v16.gguf`, published under [Releases](https://github.com/cgalvar/finper-julia/releases)
- **Format:** GGUF, Q8_0, mean pooling set in its metadata
- **Size:** 164,197,024 bytes
- **SHA-256 (v16):** `0790d3fbb99304fb378c63b7deef9140c6212097e99c14f53268aa59dc92bf81`

Since v14 the phrase is cleaned before the model reads it, in training and in the app: lowercase, no vowel accents (ñ stays), no punctuation except inside numbers.

This file holds the encoder only. The classification heads ship inside the app, so a release only works with the app version made for it. Each model is a new release, and old ones stay available.

## How it was made

The encoder of [SupersonicLabs/Julia-1](https://huggingface.co/SupersonicLabs/Julia-1) was fine-tuned on phrases written for this purpose. No user data was used for training.

## License

Apache License 2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE).

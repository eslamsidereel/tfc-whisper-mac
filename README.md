# tfc-whisper-mac

`whisper-cli` for macOS, built from [whisper.cpp](https://github.com/ggml-org/whisper.cpp)'s official source
(MIT licence, included in each release) for the TFC Captions After Effects panel.

whisper.cpp publishes no macOS command-line binary, and Homebrew no longer installs on Intel Macs. So this repo
builds one universal binary that runs natively on both:

- **Apple Silicon:** Metal GPU and Accelerate
- **Intel:** AVX2 and Accelerate

It is statically linked, so it needs nothing installed. Every build transcribes whisper.cpp's own sample on both
processor types before it is published.

Run the **build** workflow (Actions tab) with the whisper.cpp tag to build. It publishes the release
`whisper-<tag>-mac`.

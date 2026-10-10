# interactor-elixir-turboquant-llm

Elixir bindings for a vendored ggml language-model runtime with a quantised KV cache, as native functions.

## Use

`TurboquantLlm` downloads a GGUF model, starts an inference session, and runs blocking or streaming chat completions against it. The native code builds from the runtime vendored under `thirdparty/`, which carries the turboquant KV-cache quantisation.

## Build and run

The build needs CMake and a C++17 compiler:

```sh
mix deps.get && mix compile
mix test
```

## Licence

MIT. See [LICENSE](LICENSE). The vendored runtime is MIT, as its `LICENSE` states.

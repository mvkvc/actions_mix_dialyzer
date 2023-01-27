# actions_mix_dialyzer

This action runs `mix dialyzer` and caches the PLT files for faster subsequent runs.

## Usage

To include this action in your workflow, add the following line:

```yaml
- uses: actions_mix_dialyzer@v1.0.8-alpha
  with:
    - erlang-version:
    - elixir-version:
    ...
```

The full list of inputs are:

  ```yaml
inputs:
  erlang-version:
    description: Erlang version to use
    required: true
    type: string
  elixir-version:
    description: Elixir version to use
    required: true
    type: string
  args:
    description: Arguments to pass to `mix dialyzer`
    required: false
    type: string
    default: ''
  path_plt:
    description: Path to the PLT files relative to the Mix project
    required: false
    type: string
    default: dialyzer
  path_hash:
    description: Path to the hash file relative to the Mix project
    required: false
    type: string
    default: dialyzer/.plt_sha1
  path:
    description: Path to the Mix project
    required: false
    type: string
    default: .
```

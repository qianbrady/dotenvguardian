# DotEnvGuardian

Stop shipping broken configs. Two offline checks in one page:

1. **Diff** `.env` against `.env.example` — missing / extra / empty variables, duplicate keys in the example
2. **Code audit** — paste JS/TS or Python source, find *undocumented* reads (in code, not in example), *zombie* documentation (documented, never read) and *no-default* risks (`process.env.X` without `??`, bare `os.environ[...]`), scored 0-100 with dotenvelope's penalties (-12/-4/-6)

**Live tool:** https://qianbrady.github.io/dotenvguardian/ · 纯离线单文件。

![License](https://img.shields.io/badge/license-MIT-green)
![Offline](https://img.shields.io/badge/network-none-blue)

Ported from [dotenvelope](https://github.com/qianbrady/dotenvelope). Fidelity: parser maps and JS scanner output verified identical to the Python original on fixtures (comment blanking, `||`/`??` fallback detection, health-score arithmetic).

Note: the web audit uses the regex scan path (the CLI's own fallback); Python-AST precision remains CLI-only.

## License

MIT © 2025
<p align="center">
  <img src="Barge_icon.png" width="120" alt="Barge logo">
</p>

<h3 align="center">Find the code only one person knows — before they leave.</h3>

<p align="center">
  <a href="https://github.com/codebarge/barge/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/codebarge/barge?label=release&color=086862"></a>
  <img alt="Go 1.24+" src="https://img.shields.io/badge/go-1.24%2B-10847A">
  <img alt="No dependencies" src="https://img.shields.io/badge/dependencies-none-5DD1AE">
  <a href="https://gitlab.com/codebarge/barge/-/blob/main/LICENSE"><img alt="Apache 2.0" src="https://img.shields.io/badge/licence-Apache%202.0-03896A"></a>
</p>

<p align="center">
  <a href="https://gitlab.com/codebarge/barge/-/blob/main/DOCUMENTATION.md">Documentation</a> ·
  <a href="https://github.com/codebarge/barge/releases">Releases</a> ·
  <a href="https://gitlab.com/codebarge/barge/-/blob/main/CHANGELOG.md">Changelog</a> ·
  <a href="https://gitlab.com/codebarge/barge">GitLab</a>
</p>

---

**Barge** reads your git history and shows, for every module, who knows it and
how many people would have to leave before nobody does: the *bus factor*. It
runs on your machine: no code, names or history leave it, and there is no
telemetry.

```sh
go install gitlab.com/codebarge/barge/cmd/barge@latest
barge scan ~/code/your-project
```

```
RISK      BUS    AI  MODULE                  WHO KNOWS IT
critical    0     –  internal/paths          Dmitry 95% (inactive)
high        1   30%  pkg/compose             Oleg 56%, Anna 27%, Max 8%
high        1     –  relay                   Oleg 100%
medium      2   20%  cmd/compose             Oleg 52%, Anna 26%, Max 12%
```

Every scan ends with concrete next steps: who should take over an orphaned
module, who should become a second owner, whose knowledge to capture first.

- `barge scan --leaving oleg@acme.io`: see what breaks if someone leaves
- `barge handover oleg@acme.io -o handover.md`: a checklist of what only they
  know, a successor for each module and the questions worth asking
- `barge scan --only 'pkg/*' --fail-on critical`: watch one part of a monorepo in CI

Binaries for Linux, macOS and Windows are on the
[releases page](https://github.com/codebarge/barge/releases).

### Repositories

| Repository | What it is |
| --- | --- |
| [barge](https://github.com/codebarge/barge) | The CLI and analysis library. Go standard library only, Apache 2.0 |

### Barge for teams

Everything the CLI does, for all your repositories at once and over time:
a shared dashboard, alerts when a module becomes risky, short AI-assisted
handover interviews before someone leaves, and a knowledge base your AI coding
agents can ask over MCP. Self-hosted or in our cloud.

**[Request a pilot →](https://gitlab.com/codebarge/barge/-/issues/new?issuable_template=Pilot%20request)**
The request is confidential: only you and the maintainers see it.

<sub>Development happens on [GitLab](https://gitlab.com/codebarge/barge); this
organisation hosts a read-only mirror. Report a
[bug](https://gitlab.com/codebarge/barge/-/issues/new?issuable_template=Bug%20report),
suggest a [feature](https://gitlab.com/codebarge/barge/-/issues/new?issuable_template=Feature%20request)
or ask a [question](https://gitlab.com/codebarge/barge/-/issues/new?issuable_template=Question) there.</sub>

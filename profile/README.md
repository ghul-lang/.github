<img src="https://raw.githubusercontent.com/ghul-lang/ghul/main/images/ghul-logo-icon.png" alt="ghūl language logo" width="100"/>

# the ghūl programming language

ghūl is a statically typed, general-purpose programming language that targets .NET 10. It is a hobby project, but expressive enough for general-purpose work: the compiler is itself written in ghūl, and so are the runtime library, the test runner, the language server behind the editor tooling, and every other tool here. Programs compile to ordinary .NET assemblies and NuGet packages, and can use any .NET library.

The syntax is influenced by ALGOL 68 and Pascal. Blocks are delimited by keyword pairs whose closing half mirrors the opening one, so a class body runs `is` … `si`, a conditional `if` … `fi` and a `try` ends with `yrt`. Beyond that it is a fairly conventional language, with type inference inside function bodies, flow-sensitive narrowing, optional types, unions, traits, generics, first-class functions, pipes over lazy sequences, generators and async.

- [ghul.dev](https://ghul.dev) is the language documentation, with runnable examples on every page
- [the playground](https://ghul.dev/playground/) compiles and runs ghūl in the browser
- [Rosetta Code](https://rosettacode.org/wiki/Category:Ghul) has a thousand ghūl solutions, each one a tested project in [ghul-rosetta-code](https://github.com/ghul-lang/ghul-rosetta-code)

## the language

### [ghul](https://github.com/ghul-lang/ghul)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul/ci.yml?branch=main)](https://github.com/ghul-lang/ghul/actions/workflows/ci.yml?query=branch%3Amain)
[![NuGet version (ghul.compiler)](https://img.shields.io/nuget/v/ghul.compiler.svg)](https://www.nuget.org/packages/ghul.compiler/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul?label=release)](https://github.com/ghul-lang/ghul/releases)
[![Release Date](https://img.shields.io/github/release-date/ghul-lang/ghul)](https://github.com/ghul-lang/ghul/releases)
[![Issues](https://img.shields.io/github/issues/ghul-lang/ghul)](https://github.com/ghul-lang/ghul/issues)
[![License](https://img.shields.io/github/license/ghul-lang/ghul)](https://github.com/ghul-lang/ghul/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the compiler, a self-hosting compiler written entirely in ghūl; issues for every repository here are tracked in this one

### [ghul-runtime](https://github.com/ghul-lang/ghul-runtime)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-runtime/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-runtime/actions/workflows/cicd.yml?query=branch%3Amain)
[![NuGet version (ghul.runtime)](https://img.shields.io/nuget/v/ghul.runtime.svg)](https://www.nuget.org/packages/ghul.runtime/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-runtime?label=release)](https://github.com/ghul-lang/ghul-runtime/releases)
[![Release Date](https://img.shields.io/github/release-date/ghul-lang/ghul-runtime)](https://github.com/ghul-lang/ghul-runtime/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-runtime)](https://github.com/ghul-lang/ghul-runtime/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the runtime library every ghūl program builds against: the intrinsic operators, pipes, collections and the rest of the standard library

## tools

### [ghul-vsce](https://github.com/ghul-lang/ghul-vsce)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-vsce/CICD.yaml?branch=main)](https://github.com/ghul-lang/ghul-vsce/actions/workflows/CICD.yaml?query=branch%3Amain)
[![Visual Studio Marketplace](https://img.shields.io/visual-studio-marketplace/v/degory.ghul)](https://marketplace.visualstudio.com/items?itemName=degory.ghul)
[![Open VSX](https://img.shields.io/open-vsx/v/degory/ghul)](https://open-vsx.org/extension/degory/ghul)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-vsce?label=release)](https://github.com/ghul-lang/ghul-vsce/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-vsce)](https://github.com/ghul-lang/ghul-vsce/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the Visual Studio Code extension, and the language server it is built on, which is also published to npm as `@ghul/language-server`

### [ghul-cli](https://github.com/ghul-lang/ghul-cli)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-cli/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-cli/actions/workflows/ci.yml?query=branch%3Amain)
[![NuGet version (ghul.cli)](https://img.shields.io/nuget/v/ghul.cli.svg)](https://www.nuget.org/packages/ghul.cli/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-cli?label=release)](https://github.com/ghul-lang/ghul-cli/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-cli)](https://github.com/ghul-lang/ghul-cli/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the `ghul` command: runs a ghūl script directly, including from a `#!` line, and starts a REPL; also the REPL session library and a Jupyter kernel

### [ghul-debug](https://github.com/ghul-lang/ghul-debug)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-debug/CICD.yaml?branch=main)](https://github.com/ghul-lang/ghul-debug/actions/workflows/CICD.yaml?query=branch%3Amain)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-debug?label=release)](https://github.com/ghul-lang/ghul-debug/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-debug)](https://github.com/ghul-lang/ghul-debug/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the debug adapter, so ghūl programs can be debugged from the editor

### [ghul-mcp](https://github.com/ghul-lang/ghul-mcp)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-mcp/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-mcp/actions/workflows/ci.yml?query=branch%3Amain)
[![NuGet version (ghul.mcp)](https://img.shields.io/nuget/v/ghul.mcp.svg)](https://www.nuget.org/packages/ghul.mcp/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-mcp?label=release)](https://github.com/ghul-lang/ghul-mcp/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-mcp)](https://github.com/ghul-lang/ghul-mcp/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

an MCP server that answers questions about ghūl code from the compiler's analysis mode, for AI coding agents

### [ghul-raster](https://github.com/ghul-lang/ghul-raster)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-raster/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-raster/actions/workflows/cicd.yml?query=branch%3Amain)
[![NuGet version (ghul.raster)](https://img.shields.io/nuget/v/ghul.raster.svg)](https://www.nuget.org/packages/ghul.raster/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-raster?label=release)](https://github.com/ghul-lang/ghul-raster/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-raster)](https://github.com/ghul-lang/ghul-raster/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

draws into a PNG from ghūl, in managed code, with no native graphics library

### [ghul-test](https://github.com/ghul-lang/ghul-test)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-test/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-test/actions/workflows/cicd.yml?query=branch%3Amain)
[![NuGet version (ghul.test)](https://img.shields.io/nuget/v/ghul.test.svg)](https://www.nuget.org/packages/ghul.test/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-test?label=release)](https://github.com/ghul-lang/ghul-test/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-test)](https://github.com/ghul-lang/ghul-test/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

a snapshot-based integration test runner, used by the compiler and by every repository here that has programs to run

### [ghul-templates](https://github.com/degory/ghul-templates)

[![NuGet version (ghul.templates)](https://img.shields.io/nuget/v/ghul.templates.svg)](https://www.nuget.org/packages/ghul.templates/)
[![License](https://img.shields.io/github/license/degory/ghul-templates)](https://github.com/degory/ghul-templates/blob/main/LICENSE)

templates for `dotnet new` that create a ghūl console application or class library

### [ghul-repository-template](https://github.com/ghul-lang/ghul-repository-template)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-repository-template/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-repository-template/actions/workflows/cicd.yml?query=branch%3Amain)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-repository-template)](https://github.com/ghul-lang/ghul-repository-template/blob/main/LICENSE)

a template for starting a new ghūl repository on GitHub, with a build, tests and a release workflow already in place

## learning and examples

### [ghul-dev](https://github.com/ghul-lang/ghul-dev)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-dev/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-dev/actions/workflows/ci.yml?query=branch%3Amain)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-dev)](https://github.com/ghul-lang/ghul-dev/blob/main/LICENSE)

the [ghul.dev](https://ghul.dev) website: the language tutorial and reference, with every example compiled and run in CI

### [ghul-playground](https://github.com/ghul-lang/ghul-playground)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-playground/build.yml?branch=main)](https://github.com/ghul-lang/ghul-playground/actions/workflows/build.yml?query=branch%3Amain)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-playground)](https://github.com/ghul-lang/ghul-playground/blob/main/LICENSE)

the [browser playground](https://ghul.dev/playground/): a Monaco editor backed by the language server, a compile service, and a WebAssembly host that runs the result in the page

### [ghul-examples](https://github.com/ghul-lang/ghul-examples)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-examples/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-examples/actions/workflows/ci.yml?query=branch%3Amain)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-examples)](https://github.com/ghul-lang/ghul-examples/blob/main/LICENSE)

example programs, built and tested against every compiler release

### [ghul-rosetta-code](https://github.com/ghul-lang/ghul-rosetta-code)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-rosetta-code/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-rosetta-code/actions/workflows/ci.yml?query=branch%3Amain)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-rosetta-code)](https://github.com/ghul-lang/ghul-rosetta-code/blob/main/LICENSE)

the ghūl solutions on [Rosetta Code](https://rosettacode.org/wiki/Category:Ghul), each a runnable project with a test that checks its output, and the tool that publishes them

### [ghul-web-api](https://github.com/ghul-lang/ghul-web-api)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-web-api/build-and-test.yml?branch=main)](https://github.com/ghul-lang/ghul-web-api/actions/workflows/build-and-test.yml?query=branch%3Amain)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-web-api)](https://github.com/ghul-lang/ghul-web-api/blob/main/LICENSE)

an [ASP.NET](https://dotnet.microsoft.com/en-us/apps/aspnet) web API written in ghūl

### [ghul-scratchpad](https://github.com/ghul-lang/ghul-scratchpad)

a one-file project for trying ghūl in a Codespace

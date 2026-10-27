<img src="https://raw.githubusercontent.com/ghul-lang/ghul/main/images/ghul-logo-icon.png" alt="ghūl language logo" width="100"/>

# the ghūl programming language

ghūl is a statically typed, general-purpose programming language with three targets: .NET, WebAssembly and native executables through LLVM. It is a hobby project, but expressive enough for general-purpose work: the compiler is itself written in ghūl, and so are the runtime libraries, the test runner, the language server behind the editor tooling, and nearly every other tool here. On .NET a program compiles to an ordinary assembly or NuGet package and can use any .NET library; on the other two targets it builds against ghūl's own libraries and needs no .NET at all.

The syntax is influenced by ALGOL 68 and Pascal. Blocks are delimited by keyword pairs whose closing half mirrors the opening one, so a class body runs `is` … `si`, a conditional `if` … `fi` and a `try` ends with `yrt`. Beyond that it is a fairly conventional language, with type inference inside function bodies, flow-sensitive narrowing, optional types, unions, traits, generics, first-class functions, pipes over lazy sequences, generators and async.

- [ghul.dev](https://ghul.dev) is the language documentation, with runnable examples on every page
- [the playground](https://ghul.dev/playground/) and [the REPL](https://ghul.dev/repl/) compile and run ghūl in the browser
- [Rosetta Code](https://rosettacode.org/wiki/Category:Ghul) has over a thousand ghūl solutions, each one a tested project in [ghul-rosetta-code](https://github.com/ghul-lang/ghul-rosetta-code)

Issues for every repository here are tracked in [ghul](https://github.com/ghul-lang/ghul/issues).

## the compiler and the runtime

### [ghul](https://github.com/ghul-lang/ghul)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul/ci.yml?branch=main)](https://github.com/ghul-lang/ghul/actions/workflows/ci.yml?query=branch%3Amain)
[![NuGet version (ghul.compiler)](https://img.shields.io/nuget/v/ghul.compiler.svg)](https://www.nuget.org/packages/ghul.compiler/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul?label=release)](https://github.com/ghul-lang/ghul/releases)
[![Release Date](https://img.shields.io/github/release-date/ghul-lang/ghul)](https://github.com/ghul-lang/ghul/releases)
[![Issues](https://img.shields.io/github/issues/ghul-lang/ghul)](https://github.com/ghul-lang/ghul/issues)
[![License](https://img.shields.io/github/license/ghul-lang/ghul)](https://github.com/ghul-lang/ghul/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the compiler: about 200,000 lines of ghūl, compiling itself on every merge, with .NET, WebAssembly and LLVM back ends

### [ghul-runtime](https://github.com/ghul-lang/ghul-runtime)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-runtime/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-runtime/actions/workflows/cicd.yml?query=branch%3Amain)
[![NuGet version (ghul.runtime)](https://img.shields.io/nuget/v/ghul.runtime.svg)](https://www.nuget.org/packages/ghul.runtime/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-runtime?label=release)](https://github.com/ghul-lang/ghul-runtime/releases)
[![Release Date](https://img.shields.io/github/release-date/ghul-lang/ghul-runtime)](https://github.com/ghul-lang/ghul-runtime/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-runtime)](https://github.com/ghul-lang/ghul-runtime/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the runtime library every ghūl program builds against, on every target: the intrinsic operators, pipes, collections and the rest of the standard library

### [ghul-core](https://github.com/ghul-lang/ghul-core)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-core/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-core/actions/workflows/cicd.yml?query=branch%3Amain)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-core?label=release)](https://github.com/ghul-lang/ghul-core/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-core)](https://github.com/ghul-lang/ghul-core/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the base class library for the WebAssembly and native targets: strings, collections, exceptions and the console, in ghūl, standing in for the .NET base class library where there is none

### [ghul-llvm](https://github.com/ghul-lang/ghul-llvm)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-llvm/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-llvm/actions/workflows/ci.yml?query=branch%3Amain)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-llvm?label=release)](https://github.com/ghul-lang/ghul-llvm/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-llvm)](https://github.com/ghul-lang/ghul-llvm/blob/main/LICENSE)

the tool the compiler runs to turn the LLVM IR it writes into a native executable: an IR assembler, optimiser, code generator and linker in one program, built from LLVM's and LLD's libraries and shipped prebuilt

### [ghul-wasmtime](https://github.com/ghul-lang/ghul-wasmtime)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-wasmtime/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-wasmtime/actions/workflows/ci.yml?query=branch%3Amain)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-wasmtime?label=release)](https://github.com/ghul-lang/ghul-wasmtime/releases)

a standalone [wasmtime](https://wasmtime.dev) host that runs a ghūl program compiled for WebAssembly without Node.js

## tools and libraries

### [ghul-cli](https://github.com/ghul-lang/ghul-cli)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-cli/ci.yml?branch=main)](https://github.com/ghul-lang/ghul-cli/actions/workflows/ci.yml?query=branch%3Amain)
[![NuGet version (ghul.cli)](https://img.shields.io/nuget/v/ghul.cli.svg)](https://www.nuget.org/packages/ghul.cli/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-cli?label=release)](https://github.com/ghul-lang/ghul-cli/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-cli)](https://github.com/ghul-lang/ghul-cli/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the `ghul` command: builds the WebAssembly and native targets without the .NET SDK, runs a ghūl script directly, including from a `#!` line, and starts a REPL; also the REPL session library and a Jupyter kernel

### [ghul-vsce](https://github.com/ghul-lang/ghul-vsce)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-vsce/CICD.yaml?branch=main)](https://github.com/ghul-lang/ghul-vsce/actions/workflows/CICD.yaml?query=branch%3Amain)
[![Visual Studio Marketplace](https://badgen.net/vs-marketplace/v/degory.ghul)](https://marketplace.visualstudio.com/items?itemName=degory.ghul)
[![Open VSX](https://img.shields.io/open-vsx/v/degory/ghul)](https://open-vsx.org/extension/degory/ghul)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-vsce?label=release)](https://github.com/ghul-lang/ghul-vsce/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-vsce)](https://github.com/ghul-lang/ghul-vsce/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

the Visual Studio Code extension, and the language server it is built on, which is also published to npm as `@ghul/language-server`

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

### [ghul-test](https://github.com/ghul-lang/ghul-test)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-test/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-test/actions/workflows/cicd.yml?query=branch%3Amain)
[![NuGet version (ghul.test)](https://img.shields.io/nuget/v/ghul.test.svg)](https://www.nuget.org/packages/ghul.test/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-test?label=release)](https://github.com/ghul-lang/ghul-test/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-test)](https://github.com/ghul-lang/ghul-test/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

a snapshot-based integration test runner, used by the compiler and by every repository here that has programs to run

### [ghul-raster](https://github.com/ghul-lang/ghul-raster)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-raster/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-raster/actions/workflows/cicd.yml?query=branch%3Amain)
[![NuGet version (ghul.raster)](https://img.shields.io/nuget/v/ghul.raster.svg)](https://www.nuget.org/packages/ghul.raster/)
[![Release](https://img.shields.io/github/v/release/ghul-lang/ghul-raster?label=release)](https://github.com/ghul-lang/ghul-raster/releases)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-raster)](https://github.com/ghul-lang/ghul-raster/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

draws into a PNG from ghūl, in managed code, with no native graphics library

### [ghul-templates](https://github.com/ghul-lang/ghul-templates)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-templates/cicd.yml?branch=main)](https://github.com/ghul-lang/ghul-templates/actions/workflows/cicd.yml?query=branch%3Amain)
[![NuGet version (ghul.templates)](https://img.shields.io/nuget/v/ghul.templates.svg)](https://www.nuget.org/packages/ghul.templates/)
[![License](https://img.shields.io/github/license/ghul-lang/ghul-templates)](https://github.com/ghul-lang/ghul-templates/blob/main/LICENSE)

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

the [browser playground](https://ghul.dev/playground/) and [REPL](https://ghul.dev/repl/): a Monaco editor backed by the language server, a compile service, and a WebAssembly host that runs the result in the page

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

[![License](https://img.shields.io/github/license/ghul-lang/ghul-scratchpad)](https://github.com/ghul-lang/ghul-scratchpad/blob/main/LICENSE)

a one-file project for trying ghūl in a Codespace

## keeping the repositories running

### [ghul-coverage-report](https://github.com/ghul-lang/ghul-coverage-report)

[![License](https://img.shields.io/github/license/ghul-lang/ghul-coverage-report)](https://github.com/ghul-lang/ghul-coverage-report/blob/main/LICENSE)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

a test coverage report generator for ghūl projects, and the [compiler's own coverage report](https://ghul-lang.github.io/ghul-coverage-report/), regenerated twice a week

### [ghul-dashboard](https://github.com/ghul-lang/ghul-dashboard)

[![CI](https://img.shields.io/github/actions/workflow/status/ghul-lang/ghul-dashboard/build.yml?branch=main)](https://github.com/ghul-lang/ghul-dashboard/actions/workflows/build.yml?query=branch%3Amain)
[![ghūl](https://img.shields.io/badge/gh%C5%ABl-100%25!-information)](https://ghul.dev)

a terminal dashboard for a ghūl development machine: test runs in progress, and open pull requests with their CI and review state

### [ghul-code-review](https://github.com/ghul-lang/ghul-code-review)

a reusable GitHub Actions workflow that has an AI coding agent review every pull request and post the result as a formal review

### [ghul-renovate](https://github.com/ghul-lang/ghul-renovate)

the Renovate instance that keeps pinned versions current across the repositories here

### [create-version](https://github.com/ghul-lang/create-version)

[![Release](https://img.shields.io/github/v/release/ghul-lang/create-version?label=release)](https://github.com/ghul-lang/create-version/releases)
[![License](https://img.shields.io/github/license/ghul-lang/create-version)](https://github.com/ghul-lang/create-version/blob/main/LICENSE)

a GitHub Action that allocates the next version number for a release, from the latest tag and a `VERSION` floor

### [ghul-agent-guide](https://github.com/ghul-lang/ghul-agent-guide)

the standards a change to any repository here is held to, written for a coding agent working from a fresh clone

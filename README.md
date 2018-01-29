# E5R.Tools.Bit

Uma ferramenta mínima, extensível, independente e auto-suficiente para o desenvolvimento de software multiplataforma.

## Premissas:

* Ser o mínimo necessário para possibilitar portabilidade a vários sistemas operacionais, e leve o suficiente para um bootstrap rápido;

* Ser extensível para que se possa adicionar funcionalidades o quanto for necessário, sustentando inclusive uma comunidade e ecossistema;

* Ser independente de pré-requisitos de software, a não ser os essenciais: Shell e Internet;

* Ser auto-suficiente para que resolva suas dependências e extensões na execução de um único script shell sem argumentos;

## Build

### Build Status

Branch | AppVeyor | Travis-CI
------ | -------- | ---------
master | [![Build status](https://ci.appveyor.com/api/projects/status/ml0ktjidsvop9ods/branch/master?svg=true)](https://ci.appveyor.com/project/erlimar/bit/branch/master) | [![Build Status](https://travis-ci.org/e5r/bit.svg?branch=master)](https://travis-ci.org/e5r/bit)
develop | [![Build status](https://ci.appveyor.com/api/projects/status/ml0ktjidsvop9ods/branch/develop?svg=true)](https://ci.appveyor.com/project/erlimar/bit/branch/develop) | [![Build Status](https://travis-ci.org/e5r/bit.svg?branch=develop)](https://travis-ci.org/e5r/bit)

### Building on Windows:

```powershell
# Show help information
$ .\build.ps1 --help

# Show build options
$ .\build.ps1 --showdescription
```

### Building on Unix:

```sh
# Show help information
$ ./build.sh --help

# Show build options
$ ./build.sh --showdescription
```

> Mais detalhes nos arquivos [IDEA.md.](IDEA.md) e [DRAFT.md](DRAFT.md)

## Debugging on Visual Studio Code

```powershell
.\build.ps1 -Target=Bootstrap

# To ensure that you use the correct installation of
# the .NET SDK in "build/.dotnetsdk"
$env:Path = (Join-Path (Pwd) "build/.dotnetsdk") + ";${env:Path}"

# Launches the Visual Studio Code
code .
```

__TODO:__ Criar a configuração de depuração
__TODO:__ Criar a tarefa de build

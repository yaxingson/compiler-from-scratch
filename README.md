# compiler-from-scratch

English &nbsp; | &nbsp; [Chinese](./README.zh-CN.md)

## Prerequisite Knowledge

Basic Concepts:

- Translation: The process of converting the source program of one language into another language program **without changing its semantics**.
- Assembly: The process of translating assembly language into machine language.
- Compilation: The process of translating high-level language into assembly language or machine language.
- Interpretation: The process of interpreting and executing the source program code line by line.

```mermaid
flowchart LR
  SourceProgram --> id1{Preprocessor}
  id1 --> PreprocessedSourceProgram
  PreprocessedSourceProgram --> id2{Compiler}
  id2 --> AssemblyLanguageProgram
  AssemblyLanguageProgram --> id3{Assembler}
  id3 --> RelocatableMachineCode
  RelocatableMachineCode --> id4{Linker/Loader}
  id4 --> TargetMachineCode

```

Compilation Stages:

```mermaid
flowchart TB
  SourceLanguage --> LexicalAnalysis
  LexicalAnalysis --> SyntaxAnalysis
  SyntaxAnalysis --> SemanticAnalysis
  SemanticAnalysis --> IntermediateCodeGeneration
  IntermediateCodeGeneration --> Machine-IndependentCodeOptimization
  Machine-IndependentCodeOptimization --> TargetCodeGeneration
  TargetCodeGeneration --> Machine-DependentCodeOptimization

```

> Syntax-Directed Translation

## Implementation

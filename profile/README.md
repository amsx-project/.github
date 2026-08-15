<img src="https://github.com/amsx-project/.github/blob/main/banner/banner.png" alt="amsx-project banner"></img>

# AMSX-Project

**Building lightweight language models and a runtime for memory, perception, speech, personality, and action.**

[English](#english) · [日本語](#日本語)

---

<a id="english"></a>

# English

## About AMSX

**AMSX-Project** is a personal AI research and development project focused on:

> Developing the lightweight **amsx** language model series, integrated visual, auditory, and action capabilities, and a human-inspired memory system.

The project is not intended to build only a conversational LLM.

The long-term goal is to build an AI agent capable of continuous interaction, memory, perception, and action by connecting multiple components through **AMSX Runtime**.

AMSX is an experimental project under active development. Some components described below are currently being developed, while others are planned or being explored.

---

## Goals

AMSX-Project explores the integration of:

* Lightweight language models
* Short-term and long-term memory
* Visual perception
* Auditory perception
* Speech-to-Text
* Text-to-Speech
* Emotion state
* Personality
* Relationship awareness
* PC and game interaction
* Real-time conversation
* AI VTuber applications

Rather than placing every responsibility inside the language model, AMSX separates language intelligence from runtime-level state, perception, memory, and action.

---

## Current Model

### AMSX-ATRI-TB04-LLM

**AMSX-ATRI-TB04-LLM** is the current lightweight language model being developed as part of the AMSX series.

Development currently focuses on:

* Natural Japanese conversation
* Intent understanding
* Conversation history understanding
* Instruction following
* General conversational quality

The model itself is currently **closed** and is not intended for external distribution at this stage.

Details about its internal base model, technical provenance, training ancestry, and other non-public implementation details are intentionally not disclosed.

---

## AMSX Runtime

**AMSX Runtime** is the integration layer responsible for capabilities that are intentionally separated from the LLM itself.

### LLM responsibilities

The language model is primarily responsible for:

* Language understanding
* Conversation
* Reasoning
* Instruction following

### Runtime responsibilities

AMSX Runtime is planned to handle:

* Memory
* Emotion
* Personality
* Relationships
* Vision
* Speech
* Action
* Context building
* External tool integration

### Conceptual architecture

```text
Input
  ↓
Input Normalizer
  ↓
Intent / Think Router
  ↓
Memory Retrieval
  ↓
Personality / Emotion / Relationship State
  ↓
Context Builder
  ↓
AMSX-ATRI-TB04-LLM
  ↓
Response / Action Parser
  ├─ TTS
  ├─ Expression / Motion
  ├─ PC / Game Control
  └─ Memory Update
```

The initial goal is **not** to build a large microservices architecture.

AMSX Runtime will start as a relatively small system that works end-to-end, with components separated only where doing so provides a practical benefit. The architecture can then evolve as the project grows.

---

## Memory Architecture

AMSX-Project is exploring a memory architecture inspired by how human memory behaves.

The current concept separates memory into several categories.

### Working Memory

Information related to the current interaction and recent conversational context.

Examples include:

* Current conversation state
* Recent messages
* Temporary task context
* Information needed for ongoing reasoning

### Episodic Memory

Memories of events and experiences.

For example:

> “We played a game together yesterday.”

These memories represent experiences associated with a particular interaction, event, or period of time.

### Semantic Memory

Knowledge learned about people, objects, and the surrounding world.

For example:

> “This person likes this game.”

Unlike episodic memory, semantic memory represents reusable knowledge rather than a specific event.

### Memory retention and forgetting

The goal is not to permanently store every interaction.

AMSX is exploring mechanisms that determine whether information should be retained, reinforced, converted into long-term memory, or gradually forgotten based on factors such as:

* Importance
* Emotional significance
* Frequency
* Time elapsed

The exact memory model is still under research and may change as experiments progress.

---

## Planned Capabilities

| Capability                      | Status                          |
| ------------------------------- | ------------------------------- |
| Lightweight LLM                 | **In development**              |
| Japanese conversational ability | **In development**              |
| AMSX Runtime                    | **Planned / early development** |
| Working memory                  | **Planned**                     |
| Episodic memory                 | **Exploring**                   |
| Semantic memory                 | **Exploring**                   |
| Memory importance / forgetting  | **Exploring**                   |
| Emotion state                   | **Planned**                     |
| Personality state               | **Planned**                     |
| Relationship modeling           | **Planned**                     |
| Vision integration              | **Planned**                     |
| Speech-to-Text                  | **Planned**                     |
| Text-to-Speech                  | **Planned**                     |
| Real-time interaction           | **Planned**                     |
| Expression / motion control     | **Planned**                     |
| PC interaction                  | **Planned**                     |
| Game interaction                | **Planned**                     |
| AI VTuber integration           | **Long-term goal**              |

These statuses describe the current project direction and should not be interpreted as guarantees of future implementation.

---

## AI VTuber

One of the long-term applications being explored for AMSX is an **AI VTuber** built on top of AMSX Runtime.

The goal is to eventually connect:

* Real-time conversation
* Speech recognition
* Speech synthesis
* Facial expression and motion control
* Visual perception
* Game interaction
* Viewer and person memory
* Emotion state
* Persistent experiences

Instead of treating an AI VTuber as only an LLM connected to TTS, AMSX aims to explore a system where conversation, memory, relationships, perception, and actions influence one another over time.

This remains a long-term development direction rather than a completed system.

---

## Technology Stack

The currently planned technology stack is:

### Runtime Core

**Go**

Used for the main AMSX Runtime and system-level coordination.

### Machine Learning

**Python**

Used for model-related processing, machine learning experiments, datasets, evaluation, and related tooling.

### GUI

**TypeScript**

Planned for graphical interfaces and frontend components.

### GUI Controller

**Go + Wails + TypeScript**

Planned for desktop-oriented control interfaces.

### Inter-service communication

Initial communication between components is expected to use:

**HTTP + JSON**

More specialized protocols such as **gRPC** may be evaluated later where they provide a clear advantage.

The project intentionally avoids introducing additional infrastructure before it becomes necessary.

---

## Organization Repositories

This GitHub Organization is intended to host AMSX-related development such as:

* AMSX Runtime
* AMSX utilities and supporting tools
* Dataset processing code
* Evaluation and benchmark tools
* GUI Controller
* Experimental implementations
* Research prototypes

Not every part of AMSX-Project will necessarily be public.

In particular, **AMSX-ATRI-TB04-LLM itself is currently closed and is not intended for external distribution.**

Repository availability and licensing may therefore differ between individual components.

---

## Project Status

AMSX-Project is an **independent personal research and development project**.

The architecture, APIs, runtime design, memory system, model behavior, and repository structure may change significantly as experiments progress.

The project prioritizes:

1. Building small working prototypes
2. Evaluating them through actual use
3. Identifying limitations
4. Iterating on the architecture
5. Gradually integrating additional capabilities

The focus is practical experimentation rather than claiming that unfinished concepts are already solved.

---

## Developer

<a href="https://github.com/gramme-linkcom">
  <img src="https://avatars.githubusercontent.com/u/127509194?v=4" width="96" height="96" alt="ぐらむ GitHub Avatar">
</a>

### [ぐらむ](https://github.com/gramme-linkcom)

**GitHub:** [@gramme-linkcom](https://github.com/gramme-linkcom)
**Web handle:** `9ramme`
**Website:** [9ramme.net](https://9ramme.net)

AMSX-Project is currently developed as a personal research project.

---

## Notes

AMSX-Project includes both public and non-public components.

Public repositories in this Organization should not be interpreted as representing the complete internal implementation of AMSX.

Information about non-public model internals, technical provenance, training ancestry, and internal model composition is not provided unless explicitly published by the project.

---

<a id="日本語"></a>

# 日本語

## AMSXについて

**AMSX-Project** は、

> 軽量言語モデル **amsxシリーズ** の開発、および統合的な視覚・聴覚・操作能力、人間に似た記憶システムの構築

を目的として進めている、個人のAI研究・開発プロジェクトです。

単なる会話用LLMを作ることだけを目的とはしていません。

将来的には、複数の機能を **AMSX Runtime** によって統合し、継続的な対話・記憶・認識・行動を行えるAIエージェントを構築することを目指しています。

AMSXは現在も開発途中の実験的なプロジェクトです。以下に記載している機能には、開発中のものだけでなく、計画段階・研究段階のものも含まれています。

---

## 目標

AMSX-Projectでは、以下のような機能の統合を検討しています。

* 軽量言語モデル
* 長期記憶 / 短期記憶
* 視覚認識
* 聴覚認識
* Speech-to-Text
* Text-to-Speech
* 感情状態
* 人格
* 人間関係の認識
* PCやゲームなどの操作
* リアルタイム対話
* AI VTuberとしての利用

すべての機能をLLM内部だけで処理するのではなく、言語モデルとRuntimeの責務を分離する方針です。

---

## Current Model

### AMSX-ATRI-TB04-LLM

**AMSX-ATRI-TB04-LLM** は、現在開発しているAMSXシリーズの軽量言語モデルです。

現在は主に、

* 日本語での自然な会話
* 意図理解
* 会話履歴の理解
* 指示追従
* 会話品質

を重視して開発しています。

**AMSX-ATRI-TB04-LLM本体は現時点ではクローズドであり、外部配布を前提としていません。**

また、内部ベースモデル、technical provenance、学習上の由来など、公開していない内部情報については開示していません。

---

## AMSX Runtime

**AMSX Runtime** は、LLMとは責務を分離して設計する統合Runtimeです。

### LLM側

主に以下を担当します。

* 言語理解
* 会話
* 推論
* Instruction Following

### Runtime側

以下の機能を担当する予定です。

* Memory
* Emotion
* Personality
* Relationship
* Vision
* Speech
* Action
* Context Building
* 外部ツール連携

### 想定アーキテクチャ

```text
Input
  ↓
Input Normalizer
  ↓
Intent / Think Router
  ↓
Memory Retrieval
  ↓
Personality / Emotion / Relationship State
  ↓
Context Builder
  ↓
AMSX-ATRI-TB04-LLM
  ↓
Response / Action Parser
  ├─ TTS
  ├─ 表情 / モーション
  ├─ PC / Game操作
  └─ Memory Update
```

最初から大規模なmicroservices構成にすることは想定していません。

まずは小さく動作するRuntimeを構築し、必要性が明確になった機能から段階的に分離・拡張していく方針です。

---

## Memory Architecture

AMSXでは、人間の記憶に近い振る舞いを持つ記憶システムを研究しています。

現在想定している主な記憶分類は以下の通りです。

### Working Memory

現在の会話や直近の情報を保持します。

例:

* 現在の会話状態
* 直近のメッセージ
* 一時的なタスク情報
* 推論中に必要な情報

### Episodic Memory

出来事や経験に関する記憶です。

例:

> 「昨日一緒にゲームをした」

特定の出来事や時間に紐づいた経験として扱います。

### Semantic Memory

人物や世界について得た知識です。

例:

> 「この人はこのゲームが好き」

特定の出来事そのものではなく、再利用可能な知識として保持することを想定しています。

### 記憶と忘却

すべての情報を永久保存することは想定していません。

以下のような要素を利用して、

* 重要度
* 感情
* 頻度
* 時間経過

情報を長期記憶として残すか、強化するか、あるいは徐々に忘却するかを判断する仕組みを検討しています。

具体的なアルゴリズムについては現在も研究段階です。

---

## Planned Capabilities

| 機能                    | 現在の状態           |
| --------------------- | --------------- |
| 軽量LLM                 | **開発中**         |
| 日本語会話能力               | **開発中**         |
| AMSX Runtime          | **計画 / 初期開発段階** |
| Working Memory        | **計画中**         |
| Episodic Memory       | **研究中**         |
| Semantic Memory       | **研究中**         |
| 重要度・忘却システム            | **研究中**         |
| Emotion State         | **計画中**         |
| Personality State     | **計画中**         |
| Relationship Modeling | **計画中**         |
| Vision                | **計画中**         |
| Speech-to-Text        | **計画中**         |
| Text-to-Speech        | **計画中**         |
| リアルタイム対話              | **計画中**         |
| 表情 / モーション制御          | **計画中**         |
| PC操作                  | **計画中**         |
| Game操作                | **計画中**         |
| AI VTuber統合           | **長期目標**        |

ここに記載されている内容は現在の開発方針であり、将来的な実装を保証するものではありません。

---

## AI VTuber

AMSXの将来的な利用例のひとつとして、**AI VTuber** を想定しています。

Runtime上で、

* リアルタイム会話
* STT / TTS
* 表情やモーション制御
* 視覚認識
* ゲーム操作
* 視聴者や人物の記憶
* 感情状態
* 継続的な経験

などを統合することを目標としています。

単純にLLMとTTSを接続するだけではなく、会話・記憶・人間関係・認識・行動が時間とともに影響し合うシステムを研究していく予定です。

この部分は現時点では将来構想であり、完成済みのシステムではありません。

---

## Technology Stack

現在想定している技術構成です。

### Runtime Core

**Go**

AMSX Runtime本体や、システム全体の制御に使用する予定です。

### Machine Learning

**Python**

モデル関連処理、機械学習実験、Dataset、Evaluationなどに使用します。

### GUI

**TypeScript**

GUIおよびフロントエンド部分で使用する予定です。

### GUI Controller

**Go + Wails + TypeScript**

デスクトップ向けControllerとして利用する予定です。

### サービス間通信

初期段階では、

**HTTP + JSON**

を中心に構築する予定です。

必要になった場合には、将来的に **gRPC** などの利用も検討します。

必要性のない段階で複雑なインフラを導入せず、実際の開発状況に合わせて構成を拡張していく方針です。

---

## Organization Repositories

このGitHub Organizationでは今後、以下のようなAMSX関連コードを管理する予定です。

* AMSX Runtime
* AMSX関連ツール
* Dataset関連コード
* Evaluation / Benchmark関連コード
* GUI Controller
* 各種実験コード
* 研究用プロトタイプ

AMSX-Projectのすべてのコンポーネントが公開されるとは限りません。

特に、**AMSX-ATRI-TB04-LLM本体は現時点ではクローズドであり、外部配布を前提としていません。**

そのため、公開範囲やライセンスはリポジトリごとに異なる場合があります。

---

## Project Status

AMSX-Projectは、**個人で進めているAI研究・開発プロジェクト**です。

Runtimeの構成、API、Memory System、モデルの挙動、Repository構成などは、今後の研究や実験によって大きく変更される可能性があります。

開発では、

1. 小さく動作するものを作る
2. 実際に使用して評価する
3. 問題点を見つける
4. 設計を改善する
5. 段階的に機能を統合する

という流れを重視しています。

未完成の構想を完成済みの技術として扱うのではなく、実際に検証しながらAMSXを発展させていきます。

---

## Developer

<a href="https://github.com/gramme-linkcom">
  <img src="https://avatars.githubusercontent.com/u/127509194?v=4" width="96" height="96" alt="ぐらむ GitHub Avatar">
</a>

### [ぐらむ](https://github.com/gramme-linkcom)

**GitHub:** [@gramme-linkcom](https://github.com/gramme-linkcom)
**Web上のハンドル:** `9ramme`
**Webサイト:** [9ramme.net](https://9ramme.net)

AMSX-Projectは現在、個人研究プロジェクトとして開発しています。

---

## 注意事項

AMSX-Projectには、公開コンポーネントと非公開コンポーネントの両方が含まれます。

このOrganization上で公開されているRepositoryが、AMSXの内部実装全体を示しているとは限りません。

公開されていないモデル内部構造、technical provenance、学習上の由来、その他の内部情報については、プロジェクト側から明示的に公開されない限り開示しません。

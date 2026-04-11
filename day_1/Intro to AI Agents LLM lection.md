### Intro to AI Agents LLM

Video: https://www.youtube.com/live/C1OCgbONSAw?t=1080s
Materials: https://disk.yandex.ru/d/8nYIIjvHglHYYQ


Агент = рантайм система, внутри которой есть:
* model
* prompts
* tools
* memory
* planning instruments

<img width="1079" height="606" alt="image" src="https://github.com/user-attachments/assets/d431f5a0-9012-462f-864b-6d815c36fa2d" />

AI model = brain.
Model just generates textx.

## Prompts

**System** --- role, goals, limitations, style, decision making
**User** -- current task the assistant should do
**Assistant** --- messages of the assistant (its previous messages, tool calls, etc...)

## Tools
--- externel APIs and functions to interact with external

## Memory

**Short term** --- current dialogue, intermediate results agent's actions

**Long term** --- inter-session information: knowledge about user, historically done tasks, in-field knowledge

**Context** --- information the agent needs in the *current modent* --- it may CONSTRUCT from different parts!!!

## Evolution of Human-LLM Interaction

| Interaction | Description | Pattern example |
|---|---|---|
| **Prompting** | LLM output has no impact on program flow | `process_llm_output(llm_response)` |
| **Router** | LLM determines the basic control flow | `if llm_decision(): path_a() else: path_b()` |
| **Tool Calling** | LLM selects the function and arguments | `run_function(llm_chosen_tool, llm_chosen_args)` |
| **Multi-step Agent (Autonomous Agent)** | LLM output controls iterations and continuation of program execution | `while llm_should_continue(): execute_next_step()` |
| **Multi-Agent System** | One agent process can trigger another agent process | `if llm_trigger(): execute_agent()` |

This is a spectrum of how much control we give to the LLM --- from zero autonomy (prompting) to full autonomy (multi-agent).

## Guardrails
--- defend from prompt injection and making the behavious more deterministic

## Planning
Allows the agent not only respond to a query but also create  asequence of the actions and commit them.
**Reflection**
**Reasoning**
**Subgoal decomposition**

--- All of the above --- is inside the runtime

Think about the Agents --- as about the Operating System (Andrei karpaty).
LLM = kernel = orchestrates
External DB = disk
Context window = Operating memory
Tools = applications
--- very good udea!


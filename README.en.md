# StudentClaw

[中文](README.md)

> A human-powered execution platform with WeChat-native intake.  
> A graduate student stays in the loop, with `OpenClaw` or other agents used as on-demand reinforcement.

> Unofficial parody project; not affiliated with `OpenClaw`, `OpenAI`, `WeChat`, or related platforms. See the disclaimer below.

## Product Overview

`StudentClaw` is positioned for high-pressure, fragmented, time-sensitive work:  
requests arrive through WeChat, the system prioritizes them, a human execution layer carries the task forward, and external agents are pulled in only when structured generation or automation becomes the better fit.

Typical workloads include:

- research synthesis and information cleanup
- writing refinement and delivery follow-through
- deadline-driven emergency support
- tasks that still need human judgment and human fallback

## Launch Highlights

- **WeChat Native Interface**: tasks arrive through the channel people already use
- **Human Runtime**: the critical path stays human-driven and directly accountable
- **Agent Augmentation**: the operator can call `OpenClaw` or other agents on demand
- **Deadline-Aware Scheduling**: prioritization shifts with urgency, interruptions, and delivery windows
- **Low Monthly Cost**: in this repo’s fictional pricing model, the standard plan is `¥400 / month`

## Skills

| Skill | Description | Best For | Agent Escalation |
| --- | --- | --- | --- |
| `Deadline Rescue` | Prioritizes delivery under deadline pressure and pulls the result together fast. | Last-minute drafts, missing materials, final-round edits | Supported |
| `Seen-But-No-Reply` | Detects stalled threads and drags silent tasks back into motion. | Follow-ups, chasing replies, repeated pings | Optional |
| `Advisor Interrupt` | Handles sudden high-priority interruptions by reordering the queue. | Incoming urgent requests, broken schedules | Not needed |
| `Chat-to-Task` | Converts messy chat context into a concrete task list and deliverables. | Fragmented requirements, scattered context | Optional |
| `First-Draft First` | Produces a usable first pass, then tightens it through feedback loops. | Drafting, outlining, explanatory writing | Supported |
| `Human Saturation Fallback` | Switches to external agents when the human execution layer is overloaded. | Bulk rewriting, structured generation, repetitive work | Default on |

## Quick Start

1. Send the task, context, and delivery requirements through WeChat  
2. Let the routing layer decide priority and execution path  
3. `Student Runtime` handles execution, follow-through, and delivery  
4. Bring in external agents when automation becomes useful  
5. Return results and iterate until the task is closed

## Architecture

```text
                           +--------------------------------+
                           | Advisor Interrupts / Deadlines |
                           +---------------+----------------+
                                           |
                                           v
+-----------+     +----------------+     +----------------+     +----------------+
| Requester | --> | WeChat Gateway | --> |  Task Router   | --> | Priority Queue |
+-----------+     +----------------+     +----------------+     +--------+-------+
                                                                         |
                                                                         v
                                                              +-------------------+
                                                              |  Student Runtime  |
                                                              +----+---------+----+
                                                                   |         |
                                      +----------------------------+         +---------------------------+
                                      |                                                          |
                                      v                                                          v
                         +---------------------------+                             +------------------------+
                         | Research / Writing /      |                             |     Agent Adapter      |
                         | Delivery                  |                             +-----------+------------+
                         +-------------+-------------+                                         |
                                       |                                                       v
                                       v                                           +------------------------+
                         +---------------------------+                             | OpenClaw / Other Agents|
                         |      Result Delivery      |                             +-----------+------------+
                         +---------------------------+                                         |
                                                                                              v
                                                                                   +-------------------+
                                                                                   |  Student Runtime  |
                                                                                   +-------------------+
```

### Architecture Notes

| Module | Role |
| --- | --- |
| WeChat Gateway | Receives requests, context, and follow-up instructions |
| Task Router | Classifies work, assigns priority, and selects execution path |
| Priority Queue | Reorders work based on deadlines, urgency, and interruptions |
| Student Runtime | Human execution layer responsible for judgment, handling, and delivery |
| Agent Adapter | External capability layer for `OpenClaw` or other agents |
| Result Delivery | Sends results back, handles revision requests, and closes the loop |

## Comparison with OpenClaw

> This table is a parody positioning comparison. For official `OpenClaw` features, capabilities, and deployment details, refer to its official website and repository.

| Dimension | StudentClaw | OpenClaw |
| --- | --- | --- |
| Product category | Human-backed execution platform | Personal AI Assistant |
| Primary executor | Graduate student + caffeine | Local or self-hosted agent |
| Task entry | WeChat-first | Multi-channel messaging + local control plane |
| Control plane | Task routing, human judgment, and strategic disappearance | Local-first Gateway |
| Extensibility | Human tool use, agent fallback, and last-minute overtime | Tools, skills, routing, and multi-agent workflows |
| Cost structure | A fixed fictional `¥400 / month`, plus hidden sleep damage | Self-hosted software plus model / deployment costs |
| Failure mode | Seen-but-no-reply, advisor interruptions, deadline compression | Configuration, permission, runtime, and security-policy issues |
| Best fit | High-pressure tasks that need human fallback | Long-running personal AI assistant workflows |

## Plans & Service Level

| Item | Description |
| --- | --- |
| Standard Plan | `¥400 / month` |
| Token Policy | Theoretically unmetered, practically limited by how long a human can keep going |
| Response SLA | Fast on a good day, “I saw it” on a bad one |
| Escalation Policy | Brings in `OpenClaw` or other agents when the human layer is cooked |
| Autoscaling | Elastic capacity powered by caffeine, anxiety, and approaching deadlines |

## Use Cases

- delivery windows are short, but full automation is still risky
- someone needs to watch the process, details, and rework
- the request stream already lives in WeChat

## FAQ

### Is this a real product?

No.  
Please do not actually try to place an order.

### Does it actually support WeChat task dispatch?

Within the premise of the joke, yes.  
As a real shipped product feature, no.

### Why compare it with `OpenClaw`?

Because most people immediately want to know how this thing is supposed to differ from `OpenClaw`.

### Is this endorsing student exploitation?

No.  
The point is to expose how uncomfortable that logic already is, not endorse it.

## Disclaimer

`StudentClaw` is fundamentally an entertainment-oriented parody project.

- This repo does **not** provide a real subscription service
- This repo does **not** recruit students, graduate students, or labor of any kind
- This repo does **not** promise deliverables, capability, pricing guarantees, response times, or SLAs
- This repo does **not** endorse exploitative treatment of students, research assistants, or workers
- This repo has **no affiliation** with `OpenClaw`, `OpenAI`, `WeChat`, or any school, institution, organization, or platform
- Third-party names are used only for identification, commentary, parody, or context, and do not imply endorsement, partnership, agency, or official status

If you are looking for an actual product, this is not a purchase page.

## License

This repository is released under the `MIT` license; see `LICENSE` for details.

Please note:

- `MIT` applies only to the original text and code in this repository
- Third-party product names, trademarks, and brand assets remain the property of their respective owners
- If you create a derivative joke or parody, keeping the non-official disclaimer is strongly recommended

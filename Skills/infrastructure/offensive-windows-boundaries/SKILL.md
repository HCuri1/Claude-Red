---
name: offensive-windows-boundaries
description: "Windows security boundary taxonomy and attack surface enumeration: kernel/user boundary, sandbox boundaries (LPAC, AppContainer), COM/RPC boundaries, hypervisor boundary, trust level transitions. Use when planning privilege escalation paths, sandbox escapes, or understanding Windows security architecture. Triggers: Windows boundaries, security boundary, kernel user boundary, sandbox escape, AppContainer, LPAC, COM boundary, RPC boundary, hypervisor, Hyper-V, privilege escalation, trust level."
---

# Week 7: Defeating Windows Security Boundaries

## Overview

_created by AnotherOne from @Pwn3rzs Telegram channel_.

Week 6 taught you how mitigations work defensively.
You'll learn to bypass the OS security _policies and features_ that prevent your code from running, your processes from accessing protected resources, and your actions from being logged.
This is distinct from Week 8, which teaches you how to bypass _exploit mitigations_ (DEP, ASLR, CFG) once your code is already running.

> **Week 7 vs Week 8 - The Key Distinction**:
>
> - **Week 7** answers: _"Can my code execute at all?"_ - bypass AMSI, WDAC, ASR, AppContainers, integrity levels, PPL, ETW telemetry
> - **Week 8** answers: _"Can my exploit succeed?"_ - bypass DEP, ASLR, stack cookies, CFG/XFG, heap safe-unlinking

**This Week's Focus**:

- Offensive reconnaissance and mitigation fingerprinting
- AMSI bypass and script-based attack techniques
- Protected Process Light (PPL) exploitation
- Sandbox, integrity level, and AppContainer bypass
- WDAC and Attack Surface Reduction (ASR) bypass
- ETW manipulation and telemetry blinding
- Kernel driver interaction fundamentals (preparation for Week 11)

**Prerequisites**:

- Completed Week 6: Understanding Modern Windows Mitigations
- Week 5: Basic exploitation techniques (stack overflow, ROP, heap)
- Familiarity with WinDbg, x64dbg, and IDA/Ghidra
- C/C++, Python, and assembly knowledge

### Week 7 Deliverables

By the end of this week, you should have completed:

- [ ] **Recon Tool**: Built a mitigation fingerprinting tool
- [ ] **AMSI Bypass**: Implemented working AMSI bypass techniques
- [ ] **PPL Research**: Documented PPL bypass vectors
- [ ] **Sandbox Escape**: Bypassed AppContainer or integrity level restrictions
- [ ] **WDAC/ASR Bypass**: Demonstrated at least one WDAC and one ASR bypass
- [ ] **ETW Blinding**: Implemented ETW provider patching to suppress telemetry
- [ ] **Driver IOCTL Lab**: Loaded a test driver, sent an IOCTL, set a kernel breakpoint (Week 11 prep)

## Reference Index

This skill is organized as a lean overview plus detailed reference files, loaded on demand to keep context lean. Read the section you need:

- [Day 1: Offensive Reconnaissance & Mitigation Fingerprinting](references/day-1-offensive-reconnaissance-mitigation-fingerpr.md)
- [Day 2: AMSI Bypass and Script-Based Attack Techniques](references/day-2-amsi-bypass-and-script-based-attack-techniqu.md)
- [Day 3: PPL Bypass and Protected Process Exploitation](references/day-3-ppl-bypass-and-protected-process-exploitatio.md)
- [Day 4: Sandbox, Integrity Level, and AppContainer](references/day-4-sandbox-integrity-level-and-appcontainer.md)
- [Day 5: WDAC and Attack Surface Reduction (ASR) Bypass](references/day-5-wdac-and-attack-surface-reduction-asr-bypass.md)
- [Day 6: ETW Manipulation and Telemetry Blinding](references/day-6-etw-manipulation-and-telemetry-blinding.md)
- [Day 7: Full Chain Capstone - Breaking All Windows Security Boundaries](references/day-7-full-chain-capstone-breaking-all-windows-sec.md)
- [Appendix A: Redirection Guard](references/appendix-a-redirection-guard.md)
- [Appendix B: Win32 App Isolation](references/appendix-b-win32-app-isolation.md)
- [Week 7 Summary](references/week-7-summary.md)

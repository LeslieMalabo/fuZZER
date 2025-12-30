# LLM-Guided Fuzzing Prototype (WIP)

##  Overview
This project is a proof-of-concept pipeline designed to enhance traditional software fuzzing with Large Language Models (LLMs). By leveraging the reasoning capabilities of LLMs, this fuzzer generates structured, high-probability adversarial inputs to detect vulnerabilities in C binaries, such as Buffer Overflows and Injection flaws.

**Note:** This is an ongoing research project exploring the intersection of AI Safety and Cybersecurity.

## The Physics Perspective
As a physicist, I approach software security through the lens of **Dynamical Systems**. A program can be viewed as a system of states; "fuzzing" is the process of perturbing the system's input space to identify boundary conditions where the state-space transitions into an unstable regime (a crash). Using an LLM allows for a "guided" perturbation rather than a purely stochastic (random) approach.



## Features
- **Intelligent Seed Generation:** Uses LLM prompting to create context-aware test cases.
- **Vulnerability Tracking:** Automated detection of Buffer Overflows and character-based injections.
- **Python-C Integration:** A bridge between high-level logic and low-level binary execution.

##  How it Works
1. **Prompting:** The system prompts an LLM to generate potentially malicious strings based on a specific protocol or binary specification.
2. **Execution:** The Python core feeds these strings into the target binary.
3. **Monitoring:** The system monitors the process exit codes and memory state to identify crashes.
4. **Logging:** Vulnerabilities are logged with metadata for further analysis.

##  Project Structure
- `fuzzer_core.py`: The main Python engine managing the fuzzing logic.
- `targets/`: (WIP) Example C programs used as test subjects.
- `prompts/`: Templates for LLM input generation.

##  Future Roadmap
- [ ] Integrate OpenAI/Anthropic API for real-time seed generation.
- [ ] Implement Genetic Algorithms to evolve successful crash-inducing inputs.
- [ ] Add support for Grey-box fuzzing (code coverage analysis).

---
** Contact:**   www.linkedin.com/in/lesliemalabo
*Developed as part of my journey into AI Safety and Robustness.*

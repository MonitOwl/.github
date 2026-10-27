# MonitOwl

**Open-source runtime integrity for Linux and containers.**

**MonitOwl** builds tools to answer a simple question with hardware-backed evidence: *is the
software running on this machine the software we expect?* We measure what runs inside
containers, anchor those measurements in the TPM, and compare them against reference values
computed from the images they came from.

## What we work on

- **Runtime measurement** - observing executions and file accesses in the kernel with eBPF,
  without modifying the workloads being monitored
- **Remote attestation** - binding measurements to the TPM so that a verifier can trust them
  even when the host cannot be trusted
- **Reference values** - deriving the expected state of a workload from its container image,
  so that measurements can be appraised and not just collected

## Projects

| Project | Description |
| --- | --- |
| [**anchr**](https://github.com/MonitOwl/anchr) | eBPF-based integrity monitor with per-container measurement lists, Merkle tree aggregation and TPM PCR extension, plus a Go verifier for attestation |
| [**measr**](https://github.com/MonitOwl/measr) | Go library that measures the files of container images, producing the reference values runtime measurements are compared to |

## Origins

MonitOwl originated from research carried out within TORSEC, the cybersecurity research group of
Politecnico di Torino, by current and former members of the group who remain its authors.

## Get involved

Issues, questions and pull requests are welcome in each project's repository.

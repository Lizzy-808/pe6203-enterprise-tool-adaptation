# Original experiment evidence

The [consolidated evidence release](https://github.com/lingenxin3-sketch/pe6203-enterprise-tool-adaptation/releases/tag/project-evidence-20261029) contains byte-for-byte mirrors of the three original published archives. Their sizes and SHA-256 values match the source releases. This migration does not rerun experiments, change scores, or create new observations. Original archives retain historical filenames, paths, documentation, and model messages; current English project documentation is in this repository.

| Round | Run | Scored | Execution exceptions | Archive | SHA-256 |
|---|---|---:|---:|---|---|
| R1 | final-v1 | 162 | 4 | [Download ZIP](https://github.com/lingenxin3-sketch/pe6203-enterprise-tool-adaptation/releases/download/project-evidence-20261029/PE6203_Project4_Submission.zip) | `f0df5bdecbfc840cfd8b58555733ad5a4bfe99ad742fdedbd6b1f500dbc19fad` |
| R2 | repeat-r2-20261029 | 162 | 5 | [Download ZIP](https://github.com/lingenxin3-sketch/pe6203-enterprise-tool-adaptation/releases/download/project-evidence-20261029/repeat-r2-20261029-evidence.zip) | `9c2c963d0b8fa02267a87034a398672442a10424f22dae81a4298587f137fceb` |
| R3 | final-r3 | 162 | 5 | [Download ZIP](https://github.com/lingenxin3-sketch/pe6203-enterprise-tool-adaptation/releases/download/project-evidence-20261029/final-r3-evidence.zip) | `402d9a8005bc5848890fc60919dac4eef531ccf2a96a750e6b5c67f920f34c8c` |

All 486 scored observations and their failures are preserved. Only R1 + R3 form the 324-observation descriptive comparison over 18 distinct tasks. R2 remains separate because its actual resource lists differ. Fixed-seed repetitions do not establish statistical significance. The 65.1% reduction concerns update tokens; comparable three-stage recorded tokens increase 5.6%.

## Inspecting and verifying downloads

Download the archives and [SHA256SUMS.txt](../artifacts/evidence/SHA256SUMS.txt). In PowerShell, run `Get-FileHash -Algorithm SHA256 PATH_TO_ZIP` and compare the full value. Each ZIP also contains PACKAGE_MANIFEST.json with original per-file hashes. Do not rewrite paths or normalize JSON inside a frozen archive to make it match a source checkout.

The R1 ZIP includes the original main run and historical component/development material; the additional-round ZIPs include their own calls, trajectories, saved outputs, scores, failures, and closed logs. Model weights and unchanged duplicate benchmark resources are omitted and restored through the pinned reproduction process. The source tree contains summary metrics and reviews; original full run folders are release attachments.

## Source provenance

- R1: [original release](https://github.com/lingenxin3-sketch/pe6203-tool-harness-adaptation/releases/tag/v1.0.0); [original ZIP](https://github.com/lingenxin3-sketch/pe6203-tool-harness-adaptation/releases/download/v1.0.0/PE6203_Project4_Submission.zip).
- R2: [original release](https://github.com/lingenxin3-sketch/pe6203-tool-harness-adaptation/releases/tag/repeat-r2-20261029-evidence); [original ZIP](https://github.com/lingenxin3-sketch/pe6203-tool-harness-adaptation/releases/download/repeat-r2-20261029-evidence/repeat-r2-20261029-evidence.zip).
- R3: [original release](https://github.com/lingenxin3-sketch/pe6203-tool-harness-adaptation/releases/tag/final-r3-evidence); [original ZIP](https://github.com/lingenxin3-sketch/pe6203-tool-harness-adaptation/releases/download/final-r3-evidence/final-r3-evidence.zip).

The original repository remains a historical source. Historical commit links and receipt hashes intentionally refer to the original experiment. [Machine-readable provenance](../artifacts/evidence/releases.json) records original and mirror download addresses. [Migration verification](../artifacts/evidence/migration-verification.json) records anonymous readback of the destination archives when publication is complete.

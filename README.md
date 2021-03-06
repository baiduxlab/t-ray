# T-Ray: An Extensible Bug Detection Tool Targeting ARM TrustZone Applications

ARM TrustZone as an emerging technology has been increasingly adopted by consumer electronic devices, such as smartphones, smart homes, automotives, to protect sensitive data, like privacy information, biometrics and keys. Security researchers interested in finding bugs in Trusted Applications (TA) often suffer from onerous labor of reverse engineering in order to understand the TAs' logics and look for security property violations. Traditional bug finding tools don't have prior knowledge of the TrustZone environments, thus failing to accurately model the external dependencies of TA. Also, to the best of our knowledge, there are only a couple of security analysis tools specially designed for TrustZone. All of them are customized to a specific type of bug, or only works for a specific TA or TEE. To address this situation, we build an extensible bug detection tool T-Ray based on symbolic execution, which can automatically run analysis on TA binaries straight out of the box, and support most major TEEs, like OP-TEE, Samsung TEEGRIS, Trustonic, and Qualcomm QSEE. T-Ray is built as a framework that supports pluggable bug detectors. Besides built-in bug detectors that can detect common memory-safety bugs, the researchers can also implement their own bug detectors as plug-ins to fulfill their research goal.
 
Thanks to the constraint solving of the underlying symbolic executor, T-Ray can automatically generate concrete inputs as proof-of-concepts that can trigger bugs. Also, since most of the TA are stateful, they sometimes require a sequence of commands instead of a single command to reach certain "deep" logic. T-Ray is also designed to handle the statefulness of TA by running an iterative symbolic execution on each entry function.
 
We evaluated T-Ray with around 100 TAs from three TEEs, viz., OP-TEE, TEEGRIS, and Trustonic, and have found more than 30 bugs, including those running on real world Samsung devices.

## Status

Please stay tuned for further notifications of the release date.

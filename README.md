<div align="center">
    <img width="120" src="icon.svg" alt="logo">
  <h1 id="fleximq">fleximq Specification</h1>
</div>

This repository hosts the official specification for the fleximq protocol. fleximq is a flexible message queuing protocol designed for high performance and reliability.

## Protocol Overview

fleximq aims to provide a standardized way for applications to communicate asynchronously through messages. The detailed protocol specifications can be found in the respective documents within this repository.

> Note: All multi-byte numeric values in this protocol are encoded in network byte order (big-endian).
> All structured data (Header and Payload) uses MessagePack format for serialization.

### Key Design Goals

fleximq aims to provide a versatile, programming language-agnostic, and cross-platform messaging protocol. It supports various communication patterns like request/response, pub/sub, and notifications over multiple transport layers. The protocol is designed with a focus on efficiency and clear semantics, making it suitable for distributed systems, plugin architectures, and optimized for Internet of Things (IoT) applications. Compared to protocols like MQTT, fleximq offers a broader and more complex range of communication modes.

### Encoding Conventions

- **Numeric Values**: All multi-byte numeric values are encoded in network byte order (big-endian).
- **Structured Data**: Header and Payload sections use MessagePack format for serialization.
- **Strings**: All strings must be UTF-8 encoded.

* [Drafts](./draft/)
* RFCs are managed in a separate repository: [fleximq/rfcs](https://github.com/fleximq/rfcs)
* [Official Specifications](./official/)

## Contribution Process

We welcome contributions to the fleximq specification. The process is designed to be transparent and collaborative:

1.  **RFC (Request for Comments) Submission**:

    - Propose new features, changes, or improvements by submitting an RFC in the dedicated RFCs repository: [fleximq/rfcs](https://github.com/fleximq/rfcs).
    - The RFC should detail the motivation, design, and potential impact of the proposal.
    - Community discussion and feedback will take place on the RFC in its repository.

2.  **Draft Stage**:

    - If an RFC is accepted after review and discussion, its content will be used to create or update a draft specification in the `draft` directory of this (`spec`) repository.
    - At this stage, the proposal is considered a working draft and may undergo further refinements here.

3.  **Official Specification**:
    - Once a draft has been implemented by mainstream fleximq-compatible systems and has proven to be stable and beneficial, it can be promoted to an official specification.
    - Official specifications will be moved from the `draft` directory to the `official/` directory within this repository.

## Versioning

The fleximq protocol specification follows Semantic Versioning 2.0.0. Each official version of the specification will be clearly tagged and documented.

## How to Contribute

1.  For specification document changes (drafts, official specs):
    - Fork this (`spec`) repository.
    - Create a new branch for your changes.
    - Submit a Pull Request to this repository for review.
2.  For new proposals or discussions, please refer to the RFCs repository: [fleximq/rfcs](https://github.com/fleximq/rfcs).

## License

The fleximq specification is licensed under the [Unlicense](./LICENSE).

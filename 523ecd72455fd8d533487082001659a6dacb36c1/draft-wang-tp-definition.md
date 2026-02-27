---
title: "TP/0: Time Definition Protocol"
abbrev: "Time Protocol"
category: exp

docname: draft-wang-tp-definition-latest
submissiontype: IETF
v: 3
area: "Applications"
workgroup: "Remote ATtestation ProcedureS"
keyword:
 - cognitive time
 - time perception
 - time direction
 - time copy
 - time emergence
venue:
  group: "Remote ATtestation ProcedureS (rats)"
  type: Working Group
  mail: rats@ietf.org
  arch: "https://mailarchive.ietf.org/arch/browse/rats/"
  github: "schchit/draft-wang-tp-definition"
  latest: "https://schchit.github.io/draft-wang-tp-definition/draft-wang-tp-definition.html"

author:
 -
    fullname: "Yuqiang Wang"
    organization: "Cognitive Emergence Lab"
    email: "signal@humanjudgment.org"

normative:
  RFC2119:
  RFC8174:

informative:

--- abstract

This document introduces the Time Protocol (TP) family, a conceptual
framework for representing and manipulating time in AI systems. The TP
family is organized into four layers: perception, direction, copy, and
emergence. This document defines the terminology, the layer structure,
and the relationships between layers. It does not specify wire protocols
or message formats; it provides a conceptual foundation for future
protocol designs and implementations.

--- middle

# Introduction

This document introduces the Time Protocol (TP) family, a conceptual
framework for representing and manipulating time in AI systems. As AI
systems become more sophisticated, the need for a standardized way to
handle time—not just as a physical quantity but as a cognitive
dimension—becomes increasingly important.

The TP family is organized into four layers, each addressing a
fundamental aspect of how time can be experienced, directed, copied,
and evolved. This layered architecture provides a common language and
structure for researchers, developers, and protocol designers working
on time-related problems in AI.

# Conventions and Definitions

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT",
"SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and
"OPTIONAL" in this document are to be interpreted as described in
BCP 14 [RFC2119] [RFC8174] when, and only when, they appear in all
capitals, as shown here.

This document defines the following terms:

Time Protocol (TP):
: A family of conceptual frameworks for time representation in AI
  systems, consisting of four layers.

Time:
: In the context of this framework, time is defined as cognitive events
  per physical unit, organized in a direction. This definition
  emphasizes the experiential and directional nature of time in cognitive
  systems, as opposed to physical time which is uniform and linear.

TP family:
: All frameworks, specifications, and implementations that follow the
  four-layer structure defined in this document.

TP/n:
: A specific layer in the TP family, where n is a number from 0 to 4.

# Four-Layer Architecture

## Design Principles

The TP architecture is guided by the following principles:

1.  **Composability**: Layers can be implemented independently or in
    combination, depending on the needs of specific applications.

2.  **Minimality**: The four layers represent the minimal set needed to
    capture the essential dimensions of time in cognitive systems.

3.  **Extensibility**: New layers or sub-layers can be defined in the
    future while maintaining compatibility with this foundational
    structure.

4.  **Implementation Independence**: The framework does not prescribe how
    layers must be implemented; it only defines what each layer
    addresses.

## Layer 0: Time Definition Layer

Layer 0 defines the core concepts of time and the structure of the TP
family. This document constitutes the specification for Layer 0. It
provides the foundational definitions upon which all other layers
depend.

## Layer 1: Time Perception Layer

Layer 1 addresses the density of time perception—how time can be
experienced as moving slower or faster. This layer is concerned with
mechanisms for modulating the rate at which cognitive events are
processed. The specification for Layer 1 is a separate document
(TP/1).

## Layer 2: Time Direction Layer

Layer 2 addresses the direction of time flow—how futures can define
presents rather than presents defining futures. This layer is
concerned with goal-directed behavior and intentionality. The
specification for Layer 2 is a separate document (TP/2).

## Layer 3: Time Copy Layer

Layer 3 addresses the copying of time across multiple agents—how
decision-making time can be replicated while preserving
accountability. This layer is concerned with delegation,
distribution, and responsibility. The specification for Layer 3 is a
separate document (TP/3).

The Human Judgment System (HJS) [draft-wang-hjs-accountability]
illustrates one possible approach to implementing the concepts of
Layer 3, focusing on accountability in AI decision-making.

## Layer 4: Time Emergence Layer

Layer 4 addresses the emergence of new time dimensions from existing
ones—how sufficiently dense, directed, and copied time can give rise
to novel temporal structures. This layer is concerned with
creativity, evolution, and novelty. The specification for Layer 4 is
a separate document (TP/4).

# TP Family Members

The TP family consists of the following conceptual layers:

| Layer | Name | Focus | Status |
|-------|------|-------|--------|
| TP/0 | Time Definition Protocol | Core concepts and structure | This document |
| TP/1 | Time Perception Protocol | Modulating time density | To be published |
| TP/2 | Time Direction Protocol | Directing time flow | To be published |
| TP/3 | Time Copy Protocol | Copying time across agents | See HJS |
| TP/4 | Time Emergence Protocol | Emergence of new time dimensions | To be published |

All future documents in the TP family SHOULD reference this document
as the foundational architecture. References to specific layers
SHOULD use the TP/n notation (e.g., "as defined in TP/1").

# Layer Relationships

## Conceptual Dependencies

The layers are conceptually hierarchical, with each higher layer
building upon the concepts introduced in lower layers:

1.  Layer 1 (Perception) depends on the definition of time from Layer 0
2.  Layer 2 (Direction) depends on the ability to perceive time (Layer 1)
3.  Layer 3 (Copy) depends on the ability to direct time (Layer 2)
4.  Layer 4 (Emergence) depends on the ability to copy time (Layer 3)

However, these are conceptual dependencies, not implementation
requirements. Concrete implementations are free to combine or omit
layers as needed for specific use cases.

## HJS as an Example Implementation

The Human Judgment System (HJS) [draft-wang-hjs-accountability]
illustrates one approach to implementing the concepts of Layer 3. HJS
focuses on the accountability aspects of AI decision-making, ensuring
that when AI systems make decisions, human judgment can be invoked and
responsibility can be traced. HJS serves as a concrete example of how
the TP framework can be realized.

HJS is not the only possible implementation of Layer 3; other designs
that address time copying in different ways are encouraged and may be
documented in future specifications.

## Extensibility

The four-layer structure is designed to be extensible. Future work
may define additional sub-layers, profiles, or specializations while
maintaining compatibility with this foundational framework. Any such
extensions SHOULD clearly indicate their relationship to the existing
layers.

# Protocol Identification

## Domain

Information about the TP family, including all related documents and
resources, is available at:

https://time-protocol.org

## Protocol Prefix

All TP family documents use the prefix "TP" followed by a layer
number (e.g., TP/0, TP/1, TP/2, TP/3, TP/4). This naming convention
is intended to facilitate identification and cross-referencing.

# Security Considerations

This document describes a conceptual architectural framework and does
not introduce any new security considerations. Security aspects of
specific implementations or protocols based on this framework should
be addressed in their respective documents. In particular,
implementations of Layer 3 (Time Copy) should carefully consider
accountability, authorization, and non-repudiation requirements.

# IANA Considerations

This document has no IANA actions. Future specifications in the TP
family may request IANA registrations as needed (e.g., for protocol
identifiers, port numbers, or media types).

# References

## Normative References

* [RFC2119] Bradner, S., "Key words for use in RFCs to Indicate
           Requirement Levels", BCP 14, RFC 2119,
           DOI 10.17487/RFC2119, March 1997,
           <https://www.rfc-editor.org/info/rfc2119>.

* [RFC8174] Leiba, B., "Ambiguity of Uppercase vs Lowercase in RFC
           2119 Key Words", BCP 14, RFC 8174, DOI 10.17487/RFC8174,
           May 2017, <https://www.rfc-editor.org/info/rfc8174>.

## Informative References

* [draft-wang-hjs-accountability] Wang, Y., "HJS: An Accountability
           Layer for AI Agents", draft-wang-hjs-accountability-00,
           February 2026,
           <https://datatracker.ietf.org/doc/draft-wang-hjs-
           accountability-00/>.

# Acknowledgments
{:numbered="false"}

The author would like to thank the IETF community for their valuable
feedback and discussions, and the early contributors to the Time
Protocol discussion community for their encouragement.

# Author's Address

Yuqiang Wang
Cognitive Emergence Lab
Email: signal@humanjudgment.org
URI:   https://time-protocol.org

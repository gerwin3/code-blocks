# Code Blocks

Personal repository of common building blocks that I keep running into over and
over again.

TODO: Soon with reference implementations (maybe in multiple languagues).

### Service

A service is structure that starts a background thread or task, and accepts
inputs to process them asynchronously with respect to the caller.

### Service Manager

A service manager is a structure that manages multiple services instances of the
same service. For example: A service manager that manages services for each
multiple incoming data streams. Each service instance is an instantiation of a
service.

### Handler

A structure at the center of an application that accepts complex input structure
such as a request or command, and does what the request or command describes.

### Memoizer

A structure that wraps some resource-intensive function, but stores the results
with respects to each observed set of parameters and returns the cached result
if the input was already observed before.

### Identifier

An identifier is a structure that wraps some pointer-like data, but prevents the
caller from creating one themselves that is invalid.

[related to type modelling]
[related to Facade]

### Representation

A structure that can be easily mapped to a serialized counterpart such as a
file or a network packet.

### Connection

A structure that represents a connection to some external service. It will
typically provide the caller with functions to interact with the external
service, and represents a single "connection" to such an external service. Often
used in the context of databases, or internet APIs.

### Format Parser

A structure that takes binary or text input and turns it into a sturctured
format.

Note: Hard to do correctly since they often have the property that whilst
building the representation their internal state is incomplete and unstable.

[relate to representation]

### Format Writer

The opposite of a format parser.

Often unnecessary since they can be directly implemented as function on their
representation object.

[opposite of format parser]

### Buffered

A structure that provides and interface for adding (pushing) objects, but
internally buffers those items before forwarding it further. For example: Some
object that takes video frames as input, but instead of writing them to a file,
buffers them to a fixed (or configurable) amount, and only then writes them as a
batch.

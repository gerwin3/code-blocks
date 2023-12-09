# Code Strategies

Personal repository of common strategies that I keep running into over and over again.

Soon with reference implementations (maybe in multiple languagues).

### Service

A service is structure that starts a background thread or task, and accepts
inputs to process them asynchronously with respect to the caller.

### Service Manager

... TODO

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

A structure ...

Hard to do correctly since they often have the property that whilst building the
representation their internal state is incomplete and unstable.

[relate to representation]

### Format Writer

Often unnecessary since they can be directly implemented as function on their
representation object.

[opposite of format parser]

### Buffered

TODO: not sure

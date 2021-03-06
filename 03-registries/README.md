# Lab 03 - Context and registries lab

The `Context` is at the core of request processing in Ratpack applications.

It provides access to the HTTP Request and Response, allows flow control and has convenience methods for common handler operations.
More than that though, the Context is also a `Registry` of objects.  It provides access to these contextual objects via type-lookup
and allows arbitrary objects to be "pushed" into the context for use by downstream handlers.

## What to do

1. Register `DefaultBookService` as the implementation of `BookService` to the context so it is available to all downstream handlers.
1. Simply refactor the common logic of the two handlers in `Ratpack.groovy` into a new handler. And make the resulting object available
to the now downstream handlers using the context to do so.
1. Make sure `BookSpec` passes.

This time the hints are in the TODO within `Ratpack.groovy`

## This lab covers

* Registering objects in the registry
* Dynamically adding contextual objects
* Looking up contextual objects from the registry
* Injecting contextual objects into handlers

## Sign Posts

[`ratpack.handling.Context`](https://ratpack.io/manual/current/api/ratpack/handling/Context.html)

[`ratpack.registry.Registry`](https://ratpack.io/manual/current/api/ratpack/registry/Registry.html)
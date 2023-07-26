# Swagger source control

A framework for managing APIs from an external provider

Aims to fulfil the following needs

- Single source of truth
- Reduce dependency and overheads of comms (i.e. email chains)
- Provide a history of change
- Allow all parties to revolve a single artecfact(s)
- Provide in depth knowledege around API usage that might not be easily captured in swagger
- To aid engineers in consuming APIs

## Semantic versioning

All swagger specifications will be versioned using [semantic versioning](https://semver.org/)

### Definition

Given a version number **MAJOR.MINOR.PATCH**, increment the:

- **MAJOR** version when you make incompatible API changes
- **MINOR** version when you add functionality in a backward compatible manner
- **PATCH** version when you make backward compatible bug fixes

### Examples

- clarification of documentation, for example adding a **description** to a property or field which does not change the behaviour is a **PATCH** version change.
- Adding a new **optional** property to an operation is a **MINOR** version change
- Adding a new **mandatory** property to an operation is a **MAJOR** version change as it will break existing consumers of the API

## Rules of operation

- All updates to be provided via trunk, no branches required
- **PATCH** version changes can be made by either party (provider or consumers) and the changes advertised
- **MINOR** version changes can only be made by the provider of the API and changes advertised to consumers
- **MAJOR** version changes can only be made by agreement of provider and consumers as this has material impact on both delivery timelines.
- Where possible **MAJOR** version changes should be delivered in a non breaking way as a series of **MINOR** changes. This allows decoupling of dependencies and consumers to implement changes within a timeframe of their choosing, rather than to a fixed deadline.

One method for delivering **MAJOR** changes in a non breaking manner is via the Expand/Migrate/Contract pattern.

[Expand/Migrate/Contract aka Parallel change](https://martinfowler.com/bliki/ParallelChange.html)

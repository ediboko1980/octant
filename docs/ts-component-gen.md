# Generate Typescript components

This command converts components to typescript.

## Requirements

- prettier: `npm i -g prettier`

## Running

```sh
$ go run ./cmd/ts-component-gen/main.go -dest <directory>
```

## How does it work?

- Figure out what components exist. This process relies on convention, so components are labeled with an `+octant:component` tag in a doc comment.
- Extract type information by building up a new binary that contains reflect type information.
- Convert types to typescript
- Write typescript components to the supplied destination

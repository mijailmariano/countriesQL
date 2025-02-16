# GraphQL Introspection: Understanding Your Schema

## Overview
GraphQL introspection is a powerful feature that allows you to query a GraphQL schema for information about what queries it supports. This capability enables the creation of sophisticated tooling, documentation browsers, and IDE experiences.

## Core Concepts

### The `__schema` Field
The entry point for introspection queries is the `__schema` field on the root query type. This special field provides access to the schema's type system.

```graphql
query {
  __schema {
    types {
      name
      description
    }
  }
}

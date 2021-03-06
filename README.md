# benchmarker
[![Build Status](https://travis-ci.org/ideati-co/benchmarker.svg?branch=master)](https://travis-ci.org/ideati-co/benchmarker)

Various routines to put the latest web frameworks to the test.

## Motivation
Our platform receives JSON-RPC requests simultaneously from several clients. To make room for service growing, it's important to choose a performant and lightweight framework, highly optimized for:

- Database access: As per the last round (18) of [Techempower web framework Benchmarks](https://www.techempower.com/benchmarks/), 43 of the top 50 frameworks use PostgreSQL. There's also the possibility to use PostgreSQL as a NoSQL datastore with JSONB. See this [article](https://rollout.io/blog/unleash-the-power-of-storing-json-in-postgres/) for more information.

- JSON parsing: This is the most expensive operation for this kind of server due to the sheer number of conversions needed. Any gain in this area means a lot in the overall server performance.

- GraphQL: APIs implemented trough GraphQL permit more flexibility and granularity than RESTful alternatives.

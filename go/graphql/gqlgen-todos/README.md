# Todo GraphQL

Instructions for using this server:

It uses gqlgen to generate the GraphQL model and bindings. The GraphQL schema is
in `graph/schema.graphqls`; when the schema changes, rerun the tool to
regenerate the code:

		$ make generate

This may create some changes in `graph/schema.resolvers.go` - go over it
manually to make sure everything is OK (gqlgen moves functions it doesn't know
what to do with to the bottom of the file).

To run the server:

		$ make run/server

Then visit the printed link in a browser for the GraphQL playground.

In a separate window, run `scripts/manual-populate.sh` to submit some data to
the server. The data can then be explored from the playground.

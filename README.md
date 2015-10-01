# bosh-lite scripts

This is collection of small scripts that can be useful when debugging Cloud
Foundry deployments to bosh-lite. It uses the well known locations, passwords,
and credentials from the standard templates that exist in the cf-release
repository.

## Scripts

**`bosh-lite-admin`** - Target api.bosh-lite.com, login as admin, create org `o`
and space `s` and target them.

**`bosh-lite-db`** - Execute `psql` against the Cloud Controller Database as
`ccadmin`.

**`bosh-lite-diego-bulk`** - Run the Diego bulk apps query API with a batch size
of 1001.

**`bosh-lite-discover`** - Run the component discovery protocol over NATS. All
of the received responses are formatted for the user.  This is a ruby script
that requires the ruby NATS gem.

**`bosh-lite-nats`** - Connect to NATS and pretty print all of the received
messages. The user can provide a subject filter as a command line argument. If
the parameter is omitted, the subject defaults to `>` so all messages are
dumped.

**`bosh-lite-nats-connz`** - Get the contents of the NATS `/connz` endpoint.

**`bosh-lite-nats-subscriptionsz`** - Get the contents of the NATS
`/subscriptionsz` endpoint.

**`bosh-lite-nats-varz`** - Get the contents of the NATS `/varz` endpoint.

**`bosh-lite-router-stats`** - Get the contents of the Go Router's `/varz`
endpoint.

**`bosh-lite-routes`** - Get the contents of the Go Router's `/routes` endpoint.

**`bosh-lite-uaadb`** - Execute `psql` against the UAA Database as `uaaadmin`.

**`bosh-lite-varz`** - Execute the component discovery protocol and retrieve the
contents of the `/varz` endpoint of each responding component.

**`bosh-lite-varz-urls`** - Execute the component discovery protocol and print
all of the `/varz` URLs (including credentials) of the responding components.

**`pretty-json-get`** - Execute an HTTP GET against the specified URL and pretty
print the JSON response.

# Finance Benchmark Leaderboard

This repository is meant to assess agent candidates using the [Agentified Agent Assessment](https://docs.agentbeats.dev/) Benchmark for the finance benchmark in [here](https://agentbeats.dev/IraitzM/finance-benchmark).

In order to do that you would simply need to create a candidate purple agent according to what is described in the [agentbeats.dev](http://agentbeats.dev) platform and register it as such.

## How to get assessed

Well, make a branch/fork of the current repo and fill your data inside the `scenario.toml` file.

```toml
[[participants]]
agentbeats_id = ""
name = "purple_agent"
env = {}

[config]
# Query type from this options:
# - Quantitative Retrieval
# - Qualitative Retrieval
# - Numerical Reasoning
# - Complex Retrieval
# - Adjustments
# - Beat or Miss
# - Trends
# - Financial Modeling
# - Market Analysis
#
# Or all otherwise
type = ""

# For specific index in question type (comment for whole set)
query_index = ""
```

Use the `config` for particular question type assessment or simply set type to _all_ and comment que query index to assess against the whole public dataset.

![](images/purple.png)

For the participant information, once the purple agent is registered make sure to copy your agent id as this is what needs to be informed in `agentbeats_id`. Within `env`set any environment variable your agent might need considering there is an MCP server available directly from the green agent so you could use it as a variable informed with `http://green-agent:9020` as the exposed server.

There is an example under [the baseline branch](https://github.com/AITHU-AgentBeats/finance-benchmark-leaderboard/blob/baseline/scenario.toml) for some inspiration.

## Publish

Make sure to create a PR to the original repo so that results get published.
![](images/PR.png)
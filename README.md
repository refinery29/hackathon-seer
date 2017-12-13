# R29 Hackathon - Seer

An OpenStack test runner.

## Setup

1. Create GitHub hook to trigger a Jenkins job.
1. Create Jenkins job to checkout repo based on hook and run seer

## Execution

When the webhook is triggered:
1. Seer will read test configuration from a configuration file similar to a .travis.yml
1. A VM will be launched on OpenStack according to the configuration
1. Test scripts will be run the VM

## VM Creation

VMs could be preconfigured, or they could be built on demand based on configuration.

## Configuration file format

To dup or not to dup?

Although we could try to reuse existing .travis.yml files, I suspect that some fields may be nonsensical or wrong for an alternative system. This will create duplication if we are running the same tests will a similar execution environment, but seems sensible, and perhaps necessary to me.

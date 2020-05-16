Fluentd Benchmark Azure Environment with Terraform
===

## Prerequisites

* Terraform 0.12+
* Ansible 2.9+
* make

## Setup

 1. Prepare RSA public key and put it into `azure_key/id_rsa_azure.pub`.
 2. Prepare env.sh and fill `ARM_` prefixed environment variables with your credentials.
 3. Run `env.sh`
 4. Change directory to target environments(winevtlog_bench/in_tail_bench).
 5. Specify user-defined variables in `terraform.tfvars` which can be copied from `terraform.tfvars.sample` and fill them for each environment (winevtlog\_bench, in\_tail\_bench).

## Usage

### Windows EventLog Scenario Benchmark

```
$ cd winevtlog_bench
```

And then,

For creating instances:

```
$ make
```

Or, only creating instances:

```
$ make apply
```

And apply provisioning playbook:

```
% make provision
```

For destroying instances:

```
$ make clean
```

### in\_tail Scenario Benchmark

```
$ cd in_tail_bench
```

And then,

For creating instances:

```
$ make
```

Or, only creating instances:

```
$ make apply
```

And apply provisioning playbook:

```
% make provision
```

For destroying instances:

```
$ make clean
```

## License

[MIT](LICENSE).

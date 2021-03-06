
# Release Notes

- [Release Notes](#release-notes)
  - [Introduction](#introduction)
  - [Rosetta v0.1.1](#rosetta-v011)
    - [Features](#features)
  - [Rosetta v0.1.0](#rosetta-v010)
    - [Features](#features-1)
    - [Supported Platforms](#supported-platforms)
    - [Known Problems](#known-problems)
  - [Additional Information](#additional-information)

----

## Introduction
This document will maintain and continually update the release notes of each version of Rosetta. If you have questions or comments, please contact us via rosetta@latticex.foundation.

## Rosetta v0.1.1

### Features
1. Binary installation of TensorFlow is supported.

## Rosetta v0.1.0

### Features
1. Secure Multi-Party Computation (MPC) is supported, the underlying protocol is [SecureNN](https://eprint.iacr.org/2018/442.pdf). This is a $3$-party protocol, which is secure in the semi-honest model with honest majority.

2. Developers could transfer traditional TensorFlow codes into a privacy-preserving manner with minimal changes (import latticex.rosetta).

3. Static Pass is supported to replace TensorFlow native operations with MPC operations before the execution of the graph.

4. Dynamic Pass is supported to replace TensorFlow native operations with MPC operations when the graph is executed.

5. The following MPC operations and related gradients are supported.

    |  MPC OPs     |    MPC Gradient OPs    | 
    | --------------- | -------------- | 
    |MpcAdd |MpcAddGrad|
    |MpcSub |MpcSubGrad|
    |MpcMul |MpcMulGrad|
    |MpcDiv |MpcDivGrad|
    |MpcTrueDiv |MpcTrueDivGrad|
    |MpcRealDiv |MpcRealDivGrad|
    |MpcMatMul |MpcMatMulGrad|
    |MpcSigmoid |MpcSigmoidGrad|
    |MpcLog |MpcLogGrad|
    |MpcLog1p |MpcLog1pGrad|
    |MpcPow |MpcPowGrad|
    |MpcMax |MpcMaxGrad|
    |MpcMean |MpcMeanGrad|
    |MpcRelu |MpcReluGrad|
    |MpcEqual |-|
    |MpcLess |-|
    |MpcGreater |-|
    |MpcLessEqual |-|
    |MpcGreaterEqual |-|
    |MpcSaveV2 |-|
    |MpcApplyGradientDescentOp |-|

6. Support the combination of supported MPC operations to implement arbitrary models, such as: linear regression model, logistic regression model, etc.

7. Support for specifying the type (plaintext or ciphertext) of model to save;

8. Support for specifying where to save the model (Party0\Party1\Party2\all Parties);


### Supported Platforms
Rosetta has only been extensively tested on Intel X64 machines running Ubuntu 18.04.


### Known Problems
This section contains all known problems with the Rosetta system, listed by component. As new problems are discovered, they will be added to these sections.


## Additional Information
More details of Rosetta could be found in
the [documentation fold](doc/). If you have any questions or comments about Rosetta, please feel free to contact us via rosetta@latticex.foundation.

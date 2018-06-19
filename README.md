# axe-util

[![npm version](https://img.shields.io/npm/v/axe-util.svg)](https://www.npmjs.com/package/@axerunners/axe-util)
[![Build Status](https://travis-ci.org/axepay/axe-util.svg?branch=master)](https://travis-ci.org/axerunners/axe-util)
[![Dependency Status](https://david-dm.org/axepay/axe-util.svg)](https://david-dm.org/axerunners/axe-util)

**Utility functions for AXE hashes and targets**

## Usage

`npm install @axerunners/axe-util`

### Methods

#### `toHash(hex)`

Takes a hex string that contains a AXE hash as input, and returns a AXE-protocol-friendly little-endian Buffer. Throws an error if the hex string is not of length 64 (representing a 256-bit hash).

#### `compressTarget(target)`

Converts the difficulty target `target` to its compact representation (used in the "bits" field in block headers). `target` should be a `Buffer` (little-endian, the zeroes should be at the end). Returns a `number`.

#### `expandTarget(bits)`

Converts the compressed target integer `bits` to its target hash representation. Returns a `Buffer`.

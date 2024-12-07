# PHP in_array() Loose Comparison Pitfall with Array Keys

This repository demonstrates a common, yet subtle, bug in PHP related to the `in_array()` function and how it handles array keys with loose comparisons.  The example code showcases the problem and provides a corrected approach using `array_key_exists()` for strict key checking.  This is crucial when working with arrays where keys may be numeric strings or integers.

## Bug Description
The core issue lies in the default loose comparison behavior of `in_array()`. This means that if your array contains keys that are numerically equivalent but of different types (e.g., '1' (string) and 1 (integer)), `in_array()` may yield incorrect results if you're intending to perform a strict key comparison.

## Solution
The recommended solution is to avoid relying solely on `in_array()` for key checking and instead use `array_key_exists()` to ensure a strict comparison of keys.
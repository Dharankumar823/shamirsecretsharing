# shamirsecretsharing
Hashira Placements Assignment - Shamir Secret Sharing Reconstruction
 Overview

This repository contains the solution to the Hashira Placements Assignment, where the goal is to reconstruct the secret (constant term of a polynomial) from given roots (points) in JSON format using Lagrange Interpolation.

 Assignment Details

Input: JSON formatted test cases with points defined by their base and value.

Output: The reconstructed secret from the minimum required number of points k.

Languages Allowed: Any except Python.

Duration: 45 minutes.

Testing: The code reads JSON input, parses it, and reconstructs the secret using Shamir’s Secret Sharing principles.

 Implementation

Implemented entirely in Java.

Uses BigInteger to handle large values and arbitrary bases.

Applies Lagrange Interpolation to reconstruct the polynomial’s secret.

Parses JSON input using standard Java libraries for seamless integration with provided test cases.

 How to Run

Compile the Java file:

javac ShamirSecretSharingJSON.java


Run the program with the JSON input:

java ShamirSecretSharingJSON

 Sample Input (Testcase 1)
{
  "keys": {
    "n": 4,
    "k": 3
  },
  "1": {
    "base": "10",
    "value": "4"
  },
  "2": {
    "base": "2",
    "value": "111"
  },
  "3": {
    "base": "10",
    "value": "12"
  },
  "6": {
    "base": "4",
    "value": "213"
  }
}

 Output (Testcase 1)
3

 Sample Input (Testcase 2)
{
  "keys": {
    "n": 10,
    "k": 7
  },
  "1": { "base": "6", "value": "13444211440455345511" },
  "2": { "base": "15", "value": "aed7015a346d635" },
  "3": { "base": "15", "value": "6aeeb69631c227c" },
  "4": { "base": "16", "value": "e1b5e05623d881f" },
  "5": { "base": "8", "value": "316034514573652620673" },
  "6": { "base": "3", "value": "2122212201122002221120200210011020220200" },
  "7": { "base": "3", "value": "20120221122211000100210021102001201112121" },
  "8": { "base": "6", "value": "20220554335330240002224253" },
  "9": { "base": "12", "value": "45153788322a1255483" },
  "10": { "base": "7", "value": "1101613130313526312514143" }
}

 Output (Testcase 2)
-6290016743746469796


Note: The second output is negative because no modulus is applied, which is acceptable for this assignment.

 Notes

The solution has been tested manually against both sample inputs.

Handles arbitrary bases (binary, octal, decimal, hex, etc.) and large integer values using BigInteger.

The reconstructed secret uses the first k points for Lagrange interpolation, as per assignment requirements.

Submission

The code and README are pushed to this GitHub repository and linked in the official submission form.

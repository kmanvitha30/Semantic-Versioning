# Semantic Versioning

Semantic versioning (also referred as SemVer) is a versioning system with a 3-component number in the format of X.Y.Z, where :

  - X stands for a major version
  - Y stands for a minor version 
  - Z stands for a patch 
 
and X, Y and Z are non-negative integers.


![Alt text](https://github.com/kmanvitha30/Semantic-Versioning/blob/main/SemVer.png?raw=true "Optional Title")


#### Semantic Versioning Specifications 

  1. Software using Semantic Versioning MUST declare a public API. This API could be declared in the code itself or exist strictly in documentation. 
  2. Once a versioned package has been released, the contents of that version MUST NOT be modified. Any modifications MUST be released as a new version.
  3. Major version zero (0.y.z) is for initial development. Anything MAY change at any time. The public API is considered unstable.
  4. Patch version Z (x.y.Z | x > 0) MUST be incremented if only backwards compatible bug fixes are introduced. A bug fix is defined as an internal change that fixes incorrect behaviour.
  5. Minor version Y (x.Y.z | x > 0) MUST be incremented if new, backwards compatible functionality is introduced to the public API. It MUST be incremented if any public API functionality is marked as deprecated. It MAY be incremented if substantial new functionality or improvements are introduced within the private code. Patch version MUST be reset to 0 when minor version is incremented.
  6. Major version X (X.y.z | X > 0) MUST be incremented if any backwards incompatible changes are introduced to the public API. Patch and minor version MUST be reset to 0 when major version is incremented.
  7. A pre-release version indicates that the version is unstable and might not satisfy the intended compatibility requirements. Pre-release versions have a lower precedence than the associated normal version. Valid identifiers are in the set [A-Za-z0-9] and cannot be empty. Pre-release metadata is identified by appending a hyphen to the end of the SemVer sequence. Thus a pre-release for version 1.0.0 could be 1.0.0-alpha.1. Then if another build is needed, it would become 1.0.0-alpha.2, and so on.
  8. Build metadata MAY be denoted by appending a plus sign and a series of dot separated identifiers immediately following the patch or pre-release version. They are in the set [A-Za-z0-9] and cannot be empty. Examples: 1.0.0-alpha+001, 1.0.0+20130313144700, 1.0.0-beta+exp.sha.5114f85, 1.0.0+21AF26D3—-117B344092BD.
  9. Precedence refers to how versions are compared to each other when ordered.
    
       - Precedence MUST be calculated by separating the version into major, minor, patch and pre-release identifiers in that order (Build metadata does not figure into precedence).
       - Precedence is determined by the first difference when comparing each of these identifiers from left to right as follows: Major, minor, and patch versions are always compared numerically.Example: 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1.
       - When major, minor, and patch are equal, a pre-release version has lower precedence than a normal version:Example: 1.0.0-alpha < 1.0.0.
       - Precedence for two pre-release versions with the same major, minor, and patch version MUST be determined by comparing each dot separated identifier from left to right until a difference is found as follows:
                 1. Identifiers consisting of only digits are compared numerically.
                 2. Identifiers with letters or hyphens are compared lexically in ASCII sort order.
                 3. Numeric identifiers always have lower precedence than non-numeric identifiers.
                 4. A larger set of pre-release fields has a higher precedence than a smaller set, if all of the preceding identifiers are equal.
                 
    Example: 1.0.0-alpha < 1.0.0-alpha.1 < 1.0.0-alpha.beta < 1.0.0-beta < 1.0.0-beta.2 < 1.0.0-beta.11 < 1.0.0-rc.1 < 1.0.0.




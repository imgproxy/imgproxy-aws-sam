# Changelog

## [0.2.2] - 2024-09-30
### Changed
- Use HTTP/3 and HTTP/3 for CloudFront distributions.

## [0.2.1] - 2024-02-28
### Fixed
- Fixed CloudFront Origin Shield region selection.

## [0.2.0] - 2024-02-26
### Added
- Added `HowToConfigure` output.

### Changed
- If the `EnvironmentSystemsManagerParametersPath` parameter is not set, use `/${AWS::StackName}` as the default value.

### Removed
- Removed the `EnvironmentSecretARN` and `EnvironmentSecretVersionID` parameters.
- Removed the `aws-marketplace:MeterUsage` policy.

## [0.1.0] - 2024-02-07
### Added
- AWS SAM / CloudFormation template for deploying imgproxy to AWS Lambda

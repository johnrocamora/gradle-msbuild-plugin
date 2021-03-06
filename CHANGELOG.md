# gradle-msbuild-plugin changelog

## 2.16

### Fixed
* Registry keys are found when looking for msbuild versions. The issue is related to the JNA version used in other plugins.

## 2.15

### Fixed
* although the recommended use is to build through the solution, parsing the project file only now works (again, regression since 2.13)
* support for mono '-api' suffixed platform files

## 2.14

### Fixed
* solutionFile / projectFile now work also if relative (non-rooted)
 paths are provided, as it used to before 2.13


## 2.13

### Added
* support ToolsVersion upto `14.0`

### Changed
* ProjectFileParser now requires .Net Framework 4.5.2


## 2.12

### Changed
* `AssemblyInfoVersionPatcher` task now also supports setting AssemblyInformationalVersion


## 2.10

### Changed
* assemblyInfoPatcher is now automatically enabled if a version is provided
* removed input/output for msbuild, it wasn't working properly

### Added
* added dotnetAssemblyFile / dotnetDebugFile / dotnetArtifacts properties on msbuild projects


## 2.9

### Added
* Added support for assemblyInfoPatcher task
 * task will hook before msbuild, and patch AssemblyInfo.cs/fs with provided version number

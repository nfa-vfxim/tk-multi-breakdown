[![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/nfa-vfxim/tk-multi-breakdown?include_prereleases)](https://github.com/nfa-vfxim/tk-multi-breakdown) 
[![GitHub issues](https://img.shields.io/github/issues/nfa-vfxim/tk-multi-breakdown)](https://github.com/nfa-vfxim/tk-multi-breakdown/issues) 


# Scene Breakdown <img src="icon_256.png" alt="Icon" height="24"/>

Tools to see what in the scene is out of date.

## Requirements

| ShotGrid version | Core version | Engine version |
|------------------|--------------|----------------|
| -                | v0.14.48     | -              |

**Frameworks:**

| Name                      | Version | Minimum version |
|---------------------------|---------|-----------------|
| tk-framework-widget       | v1.x.x  |                 |
| tk-framework-shotgunutils | v5.x.x  | v5.2.1          |



## Configuration

### Hooks

| Name                      | Description                                                                                                                                                                                                                                                                                                             | Default value                            |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| `hook_scene_operations`   | Scan the scene for input files. Returns A list of nodes and file names. Each item in the list returned should be a dictionary containing a node, type and a path key. The node key should be a maya node name, the type key is a reference type and the path key is a full path to the file currently being referenced. | {self}/{engine_name}_scene_operations.py |
| `hook_get_version_number` | Perform a scan on disk to determine the highest version. Given a template and some fields, return the highest version number found on disk. The template key containing the version number is assumed to be named {version}.                                                                                            | {self}/get_version_number.py             |



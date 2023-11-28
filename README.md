# Application layer of the code-request Artifact

Definition of <https://github.com/pythoneda-artifact/code-request-application>, the application layer of "code request" artifacts.

## How to declare it in your flake

Check the latest tag of this repository and use it instead of the `[version]` placeholder below.

```nix
{
  description = "[..]";
  inputs = rec {
    [..]
    pythoneda-artifact-code-request-application = {
      [optional follows]
      url =
        "github:pythoneda-artifact-def/code-request-application/[version]";
    };
  };
  outputs = [..]
};
```

Should you use another PythonEDA modules, you might want to pin those also used by this project. The same applies to [nixpkgs](https://github.com/nixos/nixpkgs "nixpkgs") and [flake-utils](https://github.com/numtide/flake-utils "flake-utils").

Use the specific package depending on your system (one of `flake-utils.lib.defaultSystems`) and Python version:

- `#packages.[system].pythoneda-artifact-code-request-application-python38` 
- `#packages.[system].pythoneda-artifact-code-request-application-python39` 
- `#packages.[system].pythoneda-artifact-code-request-application-python310` 
- `#packages.[system].pythoneda-artifact-code-request-application-python311` 

## How to run pythoneda-artifact/code-request-application

``` sh
nix run 'https://github.com/pythoneda-artifact-def/code-request-application/[version]'
```

### Usage

``` sh
nix run https://github.com/pythoneda-artifact-def/code-request-application/[version] [-h|--help]
```
- `-h|--help`: Prints the usage.


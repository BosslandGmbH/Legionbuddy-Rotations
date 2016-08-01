# Legionbuddy Rotations

This repo contains the sources for the default rotations
shipped with [Legionbuddy](http://www.legionbuddy.com/).

## Using the rotations

When a new version of Legionbuddy is released it automatically contains
a snapshot of the master branch of this repository at the time of the release.
This means that a new release of Legionbuddy always will have the newest available version
of rotations.

If you still want to update manually, simply download a .zip from GitHub by pressing
the `Clone or download` -> `Download ZIP` buttons. Then delete the `Legionbuddy Rotations`
folder inside Rotations and extract the `Legionbuddy Rotations` folder from the .zip into
the Rotations directory. Assuming `C:\Path\to\Legionbuddy\Legionbuddy.exe` is a valid
path, the .zip should be extracted so that `C:\Path\to\Legionbuddy\Rotations\Legionbuddy Rotations\*.cs`
is valid.

## Developing the rotations

Since Legionbuddy compiles the rotations by itself there is no need to set up
a proper build environment. However, this is still beneficial if you are going to
be making changes to the rotations to make sure your changes still compile.

The repo includes at VS2015 solution which can be opened. To make the project compile
you must add references to Legionbuddy's `.exe` and `.dll` files. The project is already
set up to reference the correct assemblies in the `Dependencies` directory, so this
directory just needs to be created.

The easiest way to do that is with a symbolic link to your Legionbuddy installation. If
the path `C:\Path\to\Legionbuddy\Legionbuddy.exe` is valid, this is easily done by opening
a command prompt in the root of legionbuddy rotations (in the same folder as the `.sln` file)
and running the following command:
```
mklink /J Dependencies "C:\Path\to\Legionbuddy"
```
The rotations should now build successfully in VS2015.

## Contributing

See the [Contributing document](CONTRIBUTING.md) for guidelines for making contributions.

## Discuss

You can discuss Legionbuddy in our forums which can be found [here](https://thebuddyforum.com)

# sdl-cs

Automatically updated C# bindings for https://github.com/libsdl-org/SDL with native dynamic link libraries.

## How to use

### From source

1. Download and install [.NET 6](https://dotnet.microsoft.com/download).
2. Fork the repository using GitHub or clone the repository manually with submodules: `git clone --recurse-submodules https://github.com/bottlenoselabs/flecs-cs`.
3. Build the native library by running `library.sh`. To execute `.sh` scripts on Windows, use Git Bash which can be installed with Git itself: https://git-scm.com/download/win. The `library.sh` script requires that CMake is installed and in your path.
4. Import the MSBuild `SDL.props` file which is located in the root of this directory to your `.csproj` file to setup everything you need. See the [hello world sample](src/cs/samples/HelloWorld/HelloWorld.csproj) for an example of how to do this.
```xml
<!-- flecs: bindings + native library -->
<Import Project="$([System.IO.Path]::GetFullPath('path/to/SDL.props'))" />
```

#### Bindgen

If you wish to re-generate the bindings, run [`c2cs`](https://github.com/lithiumtoast/c2cs) from this directory.

## Developers: Documentation

For more information on how C# bindings work, see [`C2CS`](https://github.com/lithiumtoast/c2cs), the tool that generates the bindings for `SDL` and other C libraries.

To learn how to use `SDL`, check out the [Lazy Foo' Production](https://lazyfoo.net/tutorials/SDL).

## License

`SDL-cs` is licensed under the MIT License (`MIT`) - see the [LICENSE file](LICENSE) for details.

`SDL` itself is licensed under ZLib (`zlib`) - see https://github.com/libsdl-org/SDL/blob/main/LICENSE.txt for more details.

# `Spectre.Console.ImageSharp`

A .NET library that extends [Spectre.Console](https://github.com/spectreconsole/spectre.console)
with [ImageSharp](https://github.com/SixLabors/ImageSharp) superpowers, letting you render images
in the terminal with the `CanvasImage` widget.

```csharp
var image = new CanvasImage("cake.png");
image.MaxWidth(16);
AnsiConsole.Write(image);
```

Detailed instructions are located on the project website, https://spectreconsole.net/widgets/canvas-image

## Installing

```text
dotnet add package Spectre.Console.ImageSharp
```

## Building

```text
dotnet tool restore
dotnet make
```

### Six Labors license

This project depends on [ImageSharp](https://github.com/SixLabors/ImageSharp), which checks
for a [Six Labors license](https://sixlabors.com/pricing/) when it builds. Release builds,
including `dotnet make`, fail without one. The license must never be committed to the repository.

If you have a license, provide it in one of two ways:

* Set the `SixLaborsLicenseKey` environment variable to your license key.
* Save your license file as `sixlabors.lic` in the root of the repository.
  Git ignores this file, so it won't be committed.

Without a license you can still build and test in Debug, which only warns:

```text
dotnet build src/Spectre.Console.ImageSharp.slnx
dotnet test src/Spectre.Console.ImageSharp.slnx
```

Note that `dotnet make --configuration Debug` still fails without a license, because the build
script treats warnings as errors.

## License

Copyright © Patrik Svensson, Phil Scott, Nils Andresen, Cédric Luthi

`Spectre.Console.ImageSharp` is provided as-is under the MIT license. For more information see [LICENSE](LICENSE.md).

* SixLabors.ImageSharp, a library which `Spectre.Console.ImageSharp` relies upon, is licensed under Apache 2.0 when distributed as part of `Spectre.Console.ImageSharp`. The Six Labors Split License covers all other usage, see: https://github.com/SixLabors/ImageSharp/blob/master/LICENSE

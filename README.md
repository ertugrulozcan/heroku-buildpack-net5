# Heroku .NET 5 Buildpack

Forked by [jincod/dotnetcore-buildpack](https://github.com/jincod/dotnetcore-buildpack)

This is the [Heroku buildpack](https://devcenter.heroku.com/articles/buildpacks) for [ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/).

[![Actions Status](https://github.com/jincod/dotnetcore-buildpack/workflows/main/badge.svg)](https://github.com/jincod/dotnetcore-buildpack/actions)

The Buildpack supports C# and F# projects. It searchs through the repository's folders to locate a `Startup.*` or `Program.*` file. If found, the `.csproj` or `.fsproj` in the containing folder will be used in the `dotnet publish <project>` command.

If repository contains **multiple** Web Applications (multiple `Startup.*` or `Program.*`), `PROJECT_FILE` and `PROJECT_NAME` environment variables allow to choose project for publishing.
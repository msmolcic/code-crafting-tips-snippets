[![License](https://img.shields.io/badge/license-MIT-green)](https://github.com/YourGithubUsername/YourRepositoryName/blob/main/LICENSE)
[![Email](https://img.shields.io/badge/Email-gray?logo=gmail&style=flat-square)](mailto:mario.smolcic@rokolabs.com)
[![Stack Overflow](https://img.shields.io/badge/Stackoverflow-gray?logo=stackoverflow&style=flat-square)](https://stackoverflow.com/users/3284114/msmolcic)
[![Linkedin](https://img.shields.io/badge/-LinkedIn-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/msmolcic/)
[![Twitter Follow](https://img.shields.io/twitter/follow/MarioSmolcic?style=social)](https://twitter.com/MarioSmolcic)

# MediatR & FluentValidation Snippets

These code snippets allow developers to quickly scaffold various types of MediatR commands and queries, with or without result types and FluentValidation validation.

## How to Use:

To use these snippets, follow these steps:

1. Install the VSIX package containing the snippets.
2. Open a C# file in Visual Studio.
3. Type the desired shortcut (e.g., `mcmd`) and press `Tab` to expand the snippet.
4. Replace the placeholders (`$CommandName$`, `$ResultType$`, etc.) with the appropriate values for your use case.

## Snippets Overview

**MediatR Command**
- Shortcut: `mcmd`
- Description: Creates a new MediatR command.

```
public static class NewCommand
{
    public sealed record Command() : IRequest<Unit>;

    public sealed class CommandHandler : IRequestHandler<Command, Unit>
    {
        public CommandHandler()
        {
        }

        public async Task<Unit> Handle(Command request, CancellationToken cancellationToken)
        {
            return Unit.Value;
        }
    }
}
```

**MediatR Command With Result**
- Shortcut: `mcmdr`
- Description: Creates a new MediatR command with result.

```
public static class NewCommand
{
    public sealed record Command() : IRequest<Result>;

    public sealed class CommandHandler : IRequestHandler<Command, Result>
    {
        public CommandHandler()
        {
        }

        public async Task<Result> Handle(Command command, CancellationToken cancellationToken)
        {
        }
    }
}
```

**MediatR Command With Validation**
- Shortcut: `mcmdv`
- Description: Creates a new MediatR command with validation.

```
public static class NewCommand
{
    public sealed record Command() : IRequest<Unit>;

    public sealed class CommandValidator : AbstractValidator<Command>
    {
        public CommandValidator()
        {
        }
    }

    public sealed class CommandHandler : IRequestHandler<Command, Unit>
    {
        public CommandHandler()
        {
        }

        public async Task<Unit> Handle(Command request, CancellationToken cancellationToken)
        {
            return Unit.Value;
        }
    }
}
```

**MediatR Command With Validation And Result**
- Shortcut: `mcmdvr`
- Description: Creates a new MediatR command with validation and result.

```
public static class NewCommand
{
    public sealed record Command() : IRequest<Result>;

    public sealed class CommandValidator : AbstractValidator<Command>
    {
        public CommandValidator()
        {
        }
    }

    public sealed class CommandHandler : IRequestHandler<Command, Result>
    {
        public CommandHandler()
        {
        }

        public async Task<Result> Handle(Command command, CancellationToken cancellationToken)
        {
        }
    }
}
```

**MediatR Query**
- Shortcut: `mqry`
- Description: Creates a new MediatR query.

```
public static class NewQuery
{
    public sealed record Query() : IRequest<Result>;

    public sealed class QueryHandler : IRequestHandler<Query, Result>
    {
        public QueryHandler()
        {
        }

        public async Task<Result> Handle(Query query, CancellationToken cancellationToken)
        {
        }
    }
}
```

**MediatR Query With Validation**
- Shortcut: `mqryv`
- Description: Creates a new MediatR command with result.

```
public static class NewQuery
{
    public sealed record Query() : IRequest<Result>;

    public sealed class QueryValidator : AbstractValidator<Query>
    {
        public QueryValidator()
        {
        }
    }

    public sealed class QueryHandler : IRequestHandler<Query, Result>
    {
        public QueryHandler()
        {
        }

        public async Task<Result> Handle(Query query, CancellationToken cancellationToken)
        {
        }
    }
}
```

## Requirements:

- [MediatR](https://www.nuget.org/packages/MediatR/) NuGet package.
- [FluentValidation](https://www.nuget.org/packages/FluentValidation/) NuGet package.

## About

Created by **Mario Smolcic**. For more developer tips and tutorials, visit [www.codecrafting.tips](http://www.codecrafting.tips).
# Pasmen

Pasmen is a console-based password manager written in C#/.NET Framework 4.7.2.

## Overview

- Stores password entries as name/value pairs
- Loads and saves a single database file with the `.pasmen` extension
- Detects a premium mode when a `.lic` file is present next to the executable

## Storage modes

### Free mode

- Uses `XmlDataSerializer`
- Uses `FreeEncryptionHandler`
- These handlers are currently placeholders in the codebase

### Premium mode

- Uses `JsonDataSerializer`
- Uses the premium encryption handler
- Encrypts data with the configured database password

## Usage

1. Start the application
2. Enter or select the database name
3. Enter the database password when prompted
4. Manage entries from the console menu:
   - Add a password
   - Edit or remove an entry
   - Clear the list
   - Save or reload the database

## Build

```bash
dotnet build Pasmen.sln
```

## Project structure

- `Pasmen/Client.cs` - console entry point
- `Pasmen/Common` - menu handling, UI helpers, and dictionary extensions
- `Pasmen/Data` - configuration, serializers, encryption handlers, and factories
- `Pasmen/Exceptions` - domain-specific exceptions
- `files/` - sample database and license files

## Sample data

The `files/` directory contains example assets, including a sample database and a premium license file.

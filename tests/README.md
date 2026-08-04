# Generated test suites

These test suites are generated from the authoritative `dripsharp/dripsharp` target contract. Do not apply durable manual fixes in a generated product repository.

From a clean brine product-repository checkout:

### `DripSharp.Brine.Tests`

```sh
dotnet restore tests/DripSharp.Brine.Tests/DripSharp.Brine.Tests.csproj
dotnet build tests/DripSharp.Brine.Tests/DripSharp.Brine.Tests.csproj --configuration Release --no-restore --no-incremental -warnaserror
dotnet test tests/DripSharp.Brine.Tests/DripSharp.Brine.Tests.csproj --configuration Release --no-restore --no-build
```

The project references only paths within this checkout. Its test host permits major-version roll-forward so a later .NET runtime can exercise an earlier-targeted product family. `SHA256SUMS` inventories every generated test file except the inventory itself.
Each declared strategy records whether its output is shipped or validation-only; validation-only project paths are excluded from publication by the target contract.

The upstream-derived Brine suite exposes independently named xUnit rows from the pinned LanguageSnippet, Pkl.Core, and pkl-parser contracts. See [`TEST-BOUNDARY.md`](TEST-BOUNDARY.md) for the mechanical/authored/vendored boundary and `TEST-PROVENANCE.tsv` for exact hashes.

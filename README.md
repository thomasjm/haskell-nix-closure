# haskell-nix-closure

This is a repro for an issue where the Haskell.nix build infrastructure includes the full GCC compiler in the runtime dependency closure of a built executable.

To build and see the closure, type

```bash
nix-store -qR $(nix-build . -A haskell-nix-closure.components.exes.haskell-nix-closure-exe --no-out-link)
```

nix-portable nix repl -f '<nixpkgs>'
:lf .
outputs.packages.x86_64-linux.nix-portable

nix-portable nix store delete --ignore-liveness ./result
nix-portable nix store gc
nix-portable nix build -L .#packages.x86_64-linux.nix-portable

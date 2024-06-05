# 🌿 Labyrinth

Discover Labyrinth, a serene color scheme inspired by hidden pathways and mossy landscapes. Let its gentle tones guide your creativity with calm elegance.

Labyrinth provides four distinct variants with varying levels of contrast and color vibrancy to suit your preferences:

 - **Gloom**: The most contrasty variant, perfect for those who prefer sharp distinctions and vibrant colors.
 - **Dusk**: A balanced variant, offering a comfortable middle ground with moderate contrast and vibrancy.
 - **Shade**: A softer variant with reduced contrast, ideal for a more subdued and relaxed visual experience.
 - **Mist**: The least contrasty variant, featuring the most gentle and subtle tones for a calm and unobtrusive interface.

Whether you're coding, designing, or simply exploring new aesthetics, Labyrinth adapts to your needs with its harmonious palette.

## Usage

> [!IMPORTANT]
> Theme is utilizing the `FZF_DEFAULT_OPTS` environment variable so your specific example may be different depending if you already use that variable.

**POSIX shells**

You need to export `FZF_DEFAULT_OPTS` variable with the `--colors` options as value as provided in `dist/*.sh` files.

Either simply source selected variant's `.sh` file or copy the contents to your profile file, e.g. `.profile` for bash or `.zshrc` for zsh

**Fish**

Similiar to above you need to set the `FZF_DEFAULT_OPTS` variable.

Copy the contents of `dist/*.fish` to `~/.config/fish/config.fish` or create a
custom function:

```fish
# ~/.config/fish/functions/fzf.fish
function fzf --wraps="fzf"
    # Paste contents of preferred variant here

    command fzf
end
```

**PowerShell**

Copy the contents of `dist/.*ps1` to `~/Documents/PowerShell/Microsoft.PowerShell_profile.ps1`.

**Nix Home Manager**

```nix
let
  theme = pkgs.fetchFromGitHub {
    owner = "dgabka";
    repo = "labyrinth-fzf";
    rev = "9fe783b027f8c35c04b686ff4cb1a9777e5df73d";
    sha256 = "sha256-/HJ8XEHoqxfOHmqmCkIuU7KCBqlzsj7reTjo3Fo7UGk=";
  };
in {
  programs.fzf.colors = import "${theme}/dist/labyrinth-dusk.nix"
}
```

## Gallery

**Labyrinth Gloom**

![fzf with Labyrinth Gloom](assets/gloom.png)

**Labyrinth Dusk**

![fzf with Labyrinth Dusk](assets/dusk.png)

**Labyrinth Shade**

![fzf with Labyrinth Shade](assets/shade.png)

**Labyrinth Mist**

![fzf with Labyrinth Mist](assets/mist.png)

### Credits

Thanks to the [Rosé Pine](https://github.com/rose-pine) creators!
A special thanks to [Rosé Pine for fzf](https://github.com/rose-pine/fzf) which this theme is based on.

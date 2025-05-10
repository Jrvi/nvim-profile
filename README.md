# Neovim konfiguraatio – Juho Järvi

Tämä on henkilökohtainen Neovim-konfiguraatio, joka käyttää [lazy.nvim](https://github.com/folke/lazy.nvim) -paketinhallintaa. Tässä dokumentissa on yhteenveto käytetyistä lisäosista ja miten ne toimivat.

## Käyttöönotto

1. Varmista, että `git`, `neovim` ja `nvim`-kansio on paikoillaan:
2. Käynnistä `nvim` – `lazy.nvim` bootstrappaa itsensä automaattisesti.
3. Käytä `:Lazy`-komentoa hallinnoidaksesi lisäosia.

## Lisäosat ja asetukset

### 🎨 catppuccin

**Teema Neovimille**

- Määritelty tiedostossa: `lua/plugins/catppuccin.lua`
- Vaihtaa väriteeman Catppuccin Macchiato-tyyliin.
- Vinkki: voit muuttaa tyyliä muuttamalla `flavour`-arvoa.

### 🌳 treesitter

**Syntaksin korostus ja rakenneanalyysi**

- Tiedosto: `lua/plugins/treesitter.lua`
- Asentaa automaattisesti kielikohtaiset parserit.
- `:TSInstallInfo` näyttää mitkä kielet on asennettu.

### 🔍 telescope

**Fuzzy finder -työkalu**

- Tiedosto: `lua/plugins/telescope.lua`
- Komennot:
  - `:Telescope find_files`
  - `:Telescope live_grep`
  - `<leader>ff`, `<leader>fg`, jne. käytettävissä jos määritelty keymapit.

### 📁 neo-tree

**Tiedostoselain**

- Tiedosto: `lua/plugins/neo-tree.lua`
- Korvaa vanhan `nvim-tree`-pluginin.
- Avauskomento: `<leader>e` (jos määritelty keymappeihin)

### 📊 lualine

**Tilariviplugin**

- Tiedosto: `lua/plugins/lualine.lua`
- Tyylikäs ja informatiivinen tilarivi pohjalla.

### 🔮 completions

**Automaattitäydennys**

- Tiedosto: `lua/plugins/completions.lua`
- Käyttää `nvim-cmp`-lisäosaa ja muita lähteitä kuten LSP, buffer, path.
- TAB ja SHIFT+TAB navigoivat ehdotuksissa (jos määritelty).

### 🧠 LSP konfiguraatio

**Kielipalvelinasetukset**

- Tiedosto: `lua/plugins/lsp.config.lua`
- Käyttää `mason`, `lspconfig` ja `cmp-nvim-lsp`.
- `:LspInfo` näyttää aktiiviset palvelimet.

### 🧹 none-ls

**Formatterit ja linterit**

- Tiedosto: `lua/plugins/none-ls.lua`
- Integroi työkaluja kuten `prettier`, `eslint`, jne.
- Toimii osana LSP:tä.

---

## Muita tiedostoja

- `lua/vim-options.lua`: yleiset asetukset kuten tabit, rivinumerot, jne.
- `lazy-lock.json`: versiolukitus lisäosille.

---

## Yhteystiedot

Konfiguraation tekijä: **Juho Järvi**  
Päivitä tarvittaessa omaan käyttöön sopivaksi.

# Changelog — tkz-tab

All notable changes to `tkz-tab` are listed here, most recent first.

## [2.13c] — 2026/10/19

### Changed
- Keys use `pgfkeys` instead of `xkeyval`: same names, same default values,
  defaults reset at each call as before (`\tkzTabSetup` included).
- `\tkzTabVar`: the 31 symbols are keys `/tkztab/var/<symbol>` (the long
  cascade of `\ifthenelse` is removed); a new symbol can be added with
  `\pgfkeys{/tkztab/var/<symbol>/.code={...}}`.
- `\tkzTabLine`: the symbols `z`, `t`, `d`, `h` are keys
  `/tkztab/line/odd/<s>` and `/tkztab/line/even/<s>`.
- Useless `\makeatletter`/`\makeatother` removed (`\tkzTabLine`,
  `\tkzDrawArrow`).
- `xkeyval` is no longer loaded: a document that used it without loading it
  must now load it.

### Fixed
- Option `help` of `\tkzTabInit`, `\tkzTabLine` and `\tkzTabVar`: the labels
  of the nodes failed (`Undefined control sequence`) with the TikZ library
  `babel` when the picture is inside an environment that reads its content
  again, such as `tkzexample`.

## [2.12c] — 2020/04/29
- CTAN version.

## 2.11
- Correction of a bug in the macro `\tkzTabSetup`.

## 2.1
- Correction of bugs and examples added in the documentation.

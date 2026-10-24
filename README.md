# hash-cracker

Многопоточный подборщик хешей на Rust (MD5/SHA1/SHA256/bcrypt/Argon2) по словарям и маскам.

## Возможности (план)

- атаки: словарная, маска, полный перебор;
- алгоритмы: MD5, SHA-1, SHA-256, bcrypt, Argon2;
- многопоточность через rayon (все ядра);
- прогресс-бар и скорость в хешах/сек;
- поддержка salt и форматов типа `$2b$...`;
- экспорт найденных паролей в файл.

## Стек

- Язык: Rust
- Планируемые библиотеки: `clap`, `rayon`, `md-5`, `sha1`, `sha2`, `bcrypt`, `argon2`, `indicatif`

## Сборка и запуск

```bash
cargo build --release
cargo run -- -m sha256 -w wordlist.txt hashes.txt
```

## Лицензия

MIT

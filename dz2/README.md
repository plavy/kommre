# Potpisivanje

## Hash datoteke
```shell
openssl dgst -sha256 0036522334.imn > sha_hash
```

## Privatni ključ
```shell
openssl genrsa -out private_key.pem 2048
```

## Javni ključ
```
openssl rsa -in private_key.pem -outform PEM -pubout -out 0036522334.pem
```

## Digitalni potpis
```shell
openssl rsautl -sign -inkey private_key.pem -keyform PEM -in sha_hash > 0036522334.sig
```
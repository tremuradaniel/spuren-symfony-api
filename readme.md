symfony server:start

errors 


php bin/console lexik:jwt:generate-keypair
error:02001003:system library:fopen:No such process

mkdir -p config/jwt
openssl genpkey -out config/jwt/private.pem -aes256 -algorithm rsa -pkeyopt rsa_keygen_bits:4096
openssl pkey -in config/jwt/private.pem -out config/jwt/public.pem -pubout
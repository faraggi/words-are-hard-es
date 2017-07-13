# Palabras dificiles: Definiendo terminos comunes de Ethereum


Traducción de: "[Words are hard: Defining Common Terms in the Ethereum / Crypto Space](https://www.reddit.com/r/ethereum/comments/6kvp87/words_are_hard_defining_common_terms_in_the/)"
por [insomniasexx](reddit.com/u/insomniasexx)

## Billetera

* La interfaz / cliente / wrapper contenedor que usas para getionar tu(s) cuenta(s).
* Ejemplo: MyEtherWallet.com, tu billetera Ledger, un contrato de billetera Multisig.

## Cuenta (Account)

* Un par de llaves públicas/privadas que "contienen" tus fondos.
* En realidad, tus fondos están contenidos en la blockchain, no en la billetera o en la cuenta.
* Tal como tu cuenta Reddit tiene un nombre de `usuario (público)` y una `clave (privada)`, tu cuenta Ethereum es igual. Para más seguridad, puedes usar un password para encriptar tu llave privada que puede resultar en un `usario (púbilco)` y una `clave (privada)` y una `clave` para `esa clave (privado + seguro)`. Ver la sección de Keystore File.

## Address ("Llave Pública")

* Usas esto para enviar fondos a una cuenta.
* Algunas veces se le refiere como "llave pública".
* Una cadena de caracteres de '0x' + 40 caracteres hexadecimales.
* En Ethereum, las address comienzan con 0x.
* Ejemplo: 0x06A85356DCb5b307096726FB86A78c59D38e08ee

## LLave Pública

* En la critografía, hay un par de llaves: la pública y la privada.
* Puedes derivar la llave pública de la llave privada, pero no lo contrario.
* (Avanzado) En Ethereum, la dirección "actúa" como una llave pública, pero en realidad no lo és.
* (Avanzado) En Etherum, la llave pública es derivada de la llave privada y es una cadena de 128 caracteres hexadecimales. Luego puedes tomar el hash "SHA3" (Keccak-256) de esto (64 caracteres), tomar los ultimos 50 caracteres y prefijar con '0x', y obtendrás la address de 42 caracteres.

## Llave Privada

* Usa esto para enviar fondos desde una cuenta.
* La mitad secreta de tu combinación Adress/llave pública.
* Una cadena de 64 caracteres hexadecimales.
* (Casi) toda cadena de 64 caracteres hexadecimales es una llave privad.
* Si escribieras tu llave privada de dos maneras diferentes, tendrás acceso a otra billetera. Nunca escribas tu llave privad a mano.
* Estos son los caracteres que necesitas para enviar desde tu cuenta. Sin ello, no puedes acceder a los fondos. A pesar de que, no necesitas guardarla bruta sin encriptar en este formato. Puedes guardar versiones mas elaboradas de ella (ej. el archivo Keystore / una frase mnemotécnica).
* Ejemplo: afdfd9c3d2095ef696594f6cedcae59e72dcd697e2a7521b1578140422a4f890

Archivo Keystore
* Version criptada de tu llave privada en formato JSON (aunque no tiene extensión JSON)
* una versión elaborada de tu llave privada que está protegida por una clave que has elegido tu.
* Cuando se combina con la clave, crea la llave privada.
* Más segura que las llaves privadas ya que necesitas la clave.
* El nombre del archivo en general tiene el formato `UTC + -- + FECHA_CREADA + -- + TU_ADDRESS_SIN_0x`
* Ejemplo de nombre de archivo: `UTC--2017-07-02T20-33-09.177Z--06a85356dcb5b307096726fb86a78c59d38e08ee`
* Ejemplo de contenidos: `{"version":3,"id":"aa811d53-fe9a-44a2-bd1c-e737007b5591","address":"06a85356dcb5b307096726fb86a78c59d38e08ee","Crypto":{"ciphertext":"f5a7cc8d4b8cf93510b0d0d057f3a52ac79fd48e619e0638c4ffd978ca180248","cipherparams":{"iv":"975ab00192e2dd74170e91ca59c0b0bd"},"cipher":"aes-128-ctr","kdf":"scrypt","kdfparams":{"dklen":32,"salt":"0210f0d0b99e440dfbceb36373304638bac093a367ee7da6411cd165f7aa907a","n":1024,"r":8,"p":1},"mac":"8197a747a3855a10546a2ff939c36470daed78e393b670efa0c12fe3b23dd7e3"}}`



++++





(pw: mypassword)

Mnemonic Phrase
Another fancy version of your private key, that is actually used to derive multiple private keys.

A (typically) 12 or 24 word phrase that allows you to access infinite number of accounts.

Used by Ledger, TREZOR, MetaMask, Jaxx, and others.

Originates from BIP 39 Spec.

The accounts you can access with this phrase are determined by the "path".

Example 12-words: brain surround have swap horror body response double fire dumb bring hazard

Example 24-words: card enrich gesture connect kick topple fan body blind engine lemon swarm venue praise addict agent unaware equal bean sing govern income link leg

Hardware Wallet:
Typically, a single-purpose device that "holds" your private key(s), ensuring your private keys are safe.

Typically, they use a 24-word phrase. This phrase you should write down (not on your computer) and store separately from your hardware wallet.

If you lose your hardware wallet, you can still gain access to your accounts & funds via the word-phrase you wrote down.

Never type the word-phrase on your computer. It defeats the purpose of your hardware wallet.

AddressIdenticon / AddressIcon:
The colorful blob of colors that corresponds to your address.

It is an easy way to see if your address is correct.

Example 1
Example 2
Note: the above addresses are a single character different but have remarkably different icons & colors. Magic!

Hexadecimal
Used all over Ethereum for a variety of things, a hexadecimal string is comprised of the numbers 0 1 2 3 4 5 6 7 8 9 and A B C D E F
Seed
The input given to derive a private key. This should always be generated in a truly random way, not something you make up with your measly human brain.

If you chose the seed, it is known as a brain wallet

Brain Wallet
An account generated from a seed or password or passphrase of your choosing.

Humans are not capable of generating enough entropy and therefore the wallets derived from these phrases are insecure.

Brain wallets can be brute forced by super fast computers.

Brain wallet are insecure.

Don't use brain wallets.

Entropy
Also known as "randomness".

The more random something is, the more entropy it has, and the more secure it is.

Usually defined in "bits of entropy" or the number of years it would take to brute-force a ________ (e.g. private key) derived with that much entropy.

Ethereum private keys are 256-bit keys

24-Word mnemonic phrases are also 256 bits of entropy. 2048 words in the dictionary. 11 bits of entropy (the words). 11 * 24 = 264. The last word is a checksum.

TO DO STILL:
Derive / Derivation
Encryption
Encrypted vs Unencrypted Keys
Ledger
Difference between an exchange or hosted wallet & a wallet you control
MEW Knowledge Base Article on the Subject (WIP, too)
Node
Client (+ Light Client)
DAG
Decentralized
Blockchain
Gas (Gas Limit vs Gas Price)
https://myetherwallet.groovehq.com/knowledge_base/topics/what-is-gas

Hudson's recent post on gas

ICO
coin center has a good reference I think
DAO
Fork (Soft Fork vs Hard Fork)
Smart Contract
Ðapp
Hash
Multisig Wallet / Wallet Contract
WEI vs GWEI vs Shannon vs Ether
http://i.imgur.com/SXpY3HU.jpg

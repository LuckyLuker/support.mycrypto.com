{
"title" : "A Glossary of Common Terms in the Ethereum / Crypto Space",
"sort" : "35",
"category" : "Getting Started",
"description" : "Getting Started",
"date_published" : "2015-10-05T08:00:00+08:00",
"date_modified" : "2018-02-28T08:00:00+08:00"
}

---%

## Words are Hard

This is a list of terms you might encounter when using the MyCrypto interface.

#### [You can also read in Spanish](https://support.mycrypto.com/las-palabras-son-dificiles-definiendo-terminos-comunes-de-ethereum), thanks to [faraggi](https://github.com/faraggi/words-are-hard-es/blob/master/words-are-hard-es.md)

---

### Wallet

* The interface / client / wrapper / holder that you use to manage your account(s).

* Example: MyCrypto.com, your Ledger Hardware Wallet, a Multisig Wallet Contract.

### Account

* A public & private keypair that "holds" your funds.

* Your funds are actually stored on the blockchain, not in the wallet or account.

* Just like your Reddit account has a `username (public)` and `password (private)`, so does your Ethereum account. For additional security, you can use a password to encrypt your private key which would result in a `username (public)` and `password (private)` and `password for that password (private + more secure)`. See the `Keystore File` section.

### Address _("Public Key")_

* You use this to send funds **to** an account.

* Sometimes referred to as the "public key"

* A string made up of `0x` + `40 hexadecimal characters`.

* In Ethereum, the address begins with `0x`.

* Example: `0x06A85356DCb5b307096726FB86A78c59D38e08ee`

* This functions similarly to an email address.

### Public Key

* In cryptography, you have a keypair: the public and private key.

* You can derive a public key from a private key, but cannot derive a private key from a public key.

* (Advanced) In Ethereum, the address "acts" like the public key, but it's not actually the public key.

* (Advanced) In Ethereum, the public key is derived from the private key and is 128 hex characters. You then take the `"SHA3" (Keccak-256)` hash of this (64 characters), take the last 40 characters, and prefix with `0x`, give you your 42-character address.

### Private Key

* You use this to send funds **from** an account.

* The secret half of your Address / public key.

* A string of 64 hexadecimal characters.

* ([Almost](https://crypto.stackexchange.com/questions/30269/are-all-possible-ec-private-keys-valid)) every string of 64 hexadecimal characters is a private key.

* If you hand-type a private key differently today than yesterday, you will access a different wallet. Never hand type your private key.

* This is the string you need to send from your account. Without it you cannot access your funds. Although, you don't need to save this raw, unencrypted private key in this format. You can saving the fancy versions of it (e.g. the Keystore File / Mnemonic Phrase).

* Example: `afdfd9c3d2095ef696594f6cedcae59e72dcd697e2a7521b1578140422a4f890`

### Keystore File

* Encrypted version of your private key in JSON format (though it does not have a JSON extension)

* A fancy version of your private key that is protected by a password of your choosing.

* When combined with the password, it has the private key.

* Safer than a private key because you need the password.

* File name usually is in the format `UTC` + `--` + `DATE_CREATED` + `--` + `YOUR_ADDRESS_WITHOUT_THE_OX`

* Example of File Name: `UTC--2017-07-02T20-33-09.177Z--06a85356dcb5b307096726fb86a78c59d38e08ee`
* Example of Contents: `{"version":3,"id":"aa811d53-fe9a-44a2-bd1c-e737007b5591","address":"06a85356dcb5b307096726fb86a78c59d38e08ee","Crypto":{"ciphertext":"f5a7cc8d4b8cf93510b0d0d057f3a52ac79fd48e619e0638c4ffd978ca180248","cipherparams":{"iv":"975ab00192e2dd74170e91ca59c0b0bd"},"cipher":"aes-128-ctr","kdf":"scrypt","kdfparams":{"dklen":32,"salt":"0210f0d0b99e440dfbceb36373304638bac093a367ee7da6411cd165f7aa907a","n":1024,"r":8,"p":1},"mac":"8197a747a3855a10546a2ff939c36470daed78e393b670efa0c12fe3b23dd7e3"}}`

* (pw: `mypassword`)

### Mnemonic Phrase

* Another fancy version of your private key, that is actually used to derive multiple private keys.

* A (typically) 12 or 24 word phrase that allows you to access infinite number of accounts.

* Used by Ledger, TREZOR, MetaMask, Jaxx, and others.

* Originates from [BIP 39 Spec](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki).

* The accounts you can access with this phrase are determined by the "path".

* Example 12-words: `brain surround have swap horror body response double fire dumb bring hazard`

* Example 24-words: `card enrich gesture connect kick topple fan body blind engine lemon swarm venue praise addict agent unaware equal bean sing govern income link leg`

### Hardware Wallet:

* Typically, a single-purpose device that "holds" your private key(s), ensuring your private keys are safe.

* Typically, they use a 24-word phrase. This phrase you should write down (not on your computer) and store separately from your hardware wallet.

* If you lose your hardware wallet, you can still gain access to your accounts & funds via the word-phrase you wrote down.

* Never type the word-phrase on your computer. It defeats the purpose of your hardware wallet.

-[See here for more information about Hardware Wallets](https://support.mycrypto.com/hardware-wallets/)

### AddressIdenticon / AddressIcon:

* The colorful blob of colors that corresponds to your address.

* It is an easy way to see if your address is correct.

* [Example 1](https://i.imgur.com/lHUrIiZ.jpg)

* [Example 2](https://i.imgur.com/FvyLewS.jpg)

* _Note: the above addresses are a single character different but have remarkably different icons & colors. Magic!_

### Hexadecimal

* Used all over Ethereum for a variety of things, a hexadecimal string is comprised of the numbers `0 1 2 3 4 5 6 7 8 9` and `A B C D E F`

### Seed

* The input given to derive a private key. This should always be generated in a truly random way, not something you make up with your measly human brain.

* If you chose the seed, it is known as a `brain wallet`

### Brain Wallet

* An account generated from a seed or password or passphrase of your choosing.

* Humans are not capable of generating enough entropy and therefore the wallets derived from these phrases are insecure.

* Brain wallets can be brute forced by super fast computers.

* [Brain wallet are insecure.](https://www.reddit.com/r/ethereum/comments/45y8m7/brain_wallets_are_now_generally_shunned_by/)

* Don't use brain wallets.

### Entropy

* Also known as "randomness".

* The more random something is, the more entropy it has, and the more secure it is.

* Usually defined in "bits of entropy" or the number of years it would take to brute-force a **\_\_\_\_** (e.g. private key) derived with that much entropy.

* Ethereum private keys are 256-bit keys

* 24-Word mnemonic phrases are also 256 bits of entropy. 2048 words in the dictionary. 11 bits of entropy (the words). `11 * 24 = 264`. The last word is a checksum.

### Key Derivation

* Key derivation functions derive bytes suitable for cryptographic operations from passwords or other data sources using a pseudo-random function (PRF). Different KDFs are suitable for different tasks such as:

Cryptographic key derivation

Deriving a key suitable for use as input to an encryption algorithm. Typically this means taking a password and running it through an algorithm such as PBKDF2HMAC or HKDF. This process is typically known as key stretching.

Password storage

When storing passwords you want to use an algorithm that is computationally intensive. Legitimate users will only need to compute it once (for example, taking the user’s password, running it through the KDF, then comparing it to the stored value), while attackers will need to do it billions of times. Ideal password storage KDFs will be demanding on both computational and memory resources.

*taken from cryptography.io* - [Read Full Article](https://cryptography.io/en/latest/hazmat/primitives/key-derivation-functions/)

### Encryption

* In its most basic form, encryption is the process of encoding data, making it unintelligible and scrambled. In a lot of cases, encrypted data is also paired with an encryption key, and only those that possess the key will be able to open it.

An encryption key is a collection of algorithms designed to be totally unique. These are able to scramble and unscramble data, essentially unlocking the information and turning it back to readable data.

Usually, the person that is encrypting the data will possess the key that locks the data and will make 'copies' and pass them on to relevant people that require access. This process is called public-key cryptography.

*taken from techworld.com* - [Read Full Article](https://www.techworld.com/security/what-is-encryption-3659671/)

### Encrypted vs Unencrypted Keys

* Encrypted Keys require a password or some other type of authorization in order to access the encoded information. MyCrypto encrypts your private key via a Keystore File (UTC/JSON). Unencrypted Keys have been decrypted successfully or have initially not been encrypted.

### Decentralize / Decentralization

* The process of transferring authority of a single entity (ex. Government or large corporation) to multiple smaller entities.

### Trustless

* A distributed trustless consensus which the blockchain is responsible for. Since everyone has a copy of the ledger of all transactions ever executed, there is no need for a third-party. You can verify the transactions yourself, however the Ethereum blockchain and Bitcoin blockchain were created to ensure rules and agreements between all parties are executed when all conditions are met.

### Smart Contracts

* A piece of code (or program) that is stored on the blockchain network. Conditions of the contract are predefined by the users, if all conditions are met, certain actions are executed by the contract (program).

* These can be executed automatically by the same distributed blockchain that it is stored on.

* These contracts are designed to be tamper-proof permanent (which includes the code used in their creation). To edit a contract, one will have to create and deploy an entirely new contract.

### Blockchain

* A decentralized publicly owned ledger.

* Consists of a series of Blocks.

### Block

* A data structure that contains aggregated transaction data.

* Is cryptographically linked together to form the blockchain (literally, a chain of blocks).

* The first block in a blockchain is called the Genesis Block.

### Hashing

* Calculating a function that takes an arbitrary amount of input data and deterministically produces a fixed-length output known as the data's "hash".

* This can be used to verify that data has not be altered as any part of the input data is changed, the hash will change too.

### Mining

* The process by which transactions are verified and added to a Proof-of-Work blockchain.

* Solving cryptographic problems using high-powered, specialized computing hardware is the actual process that is being completed.

### Proof-of-Work

* A system of using to computational power to apply a method of security to the consensus of a blockchain (determining the order of blocks in a blockchain).

* Blocks of transactions must be hashed with an additional parameter which takes many tries to create a valid block hash.

* The successfully hashed block is considered a correct and valid proof of computational work.

* An alternative to this system is called Proof-Of-Stake.

### Proof-of-Stake

* A system of using tying up a validator's economic stake in the network, to allow them to have a random chance to propose the next block.

* After a block is proposed, it is then voted on by a pool of validators that have a certain economic representation of the network's units each.

* Benefits of Proof-of-Stake consensus algorithms: Energy efficiency leading to decreased environmental effects, reduced risk of centralization, and security.

* Casper Proof-of-Stake is Ethereum's future version of Proof-of-Stake.

### Multisignature Address

* A multisignature (multisig) address allows the address's creator to require multiple parties using different cryptographic keys to authorize a transaction.

* The exact process of this is defined at the time that the address is created.

* The reason why a multisig address is used is because it allows for increased security, and some level of resistance to theft.

### Unpermissioned vs Permissioned ledger

* Unpermissioned Ledgers (like the Bitcoin blockchain) have no single owner and any number of people can operate on them, and store a copy of them.

* Permissioned Ledgers, on the other hand, may have an owner and may also have a limited number of parties with the ability to read or write data to them.

All feedback, rewrites, clarification, typo-fixing, and requests for additions are more than welcome!
# LavaCoin

* Based on CryptoNote Protocol
* Untraceable Payments
* Unlinkable Transcations
* Double-Spending Proof
* Blockchain Analysis Resistance
* Egalitarian Proof
* Adaptive Parameters

## Untraceable Payments
CryptoNote provides users with a completely anonymous payment scheme. CryptoNote implements the ring signature technology which allows you to sign a message on behalf of a group. The signature only proves the message was created by someone from the group, but all the possible signers are indistinguishable from each other.

## Unlinkable Transcations
Even if outgoing transactions are untraceable, everyone may still be able to see the payments you have received and thus determine your income. However, by using a variation of the Diffie-Hellman exchange protocol, a receiver has multiple unique one-time addresses derived from his single public key. After funds are sent to these addresses they can only be redeemed by the receiver; and it would be impossible to cross-link these payments. 

## Double-Spending Proof
Nobody is able to spend the same money twice — even if all his signatures are anonymous. Every signature contains a key image — a kind of fingerprint of the secret key. It is based on a one-way cryptographic function; this implies that given only the key image it is impossible to restore the corresponding secret key. These key images are used to prevent double-spending. 

## Blockchain Analysis Resistance
Non-repeating one-time addresses and mixed keys in ring signatures make the whole blockchain resistant to analysis. Each future transaction will only increase the entropy and create additional obstacles for an analyst. 

## Egalitarian Proof
The proof of work mechanism acts as a voting system. Thus, it is crucial that during the voting process all the participants have equal voting privileges. CryptoNote brings this equality with its egalitarian proof of work, utilizing built-in CPU instructions, which are very hard and too expensive to implement in special purpose devices, but perfectly suitable for ordinary PCs. 

## Adaptive Parameters
A decentralized payment system must not depend on a single person's decisions, even if this person is a developer. CryptoNote has no hard-coded constants; magic numbers in the code are designed to be re-calculated based on the previous state of the network. Thus, they always change adaptively and independently, allowing the network to develop on its own. 



## Building LavaCoin

### On *nix

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, and Boost 1.55.

You may download them from:

* http://gcc.gnu.org/
* http://www.cmake.org/
* http://www.boost.org/
* Alternatively, it may be possible to install them using a package manager.

To build, change to a directory where this file is located, and run `make`. The resulting executables can be found in `build/release/src`.

**Advanced options:**

* Parallel build: run `make -j<number of threads>` instead of `make`.
* Debug build: run `make build-debug`.
* Test suite: run `make test-release` to run tests in addition to building. Running `make test-debug` will do the same to the debug version.
* Building with Clang: it may be possible to use Clang instead of GCC, but this may not work everywhere. To build, run `export CC=clang CXX=clang++` before running `make`.

### On Windows
Dependencies: MSVC 2015 or later, CMake 2.8.6 or later, and Boost 1.65. You may download them from:

* http://www.microsoft.com/
* http://www.cmake.org/
* http://www.boost.org/

To build, change to a directory where this file is located, and run theas commands: 
```
mkdir build
cd build
cmake -G "Visual Studio 14 Win64" .. -DBOOST_ROOT=<path to boost directory>
```

And then open the project in Visual Studio and build.

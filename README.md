# Ethdig.io smart contract

[Ethdig eth](https://ethdig.xyz)


### Check contract working


**Before you start, you need to install required packages.**

```
$ npm install ganache-cli truffle -g
$ npm install
```

**Launch private blockchain using ganache.**

`$ ganache-cli`

**Testing**

First of all, to ensure that everything works properly you should run tests.

`$ truffle test test/ethdig.xyz`

If everything was great you will see smth like this:
```
Compiling ./contracts/Ethdig.sol...
Compiling ./contracts/Theft.sol...


  Contract: Ethdig
    ✓ Has an owner
    ✓ Contract can accept incoming transactions (231ms)
    ✓ Reinvest is correct (157ms)
    ✓ Owner receives correct fee (270ms)
    ✓ Referrer commission works properly (598ms)
    ✓ Referrer: incorrectly specified referrer has no effect (425ms)
    ✓ Referrer: cash-back works properly (772ms)
    ✓ Check minimum invest
    ✓ Payout: check function getInvestorDividendsAmount (100ms)
    ✓ Payout: check function self payout (537ms)
    ✓ Check getDepositAmount & getInvestorCount functions (108ms)
    ✓ Payout: check payouts work properly (735ms)
    ✓ Check ownershipTransfer (290ms)
    ✓ Check revert on another contract (291ms)
    ✓ Check KOtH: a_good_investor (452ms)
    ✓ Check rounds (455ms)


  16 passing (7s)
```

To ensure that smart-contact can be used by tones of investors,
you should run `load-test.js

Before testing you should start ganache-cli with key `-a 500`  (investors count).

`$ ganache-cli -a 500`


Warning! This test took a lot of time!

`$ truffle test test/ethdig-loadtest.io`


If everything was great you will see smth like this:
```
Compiling ./contracts/Ethdig.sol...


  Contract: Ethdig
    ✓ Loadtesting: Create a many investors (700ms)
    ✓ Loadtesting: Check payout for a large number of investors (2716ms)
    ✓ Loadtesting: Check next round on a lot investors (851ms)


  3 passing (4s)
```

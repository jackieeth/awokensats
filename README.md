# Awoken Sats
Sats were awoken when sat numbers were inscribed in the inscription content. They are *Awoken Sats*.

- Magic Eden: https://magiceden.io/ordinals/marketplace/awoken

- Notes: Please use `ordiscan.com` to check those inscriptions for now. `ordinals.com` and `ord.io` still have cors restrictions so it may not work.

## Why?
Inscriptions are immutable digital artifacts. Inscriptions can also be dynamic machinery operating based on the Bitcoin blockchain's immutable data.

## How?
- barely awoken: inscribing a Sat number into the inscription content. 
- awoken: call Ord to find the inscription owner and do other cool stuff. Sat number [45015236932](https://ordiscan.com/inscription/62533038) inscribed in the content to retrieve owner address via [Ord](https://docs.ordinals.com/guides/explorer.html)
- advanced awoken: Sat number [156146060642193](https://ordiscan.com/inscription/62682641) inscribed in the content to retrieve owner address and look up KARMA (TAP token) balance via TRAC's [public endpoints](https://github.com/BennyTheDev/trac-tap-public-endpoint)

## Valid Sat Range
"Consider the genesis block to be satoshis `0` thru `4999999999` (despite them technically being unspendable).  The proceeds of block 1 would be `5000000000` (`5e9`) thru `9999999999` (`1e10 - 1`). The last satoshi of the block with 50 BTC reward would be `1049999999999999` (`50 x 210000 x 1e8 - 1`). Block 210000 would be `1050000000000000` - `1050002499999999`, spanning a total of `25 x 1e8` satoshis." ([ref](https://bitcointalk.org/index.php?topic=117224.0))

## Regex
To match the valid sat number (ranging from `5000000000` to `1050002499999999`) using regular expression in the inscription content

`(500000000\d|50000000[1-9]\d|5000000[1-9]\d{2}|500000[1-9]\d{3}|50000[1-9]\d{4}|5000[1-9]\d{5}|500[1-9]\d{6}|50[1-9]\d{7}|5[1-9]\d{8}|[6-9]\d{9}|[1-9]\d{10,14}|10[0-4]\d{13}|105000[01]\d{9}|1050002[0-4]\d{8})`

[Feedback?](https://twitter.com/JackieLeeETH)

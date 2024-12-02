# A. Research in Methodology

You’re developing an algorithm to detect the type of vulnerability similar to KyberSwap Exploit
(22 Nov 2023). Suggest a prospective algorithm (s) with reference provided. Free feel to delve
into technical details and be innovative, while keeping your explanation clear and
understandable to our team.
Candidate is expected to explain the following:
a) Own understandings of the major challenges to detect the exploit
b) Summary of the algorithm
c) Rationale behind using the algorithm
d) Core limitations
e) Core advantage
f) How to evaluate the effectiveness of the algorithms

## Reference

[Post Mortem : KyberSwap Exploit Swap](https://blog.kyberswap.com/post-mortem-kyberswap-elastic-exploit/#:~:text=Overview%3A%20On%20November%2022%2C%202023,significant%20amount%20of%20assets%20of)
[Defi Hacks Labs Code](https://github.com/SunWeb3Sec/DeFiHackLabs/blob/main/src/test/2023-11/KyberSwap_exp.eth.1.sol)

## Challenges of detecting the exploit

1. Flash Loans Complexity : flash loans allows users to borrow without collateral provided they are repaid in the same text. Detecting malicious loans is difficult due to complexity of its implementation and cuz attackers mimic legitimate arbitrage strategies.

2. AMM Manipulation: manipulating the price within an Automated Market Maker (AMM) by changing the liquidity distribution across ticks. Since its happens over shorter timeframes, complicating detection through conventional price monitoring.

3. Cross Protocol arbitrage: exploit price differences across multiple Protocols. Tracking is expensive due to data Enginering as there is no standard for data formats

4. High Tx Vol: monitoring every tx in real time and analyzing it is very computationally & infra expensive.

5. Onchain data limitations : onchain privacy soln and ofchain components and offchain oracles hinder detection

6. Sophisticated Attacks :

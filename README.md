# SushiProposal


## Problem:

Currently Sushiswap generates an annual protocol revenue of nearly $90M and has $4B in TVL but suffers from a few key economics problems:

1. The team is underpaid in relation to market value and does not have compensation alignment.

2. Sushi's Onsen, which is a key driver of new users and a competitive advantage, is dilutive.

3. The current SushiMaker model over concentrates rewards without a long term incentive.

## Proposed Solution:

[OpenOrg](http://openorg.gg) is proposing to solve this problem through a new version of the SushiMaker contract located at `0xE11fc0B43ab98Eb91e9836129d1ee7c3Bc95df50`.

Our draft proposal in repo makes a few small changes:

### 1) Team Compensation:
8% of the fee collected in the SushiMaker is directed to the Sushi Treasury to be used for team compensation. 

This is an increase of roughly $7M in new treasury allocation allowing the team to increase salaries across the board and improve hiring. 

Rather than the current proposal of using existing treasury Sushi, this creates a long term budget the team can use that is refreshing yearly.

It also aligns the goals of the dev team with the DAO, if the want to increase allocation it can be done by increasing the overall volume use of Sushi products.

Also unlike a one time grant from the treasury which is dilutive this allocation still puts buying pressure on the market Sushi price by going through the Sushi maker.

### 2) Onsen Vault:

This proposal would also create an Onsen Vault. The Onsen program is a key competitive driver for Sushi, but creates a dilutive set up that will eventuall run out of capital.

Instead this diverts 8% of SushiMaker earnings to a vault to be used in Onsen program compensation moving forward. Shifting Onsen from being dilutive to being more buying pressure on Sushi.

### 3) Sushi Burn:

The current SushiMaker model with xSushi continues to concentrate Sushi into the hands of those who already have it who can only realize any of the value captured by dumping it, only to re-earn that Sushi from current staking.

In order to combat that cycle this version of SushiMaker would introduce a burn of the portion of the fees buy market buying Sushi and burning that amount.

Currently this is set at 12%, the equivelent of $10M a year.

While this is diverted from the xSushi component, it ultimately has the same economic impact for those users while create a deflationary offset for both Sushi and xSushi holders who proportionally have more governance authority with each burn.

This model creates a more uniform impact for the asset.

### 4) xSushi Reduction:

This would in turn lower xSushi rewards to 72% of their current value, but the economic equivelent should roughly be the same as it is now because this removes deflationary measure of treasury payout, and reduces the deflationary impact of the Onsen.


The SushiMaker.sol in this repo is a quick typed draft of the proposed contract and is not yet tested. It can likely be better implemented through directing the initial \_swap to a seperate splitter contract to manage the logic rather than adding the gas to an existing complex transaction.

# Splinterlands-API
API Documentation  
**//_Work in progress._**

---

- [Splinterlands-API](#splinterlands-api)
    + [General](#general)
      - [Game Settings](#game-settings)
      - [Transaction Lookup](#transaction-lookup)
      - [Transaction History](#transaction-history)
      - [Global Card Stats](#global-card-stats)
      - [Card Details](#card-details)
      - [Card Lookup](#card-lookup)
      - [Player Collection](#player-collection)
      - [Check Promo Code](#check-promo-code)
    + [Market](#market)
      - [Market Listings - All](#market-listings---all)
      - [Grouped Market Listings - Summary](#grouped-market-listings---summary)
      - [Market Transaction Lookup](#market-transaction-lookup)
      - [Player Market Sale History](#player-market-sale-history)
      - [Card Pack Purchase Lookup](#card-pack-purchase-lookup)
    + [Gameplay](#gameplay)
      - [Top - Last 50 Matches](#top---last-50-matches)
      - [Player - Last 50 Matches](#player---last-50-matches)
      - [Battle Transaction Lookup](#battle-transaction-lookup)
    + [Player Status](#player-status)
      - [Get Player Balances](#get-player-balances)
      - [Player Settings - General](#player-settings---general)
      - [Player Settings - Login](#player-settings---login)
      - [Player Quest](#player-quest)
      - [Referrals](#referrals)
    + [Guilds](#guilds)
      - [Guild Members](#guild-members)
      - [Guild Lookup](#guild-lookup)


---

### General

#### Game Settings
>*https://steemmonsters.com/purchases/settings*

_Example Response:_

>booster_pack_price: 2 <br>
market_fee: 500 <br>
paypal_acct: "matt@steemmonsters.com" <br>
paypal_sandbox: false <br>
sbd_price: 0.7203524 <br>
starter_pack_price: 10 <br>
starter_pack_price_account_create: 10 <br>
steem_price: 0.1502343 <br>
usd_enabled: true <br>

#### Transaction Lookup
> https://steemmonsters.com/transactions/lookup?trx_id=09c8ac9db08d246696fa795cbf03ff07b83303e6

_Example Response:_

>block_id: "0242021dc93ce1ccca2794d7b58bf2e8c431465c" <br>
block_num: 37880349 <br>
created_date: "2019-11-04T12:46:55.560Z" <br>
data: "{"type":"daily"}" <br>
error: null <br>
id: "09c8ac9db08d246696fa795cbf03ff07b83303e6" <br>
player: "buffnecked-ibis" <br>
prev_block_id: "0242021c1db4e5e4c31b7d5ff819352194e7d400" <br>
result: "{…}" <br>
sbd_price: "0.717364" <br>
steem_price: "0.149986" <br>
success: true <br>
type: "sm_start_quest" <br>

#### Transaction History
> https://steemmonsters.com/transactions/history?from_block=37904629  

Gets 1000 Splinterlands transactions starting from the target block.


#### Global Card Stats
> https://steemmonsters.com/cards/stats

_Example Response:_  

>card_detail_id: 1 <br>
edition: 0 <br>
gold: false <br>
num_burned: "159" <br>
num_cards: "8026" <br>
total_burned_xp: "5540" <br>
total_xp: "879140" <br>

#### Card Details
> https://steemmonsters.com/cards/get_details

_Example Response:_  

>color: "Red" <br>
created_block_num: null <br>
distribution: […] <br>
drop_rate: 80 <br>
editions: "0,1" <br>
id: 1 <br>
is_starter: false <br>
last_update_tx: null <br>
name: "Goblin Shaman" <br>
rarity: 1 <br>
stats: {…} <br>
sub_type: null <br>
total_printed: 174855 <br>
type: "Monster" <br>

#### Card Lookup
> https://steemmonsters.com/cards/find?ids=C3-79-UUT7TSLVN4

_Example Response:_  

> alpha_xp: null <br>
buy_price: null <br>
card_detail_id: 79 <br>
delegated_to: null <br>
delegation_tx: null <br>
details: {…} <br>
edition: 3 <br>
gold: false <br>
last_transferred_block: 36440204 <br>
last_used_block: 36300473 <br>
market_id: null <br>
player: "kiokizz" <br>
skin: null <br>
uid: "C3-79-UUT7TSLVN4" <br>
xp: 0 <br>

#### Player Collection
> https://steemmonsters.com/cards/collection/kiokizz

Lists every card in a players collection.

#### Check Promo Code
> https://steemmonsters.com/purchases/check_code?code=K5XF-7N1N

_Example Response:_

>error: "Promo code: [K5XF-7N1N] has already been used." <br>
valid: false

---

### Market
#### Market Listings - All
> https://steemmonsters.com/market/for_sale

_Example Response:_

>market_id:"61f090b013c28e5119119184bf3cd10aa7bccef7-14" <br>
fee_percent:500,"uid":"C2-128-68T1UWO9SW" <br>
seller:"cannonwar" <br>
card_detail_id:128 <br>
xp:0 <br>
gold:false <br>
edition:2 <br>
last_used_block:null <br>
last_transferred_block":null <br>
buy_price:"0.237" <br>
currency:"USD" <br>
desc:null <br>

#### Grouped Market Listings - Summary
> https://steemmonsters.com/market/for_sale_grouped

_Example Response:_

>card_detail_id: 1 <br>
edition: 0 <br>
gold: false <br>
high_price: 302.99 <br>
low_price: 0.294 <br>
low_price_bcx: 0.148936170212766 <br>
qty: 103 <br>

#### Market Transaction Lookup
> https://steemmonsters.com/market/status?id=d8f8593d637ebdd0bca7994dd7e1a15d9f12efa7-0

_Example Response:_

>buy_price: "0.020" <br>
cards: [{…}] <br>
completed_date: null <br>
created_date: "2019-11-05T09:50:40.001Z" <br>
currency: "USD" <br>
desc: null <br>
expiration_date: null <br>
fee_percent: 500 <br>
id: 3078824 <br>
lock_block: null <br>
locked_by: null <br>
num_cards: 1 <br>
payment: null <br>
purchaser: null <br>
sell_trx_id: "d8f8593d637ebdd0bca7994dd7e1a15d9f12efa7-0" <br>
seller: "kiokizz" <br>
starting_price: null <br>
status: 0 <br>
transaction_id: null <br>
type: "SELL" <br>

#### Player Market Sale History
> https://steemmonsters.com/market/history?player=kiokizz

_Example Response:_

>buy_price: "0.970" <br>
card_detail_id: 25 <br>
card_id: "C1-25-OWZ9GQKUFK" <br>
completed_date: "2019-10-29T23:44:21.775Z" <br>
created_date: "2019-10-29T23:26:36.246Z" <br>
currency: "USD" <br>
desc: null <br>
edition: 1 <br>
expiration_date: null <br>
fee_percent: 500 <br>
gold: false <br>
id: 3047243 <br>
lock_block: null <br>
locked_by: null <br>
num_cards: 1 <br>
payment: "1059.183 DEC" <br>
purchaser: "kiokizz" <br>
sell_trx_id: "24c791da3d73e90d860939d0f54a5f8dd28fabbe-0" <br>
seller: "luckyice" <br>
starting_price: null <br>
status: 1 <br>
transaction_id: "691ed9c606c623d6acb72f6debdda90242cf1cf4" <br>
type: "SELL" <br>
xp: 440 <br>

#### Card Pack Purchase Lookup
> https://steemmonsters.com/purchases/status?id=P-2H7MGOOU74

_Example Response:_

> amount_usd: "20.00" <br>
bonus_quantity: 0 <br>
completed_date: "2018-09-11T18:24:12.786Z" <br>
created_date: "2018-09-11T18:19:58.801Z" <br>
currency: "USD" <br>
edition: null <br>
merchant: null <br>
payment: "28.043 STEEM" <br>
player: "sacred-agent" <br>
quantity: 10 <br>
status: 1 <br>
transaction_id: "366d91018a989b24e519b97edab9f364e90d7a90" <br>
type: "booster_pack" <br>
uid: "P-2H7MGOOU74" <br>

---

### Gameplay

#### Top - Last 50 Matches
> https://steemmonsters.com/battle/history?player=%24top

_Example Response:_

>battle_queue_id_1: "dcfc3739231d52b722531ba319bb82b658d63f56" <br>
battle_queue_id_2: "00374cfaf25bee57358e2b72a01b031781ebd30f" <br>
block_num: 37932809 <br>
created_date: "2019-11-06T08:35:18.631Z" <br>
current_streak: 2 <br>
dec_info: "{…}" <br>
details: "{"seed":"e50144ba8997191038fe6381fd689339","rounds" <br>
inactive: "Black,Red" <br>
mana_cap: 30 <br>
match_type: "Ranked" <br>
player_1: "sensful" <br>
player_1_rating_final: 4190 <br>
player_1_rating_initial: 4175 <br>
player_2: "vaansteam" <br>
player_2_rating_final: 4078 <br>
player_2_rating_initial: 4093 <br>
rshares: 20510572 <br>
ruleset: "Broken Arrows" <br>
settings: null <br>
winner: "sensful" <br>

#### Player - Last 50 Matches
> https://steemmonsters.com/battle/history?player=kiokizz

Last 50 Matches for target player.

#### Battle Transaction Lookup
> https://steemmonsters.com/battle/status?id=53d989a49ce9f8d15d945240f2621682b26b552d

_Example Response:_

>app: null <br>
created_block_num: 37852963 <br>
created_date: "2019-11-03T13:54:48.000Z" <br>
expiration_block_num: 37853023 <br>
expiration_date: "2019-11-03T13:57:48.000Z" <br>
id: "53d989a49ce9f8d15d945240f2621682b26b552d" <br>
inactive: "Black,White" <br>
mana_cap: 26 <br>
match_block_num: 37852970 <br>
match_date: "2019-11-03T13:55:09.000Z" <br>
match_type: "Ranked" <br>
opponent: "89eb915b4c3356462ca4d02c99213d27d1217ad2" <br>
opponent_player: "stranger27" <br>
opponent_team_hash: "523e5673a683d8e1842bd8db11737a04" <br>
player: "boatbilled-heron" <br>
reveal_block_id: "37853016" <br>
reveal_tx: "b317ca6b468f1eca959715e0e948e8dd04fda702" <br>
ruleset: "Earthquake" <br>
settings: null <br>
status: 2 <br>
submit_expiration_block_num: 37853016 <br>
submit_expiration_date: "2019-11-03T13:57:27.000Z" <br>
summoner_level: null <br>
team: "{…}" <br>
team_hash: "5c32b85eb1d319ef3ec546aa0feb0975" <br>

---

### Player Status
#### Get Player Balances
> https://steemmonsters.com/players/balances?username=ottermaker

_Example Response:_

>0: {player: "ottermaker", token: "BETA", balance: 0} <br>
balance: 0 <br>
player: "ottermaker" <br>
token: "BETA" <br>
1: {player: "ottermaker", token: "DEC", balance: 232373.361} <br>
balance: 232373.361 <br>
player: "ottermaker" <br>
token: "DEC" <br>
2: {player: "ottermaker", token: "ECR", balance: null, last_reward_block: null} <br>
balance: null <br>
last_reward_block: null <br>
player: "ottermaker" <br>
token: "ECR" <br>

#### Player Settings - General
> https://steemmonsters.com/players/details?name=kiokizz

_Example Response:_

>battles: 64162 <br>
capture_rate: 6630 <br>
champion_points: 61 <br>
current_streak: 3 <br>
guild: {…} <br>
join_date: "2018-06-01T02:04:20.076Z" <br>
last_reward_block: 37926905 <br>
longest_streak: 62 <br>
max_rank: 283 <br>
max_rating: 4161 <br>
name: "kiokizz" <br>
rank: "833" <br>
rating: 1924 <br>
season_details: {…} <br>
starter_pack_purchase: true <br>
wins: 28584  <br>

#### Player Settings - Login
> https://steemmonsters.com/players/login?name=kiokizz

More detailed player settings. Known to update more slowly than [Player Settings - General](#player-settings---general).

#### Player Quest
> https://steemmonsters.com/players/quests?username=kiokizz

_Example Response:_

>claim_date: "2019-11-06T03:41:18.917Z"  <br>
claim_trx_id: "4a191c60448b9116529e2692bae9b964a4e9ed8e" <br>
completed_items: 5 <br>
created_block: 37911338 <br>
created_date: "2019-11-05T14:39:51.537Z" <br>
id: "cfb4854676784c161036496464d1523b75446279" <br>
name: "Stir the Volcano" <br>
player: "kiokizz" <br>
rating: 1924 <br>
refresh_trx_id: null <br>
reward_qty: 6 <br>
total_items: 5 <br>

#### Referrals
> https://steemmonsters.com/players/referrals?username=kiokizz

_Example Response:_

>battles: 13154 <br>
join_date: "2018-10-30T05:35:27.203Z" <br>
name: "sm-starter-beta" <br>
rating: 781 <br>
starter_pack_purchase: true <br>

---

### Guilds
#### Guild Members
> https://steemmonsters.com/guilds/members?guild_id=d14d94bfab9f2532e26c33732cdba602d316f5bf

_Example Response:_

>data: "{"contributions":{"quest_lodge":57}}" <br>
guild_id: "d14d94bfab9f2532e26c33732cdba602d316f5bf" <br>
is_online: false <br>
join_date: "2019-07-29T23:17:00.000Z" <br>
player: "lava-heron" <br>
rank: 1 <br>
rating: 3320 <br>
status: "active" <br>

#### Guild Lookup
> https://steemmonsters.com/guilds/find?id=d14d94bfab9f2532e26c33732cdba602d316f5bf

_Example Response:_

>announcements: [] <br>
buildings: "{"guild_hall":{"level":6,"contributions":210000},"quest_lodge":{"level":6,"contributions":555}}" <br>
created_date: "2019-07-29T23:13:12.000Z" <br>
data: "{"crest":{"banner":"blue","decal":null}}" <br>
description: "Guild for Herons Unlimited accounts.…" <br>
id: "d14d94bfab9f2532e26c33732cdba602d316f5bf" <br>
language: "English" <br>
level: 6 <br>
membership_type: "invite_only" <br>
motto: "Herons Unlimited" <br>
name: "Herons Unlimited" <br>
num_members: "21" <br>
owner: "zigzag-heron" <br>
rank: "14" <br>
rating: "52409" <br>
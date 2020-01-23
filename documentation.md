## Classes

<dl>
<dt><a href="#Driver">Driver</a></dt>
<dd></dd>
<dt><a href="#Model">Model</a></dt>
<dd></dd>
</dl>

## Typedefs

<dl>
<dt><a href="#coinParam">coinParam</a> : <code><a href="#Model.Coin">Coin</a></code></dt>
<dd><p>Coin model with properties needed to fetch supplies.</p>
</dd>
<dt><a href="#modifierParam">modifierParam</a> : <code>string</code></dt>
<dd><p>Address which balance is used as a modifier.</p>
</dd>
<dt><a href="#referenceParam">referenceParam</a> : <code>string</code></dt>
<dd><p>Reference to a coin unique for the blockchain. E.g. a smart contract address.</p>
</dd>
<dt><a href="#decimalsParam">decimalsParam</a> : <code>number</code></dt>
<dd><p>Amount of decimals used for this coin.</p>
</dd>
</dl>

<a name="Driver"></a>

## Driver
**Kind**: global class  

* [Driver](#Driver)
    * [new Driver()](#new_Driver_new)
    * _static_
        * [.fetchTotalSupply](#Driver.fetchTotalSupply) ⇒ <code>number</code>
        * [.fetchCirculatingSupply](#Driver.fetchCirculatingSupply) ⇒ <code>number</code>
        * [.fetchMaxSupply](#Driver.fetchMaxSupply) ⇒ <code>number</code>
        * [.fetchBalance](#Driver.fetchBalance) ⇒ <code>number</code>
        * [.fetchAssetTotalSupply](#Driver.fetchAssetTotalSupply) ⇒ <code>number</code>
        * [.fetchAssetBalance](#Driver.fetchAssetBalance) ⇒ <code>number</code>
        * [.getSupply](#Driver.getSupply) ⇒ [<code>Promise.&lt;Supply&gt;</code>](#Model.Supply)
    * _inner_
        * [~BlockchainInfo](#Driver.BlockchainInfo) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.BlockchainInfo+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchCirculatingSupply()](#Driver.BlockchainInfo+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
            * [.fetchMaxSupply()](#Driver.BlockchainInfo+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
            * [.getSupply()](#Driver.BlockchainInfo+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~CardanoExplorer](#Driver.CardanoExplorer) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.CardanoExplorer+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchBalance(modifier)](#Driver.CardanoExplorer+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
            * [.getSupply(coin)](#Driver.CardanoExplorer+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~ChainNemNinja](#Driver.ChainNemNinja) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.ChainNemNinja+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchMaxSupply()](#Driver.ChainNemNinja+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
            * [.fetchBalance(modifier)](#Driver.ChainNemNinja+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
            * [.getSupply(coin)](#Driver.ChainNemNinja+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~CryptoidDash](#Driver.CryptoidDash) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.CryptoidDash+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchCirculatingSupply()](#Driver.CryptoidDash+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
            * [.getSupply()](#Driver.CryptoidDash+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~DogeChain](#Driver.DogeChain) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.DogeChain+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchCirculatingSupply()](#Driver.DogeChain+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
            * [.getSupply()](#Driver.DogeChain+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~Etherscan](#Driver.Etherscan) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.Etherscan+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchBalance(modifier)](#Driver.Etherscan+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
            * [.fetchAssetTotalSupply(reference, decimals)](#Driver.Etherscan+fetchAssetTotalSupply) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
            * [.fetchAssetBalance(reference, modifier, decimals)](#Driver.Etherscan+fetchAssetBalance) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
            * [.getSupply(coin)](#Driver.Etherscan+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~Lisk](#Driver.Lisk) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.Lisk+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchBalance(modifier)](#Driver.Lisk+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
            * [.getSupply(coin)](#Driver.Lisk+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~LitecoinNet](#Driver.LitecoinNet) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.LitecoinNet+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchCirculatingSupply()](#Driver.LitecoinNet+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
            * [.fetchMaxSupply()](#Driver.LitecoinNet+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
            * [.getSupply()](#Driver.LitecoinNet+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~MoneroBlocks](#Driver.MoneroBlocks) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.MoneroBlocks+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchCirculatingSupply()](#Driver.MoneroBlocks+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
            * [.getSupply()](#Driver.MoneroBlocks+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~NeoScan](#Driver.NeoScan) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.NeoScan+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchBalance(modifier)](#Driver.NeoScan+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
            * [.fetchAssetTotalSupply(reference)](#Driver.NeoScan+fetchAssetTotalSupply) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
            * [.fetchAssetBalance(reference, modifier)](#Driver.NeoScan+fetchAssetBalance) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
            * [.getSupply(coin)](#Driver.NeoScan+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~OmniExplorer](#Driver.OmniExplorer) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.OmniExplorer+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchBalance(modifier)](#Driver.OmniExplorer+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
            * [.fetchAssetTotalSupply(reference)](#Driver.OmniExplorer+fetchAssetTotalSupply) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
            * [.fetchAssetBalance(reference, modifier)](#Driver.OmniExplorer+fetchAssetBalance) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
            * [.getSupply(coin)](#Driver.OmniExplorer+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)
        * [~Ripple](#Driver.Ripple) ⇐ [<code>Driver</code>](#Driver)
            * [.fetchTotalSupply()](#Driver.Ripple+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
            * [.fetchCirculatingSupply()](#Driver.Ripple+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
            * [.fetchMaxSupply()](#Driver.Ripple+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
            * [.getSupply()](#Driver.Ripple+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="new_Driver_new"></a>

### new Driver()
Driver parent class, to be extended by drivers for specific block explorers.

<a name="Driver.fetchTotalSupply"></a>

### Driver.fetchTotalSupply ⇒ <code>number</code>
Fetch the total supply of a coin

**Kind**: static namespace of [<code>Driver</code>](#Driver)  
**Returns**: <code>number</code> - All the currently mined coins.  
<a name="Driver.fetchCirculatingSupply"></a>

### Driver.fetchCirculatingSupply ⇒ <code>number</code>
Fetch the circulating supply of a coin

**Kind**: static namespace of [<code>Driver</code>](#Driver)  
**Returns**: <code>number</code> - The total supply minus coins not in circulation, such as burned, premined or escrowed coins.  
<a name="Driver.fetchMaxSupply"></a>

### Driver.fetchMaxSupply ⇒ <code>number</code>
Fetch the maximum supply of a coin

**Kind**: static namespace of [<code>Driver</code>](#Driver)  
**Returns**: <code>number</code> - The maximum possible amount of supply ever to be reached.  
<a name="Driver.fetchBalance"></a>

### Driver.fetchBalance ⇒ <code>number</code>
Fetch the balance

**Kind**: static namespace of [<code>Driver</code>](#Driver)  
**Returns**: <code>number</code> - Amount on a specific address.  
<a name="Driver.fetchAssetTotalSupply"></a>

### Driver.fetchAssetTotalSupply ⇒ <code>number</code>
Fetch the total supply of an asset, i.e. a token on a blockchain.

**Kind**: static namespace of [<code>Driver</code>](#Driver)  
**Returns**: <code>number</code> - Total amount of a token.  
<a name="Driver.fetchAssetBalance"></a>

### Driver.fetchAssetBalance ⇒ <code>number</code>
Fetch asset balance

**Kind**: static namespace of [<code>Driver</code>](#Driver)  
**Returns**: <code>number</code> - Balance of a specific token on a specific address, to be used as supply modifier in order to
  calculate the circulating supply.  
<a name="Driver.getSupply"></a>

### Driver.getSupply ⇒ [<code>Promise.&lt;Supply&gt;</code>](#Model.Supply)
Drivers must include a getSupplies method. This method will call supported supply data
such as methods to fetch total, circulating and max supply.

**Kind**: static namespace of [<code>Driver</code>](#Driver)  
**Returns**: [<code>Promise.&lt;Supply&gt;</code>](#Model.Supply) - Returns a promise of a supply model.  

| Param | Type | Description |
| --- | --- | --- |
| [coin] | [<code>Coin</code>](#Model.Coin) | The getSupply method gets called with an [coin instance](#Model.Coin). |

<a name="Driver.BlockchainInfo"></a>

### Driver~BlockchainInfo ⇐ [<code>Driver</code>](#Driver)
BlockchainInfo driver. Supports circulating and max supply for BTC.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~BlockchainInfo](#Driver.BlockchainInfo) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.BlockchainInfo+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchCirculatingSupply()](#Driver.BlockchainInfo+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
    * [.fetchMaxSupply()](#Driver.BlockchainInfo+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
    * [.getSupply()](#Driver.BlockchainInfo+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.BlockchainInfo+fetchTotalSupply"></a>

#### blockchainInfo.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>BlockchainInfo</code>](#Driver.BlockchainInfo)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.BlockchainInfo+fetchCirculatingSupply"></a>

#### blockchainInfo.fetchCirculatingSupply() ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
**Kind**: instance method of [<code>BlockchainInfo</code>](#Driver.BlockchainInfo)  
**Extends**: [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)  
<a name="Driver.BlockchainInfo+fetchMaxSupply"></a>

#### blockchainInfo.fetchMaxSupply() ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
**Kind**: instance method of [<code>BlockchainInfo</code>](#Driver.BlockchainInfo)  
**Extends**: [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)  
<a name="Driver.BlockchainInfo+getSupply"></a>

#### blockchainInfo.getSupply() ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>BlockchainInfo</code>](#Driver.BlockchainInfo)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  
<a name="Driver.CardanoExplorer"></a>

### Driver~CardanoExplorer ⇐ [<code>Driver</code>](#Driver)
Cardano explorer driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~CardanoExplorer](#Driver.CardanoExplorer) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.CardanoExplorer+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchBalance(modifier)](#Driver.CardanoExplorer+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
    * [.getSupply(coin)](#Driver.CardanoExplorer+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.CardanoExplorer+fetchTotalSupply"></a>

#### cardanoExplorer.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>CardanoExplorer</code>](#Driver.CardanoExplorer)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.CardanoExplorer+fetchBalance"></a>

#### cardanoExplorer.fetchBalance(modifier) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
**Kind**: instance method of [<code>CardanoExplorer</code>](#Driver.CardanoExplorer)  
**Extends**: [<code>fetchBalance</code>](#Driver.fetchBalance)  

| Param | Type | Description |
| --- | --- | --- |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.CardanoExplorer+getSupply"></a>

#### cardanoExplorer.getSupply(coin) ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>CardanoExplorer</code>](#Driver.CardanoExplorer)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  

| Param | Type | Description |
| --- | --- | --- |
| coin | [<code>coinParam</code>](#coinParam) | [coinParam](#coinParam) |

<a name="Driver.ChainNemNinja"></a>

### Driver~ChainNemNinja ⇐ [<code>Driver</code>](#Driver)
Chain Nem Ninja / Nembex driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~ChainNemNinja](#Driver.ChainNemNinja) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.ChainNemNinja+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchMaxSupply()](#Driver.ChainNemNinja+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
    * [.fetchBalance(modifier)](#Driver.ChainNemNinja+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
    * [.getSupply(coin)](#Driver.ChainNemNinja+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.ChainNemNinja+fetchTotalSupply"></a>

#### chainNemNinja.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>ChainNemNinja</code>](#Driver.ChainNemNinja)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.ChainNemNinja+fetchMaxSupply"></a>

#### chainNemNinja.fetchMaxSupply() ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
**Kind**: instance method of [<code>ChainNemNinja</code>](#Driver.ChainNemNinja)  
**Extends**: [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)  
<a name="Driver.ChainNemNinja+fetchBalance"></a>

#### chainNemNinja.fetchBalance(modifier) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
**Kind**: instance method of [<code>ChainNemNinja</code>](#Driver.ChainNemNinja)  
**Extends**: [<code>fetchBalance</code>](#Driver.fetchBalance)  

| Param | Type | Description |
| --- | --- | --- |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.ChainNemNinja+getSupply"></a>

#### chainNemNinja.getSupply(coin) ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>ChainNemNinja</code>](#Driver.ChainNemNinja)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  

| Param | Type | Description |
| --- | --- | --- |
| coin | [<code>coinParam</code>](#coinParam) | [coinParam](#coinParam) |

<a name="Driver.CryptoidDash"></a>

### Driver~CryptoidDash ⇐ [<code>Driver</code>](#Driver)
Cryptoid Dash driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~CryptoidDash](#Driver.CryptoidDash) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.CryptoidDash+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchCirculatingSupply()](#Driver.CryptoidDash+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
    * [.getSupply()](#Driver.CryptoidDash+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.CryptoidDash+fetchTotalSupply"></a>

#### cryptoidDash.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>CryptoidDash</code>](#Driver.CryptoidDash)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.CryptoidDash+fetchCirculatingSupply"></a>

#### cryptoidDash.fetchCirculatingSupply() ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
**Kind**: instance method of [<code>CryptoidDash</code>](#Driver.CryptoidDash)  
**Extends**: [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)  
<a name="Driver.CryptoidDash+getSupply"></a>

#### cryptoidDash.getSupply() ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>CryptoidDash</code>](#Driver.CryptoidDash)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  
<a name="Driver.DogeChain"></a>

### Driver~DogeChain ⇐ [<code>Driver</code>](#Driver)
Dogechain driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~DogeChain](#Driver.DogeChain) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.DogeChain+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchCirculatingSupply()](#Driver.DogeChain+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
    * [.getSupply()](#Driver.DogeChain+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.DogeChain+fetchTotalSupply"></a>

#### dogeChain.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>DogeChain</code>](#Driver.DogeChain)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.DogeChain+fetchCirculatingSupply"></a>

#### dogeChain.fetchCirculatingSupply() ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
**Kind**: instance method of [<code>DogeChain</code>](#Driver.DogeChain)  
**Extends**: [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)  
<a name="Driver.DogeChain+getSupply"></a>

#### dogeChain.getSupply() ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>DogeChain</code>](#Driver.DogeChain)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  
<a name="Driver.Etherscan"></a>

### Driver~Etherscan ⇐ [<code>Driver</code>](#Driver)
Etherscan driver. Supports circulating and total supply for ethereum and
tokens on the ethereum blockchain.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~Etherscan](#Driver.Etherscan) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.Etherscan+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchBalance(modifier)](#Driver.Etherscan+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
    * [.fetchAssetTotalSupply(reference, decimals)](#Driver.Etherscan+fetchAssetTotalSupply) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
    * [.fetchAssetBalance(reference, modifier, decimals)](#Driver.Etherscan+fetchAssetBalance) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
    * [.getSupply(coin)](#Driver.Etherscan+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.Etherscan+fetchTotalSupply"></a>

#### etherscan.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>Etherscan</code>](#Driver.Etherscan)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.Etherscan+fetchBalance"></a>

#### etherscan.fetchBalance(modifier) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
**Kind**: instance method of [<code>Etherscan</code>](#Driver.Etherscan)  
**Extends**: [<code>fetchBalance</code>](#Driver.fetchBalance)  

| Param | Type | Description |
| --- | --- | --- |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.Etherscan+fetchAssetTotalSupply"></a>

#### etherscan.fetchAssetTotalSupply(reference, decimals) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
**Kind**: instance method of [<code>Etherscan</code>](#Driver.Etherscan)  
**Extends**: [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)  

| Param | Type | Description |
| --- | --- | --- |
| reference | [<code>referenceParam</code>](#referenceParam) | [referenceParam](#referenceParam) |
| decimals | [<code>decimalsParam</code>](#decimalsParam) | [decimalsParam](#decimalsParam) |

<a name="Driver.Etherscan+fetchAssetBalance"></a>

#### etherscan.fetchAssetBalance(reference, modifier, decimals) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
**Kind**: instance method of [<code>Etherscan</code>](#Driver.Etherscan)  
**Extends**: [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)  

| Param | Type | Description |
| --- | --- | --- |
| reference | [<code>referenceParam</code>](#referenceParam) | [referenceParam](#referenceParam) |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |
| decimals | [<code>decimalsParam</code>](#decimalsParam) | [decimalsParam](#decimalsParam) |

<a name="Driver.Etherscan+getSupply"></a>

#### etherscan.getSupply(coin) ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>Etherscan</code>](#Driver.Etherscan)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  

| Param | Type | Description |
| --- | --- | --- |
| coin | [<code>coinParam</code>](#coinParam) | [coinParam](#coinParam) |

<a name="Driver.Lisk"></a>

### Driver~Lisk ⇐ [<code>Driver</code>](#Driver)
Lisk driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~Lisk](#Driver.Lisk) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.Lisk+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchBalance(modifier)](#Driver.Lisk+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
    * [.getSupply(coin)](#Driver.Lisk+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.Lisk+fetchTotalSupply"></a>

#### lisk.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>Lisk</code>](#Driver.Lisk)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.Lisk+fetchBalance"></a>

#### lisk.fetchBalance(modifier) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
**Kind**: instance method of [<code>Lisk</code>](#Driver.Lisk)  
**Extends**: [<code>fetchBalance</code>](#Driver.fetchBalance)  

| Param | Type | Description |
| --- | --- | --- |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.Lisk+getSupply"></a>

#### lisk.getSupply(coin) ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>Lisk</code>](#Driver.Lisk)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  

| Param | Type | Description |
| --- | --- | --- |
| coin | [<code>coinParam</code>](#coinParam) | [coinParam](#coinParam) |

<a name="Driver.LitecoinNet"></a>

### Driver~LitecoinNet ⇐ [<code>Driver</code>](#Driver)
LitecoinNet driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~LitecoinNet](#Driver.LitecoinNet) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.LitecoinNet+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchCirculatingSupply()](#Driver.LitecoinNet+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
    * [.fetchMaxSupply()](#Driver.LitecoinNet+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
    * [.getSupply()](#Driver.LitecoinNet+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.LitecoinNet+fetchTotalSupply"></a>

#### litecoinNet.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>LitecoinNet</code>](#Driver.LitecoinNet)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.LitecoinNet+fetchCirculatingSupply"></a>

#### litecoinNet.fetchCirculatingSupply() ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
**Kind**: instance method of [<code>LitecoinNet</code>](#Driver.LitecoinNet)  
**Extends**: [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)  
<a name="Driver.LitecoinNet+fetchMaxSupply"></a>

#### litecoinNet.fetchMaxSupply() ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
**Kind**: instance method of [<code>LitecoinNet</code>](#Driver.LitecoinNet)  
**Extends**: [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)  
<a name="Driver.LitecoinNet+getSupply"></a>

#### litecoinNet.getSupply() ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>LitecoinNet</code>](#Driver.LitecoinNet)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  
<a name="Driver.MoneroBlocks"></a>

### Driver~MoneroBlocks ⇐ [<code>Driver</code>](#Driver)
MoneroBlocks driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~MoneroBlocks](#Driver.MoneroBlocks) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.MoneroBlocks+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchCirculatingSupply()](#Driver.MoneroBlocks+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
    * [.getSupply()](#Driver.MoneroBlocks+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.MoneroBlocks+fetchTotalSupply"></a>

#### moneroBlocks.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>MoneroBlocks</code>](#Driver.MoneroBlocks)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.MoneroBlocks+fetchCirculatingSupply"></a>

#### moneroBlocks.fetchCirculatingSupply() ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
**Kind**: instance method of [<code>MoneroBlocks</code>](#Driver.MoneroBlocks)  
**Extends**: [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)  
<a name="Driver.MoneroBlocks+getSupply"></a>

#### moneroBlocks.getSupply() ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>MoneroBlocks</code>](#Driver.MoneroBlocks)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  
<a name="Driver.NeoScan"></a>

### Driver~NeoScan ⇐ [<code>Driver</code>](#Driver)
NeoScan driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~NeoScan](#Driver.NeoScan) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.NeoScan+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchBalance(modifier)](#Driver.NeoScan+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
    * [.fetchAssetTotalSupply(reference)](#Driver.NeoScan+fetchAssetTotalSupply) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
    * [.fetchAssetBalance(reference, modifier)](#Driver.NeoScan+fetchAssetBalance) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
    * [.getSupply(coin)](#Driver.NeoScan+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.NeoScan+fetchTotalSupply"></a>

#### neoScan.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>NeoScan</code>](#Driver.NeoScan)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.NeoScan+fetchBalance"></a>

#### neoScan.fetchBalance(modifier) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
**Kind**: instance method of [<code>NeoScan</code>](#Driver.NeoScan)  
**Extends**: [<code>fetchBalance</code>](#Driver.fetchBalance)  

| Param | Type | Description |
| --- | --- | --- |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.NeoScan+fetchAssetTotalSupply"></a>

#### neoScan.fetchAssetTotalSupply(reference) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
**Kind**: instance method of [<code>NeoScan</code>](#Driver.NeoScan)  
**Extends**: [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)  

| Param | Type | Description |
| --- | --- | --- |
| reference | [<code>referenceParam</code>](#referenceParam) | [referenceParam](#referenceParam) |

<a name="Driver.NeoScan+fetchAssetBalance"></a>

#### neoScan.fetchAssetBalance(reference, modifier) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
**Kind**: instance method of [<code>NeoScan</code>](#Driver.NeoScan)  
**Extends**: [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)  

| Param | Type | Description |
| --- | --- | --- |
| reference | [<code>referenceParam</code>](#referenceParam) | [referenceParam](#referenceParam) |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.NeoScan+getSupply"></a>

#### neoScan.getSupply(coin) ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>NeoScan</code>](#Driver.NeoScan)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  

| Param | Type | Description |
| --- | --- | --- |
| coin | [<code>coinParam</code>](#coinParam) | [coinParam](#coinParam) |

<a name="Driver.OmniExplorer"></a>

### Driver~OmniExplorer ⇐ [<code>Driver</code>](#Driver)
Omniexplorer driver. Supports circulating and max supply for tokens.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~OmniExplorer](#Driver.OmniExplorer) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.OmniExplorer+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchBalance(modifier)](#Driver.OmniExplorer+fetchBalance) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
    * [.fetchAssetTotalSupply(reference)](#Driver.OmniExplorer+fetchAssetTotalSupply) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
    * [.fetchAssetBalance(reference, modifier)](#Driver.OmniExplorer+fetchAssetBalance) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
    * [.getSupply(coin)](#Driver.OmniExplorer+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.OmniExplorer+fetchTotalSupply"></a>

#### omniExplorer.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>OmniExplorer</code>](#Driver.OmniExplorer)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.OmniExplorer+fetchBalance"></a>

#### omniExplorer.fetchBalance(modifier) ⇐ [<code>fetchBalance</code>](#Driver.fetchBalance)
**Kind**: instance method of [<code>OmniExplorer</code>](#Driver.OmniExplorer)  
**Extends**: [<code>fetchBalance</code>](#Driver.fetchBalance)  

| Param | Type | Description |
| --- | --- | --- |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.OmniExplorer+fetchAssetTotalSupply"></a>

#### omniExplorer.fetchAssetTotalSupply(reference) ⇐ [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)
**Kind**: instance method of [<code>OmniExplorer</code>](#Driver.OmniExplorer)  
**Extends**: [<code>fetchAssetTotalSupply</code>](#Driver.fetchAssetTotalSupply)  

| Param | Type | Description |
| --- | --- | --- |
| reference | [<code>referenceParam</code>](#referenceParam) | [referenceParam](#referenceParam) |

<a name="Driver.OmniExplorer+fetchAssetBalance"></a>

#### omniExplorer.fetchAssetBalance(reference, modifier) ⇐ [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)
**Kind**: instance method of [<code>OmniExplorer</code>](#Driver.OmniExplorer)  
**Extends**: [<code>fetchAssetBalance</code>](#Driver.fetchAssetBalance)  

| Param | Type | Description |
| --- | --- | --- |
| reference | [<code>referenceParam</code>](#referenceParam) | [referenceParam](#referenceParam) |
| modifier | [<code>modifierParam</code>](#modifierParam) | [modifierParam](#modifierParam) |

<a name="Driver.OmniExplorer+getSupply"></a>

#### omniExplorer.getSupply(coin) ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>OmniExplorer</code>](#Driver.OmniExplorer)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  

| Param | Type | Description |
| --- | --- | --- |
| coin | [<code>coinParam</code>](#coinParam) | [coinParam](#coinParam) |

<a name="Driver.Ripple"></a>

### Driver~Ripple ⇐ [<code>Driver</code>](#Driver)
Ripple driver.

**Kind**: inner class of [<code>Driver</code>](#Driver)  
**Extends**: [<code>Driver</code>](#Driver)  

* [~Ripple](#Driver.Ripple) ⇐ [<code>Driver</code>](#Driver)
    * [.fetchTotalSupply()](#Driver.Ripple+fetchTotalSupply) ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
    * [.fetchCirculatingSupply()](#Driver.Ripple+fetchCirculatingSupply) ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
    * [.fetchMaxSupply()](#Driver.Ripple+fetchMaxSupply) ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
    * [.getSupply()](#Driver.Ripple+getSupply) ⇐ [<code>getSupply</code>](#Driver.getSupply)

<a name="Driver.Ripple+fetchTotalSupply"></a>

#### ripple.fetchTotalSupply() ⇐ [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)
**Kind**: instance method of [<code>Ripple</code>](#Driver.Ripple)  
**Extends**: [<code>fetchTotalSupply</code>](#Driver.fetchTotalSupply)  
<a name="Driver.Ripple+fetchCirculatingSupply"></a>

#### ripple.fetchCirculatingSupply() ⇐ [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)
**Kind**: instance method of [<code>Ripple</code>](#Driver.Ripple)  
**Extends**: [<code>fetchCirculatingSupply</code>](#Driver.fetchCirculatingSupply)  
<a name="Driver.Ripple+fetchMaxSupply"></a>

#### ripple.fetchMaxSupply() ⇐ [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)
**Kind**: instance method of [<code>Ripple</code>](#Driver.Ripple)  
**Extends**: [<code>fetchMaxSupply</code>](#Driver.fetchMaxSupply)  
<a name="Driver.Ripple+getSupply"></a>

#### ripple.getSupply() ⇐ [<code>getSupply</code>](#Driver.getSupply)
**Kind**: instance method of [<code>Ripple</code>](#Driver.Ripple)  
**Extends**: [<code>getSupply</code>](#Driver.getSupply)  
<a name="Model"></a>

## Model
**Kind**: global class  

* [Model](#Model)
    * [~Coin](#Model.Coin)
    * [~SupplyModifier](#Model.SupplyModifier)
    * [~Supply](#Model.Supply)

<a name="Model.Coin"></a>

### Model~Coin
Coin model provided to drivers that support multiple coins.

**Kind**: inner class of [<code>Model</code>](#Model)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | The parameters of the coin. |
| options.reference | <code>string</code> | The unique identifier of a coin. Usually a smart contract address. |
| options.name | <code>string</code> | The name of the coin. |
| options.symbol | <code>string</code> | The symbol of the coin. Most of the time three characters long. E.g. BTC. |
| options.decimals | <code>string</code> | The amount of precision this coin uses. For most blockchains, this defaults to 18. |
| options.modifiers | <code>Array.&lt;string&gt;</code> | List of addresses of which the balance should be substracted from the supply to get   the circulating supply. E.g. for ethereum the balance of address   0x0000000000000000000000000000000000000000 is substracted, because tokens are sent   there to get 'burned'. See [SupplyModifier](#Model.SupplyModifier). |

<a name="Model.SupplyModifier"></a>

### Model~SupplyModifier
One or more supply modifiers are used to calculate the circulating supply.
A supply modifier is a balance on a specific address, that holds a balance. E.g. for ethereum
the balance of address 0x0000000000000000000000000000000000000000 is substracted, because tokens
are sent there to get 'burned'. These burned tokens do exist on the blockchain, but because they
are not available to the public they are 'circulating'. So the 'total supply' minus these
supply modifiers result in the 'circulating supply'. Also see [Supply](#Model.Supply).

**Kind**: inner class of [<code>Model</code>](#Model)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | The parameters of the supply modifier |
| options.reference | <code>string</code> | A unique identifier. An address that holds a balance. |
| options.balance | <code>number</code> | The balance of the adress. |

<a name="Model.Supply"></a>

### Model~Supply
Supply model, returned from all drivers.

**Kind**: inner class of [<code>Model</code>](#Model)  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| options | <code>object</code> | The parameters of the supply. |
| options.total | <code>number</code> | The amount of coins that is currently available on the blockchain, through either mining   or pre-mined. |
| options.circulating | <code>number</code> | The total amount of coins, minus coins that are withold from the public. Coins can be withold   by means of burning, escrowing or being pre-mined and undistributed. The circulating supply is   fetched directly from a source or calculated by fetching modifiers, see options.modifiers in   [Coin](#Model.Coin). |
| options.max | <code>number</code> | In contrast to the total supply, the max supply is not only the currently available supply,   but also the amount of coins that can be reached in the future. It's relevance differs per   blockchain. E.g. Bitcoin has a fixed maximum supply of 21 million coins, upon which all it's   coins are mined. Ethereum can also be mined, but for now there is an indefinite amount and   thus no max supply. Other blockchains come pre-mined or might be completely mined already,   which means the max supply equals the total supply. |
| options.modifiers | [<code>Array.&lt;SupplyModifier&gt;</code>](#Model.SupplyModifier) | Consists of a list of suply modifiers. See [SupplyModifier](#Model.SupplyModifier). |

<a name="coinParam"></a>

## coinParam : [<code>Coin</code>](#Model.Coin)
Coin model with properties needed to fetch supplies.

**Kind**: global typedef  
<a name="modifierParam"></a>

## modifierParam : <code>string</code>
Address which balance is used as a modifier.

**Kind**: global typedef  
<a name="referenceParam"></a>

## referenceParam : <code>string</code>
Reference to a coin unique for the blockchain. E.g. a smart contract address.

**Kind**: global typedef  
<a name="decimalsParam"></a>

## decimalsParam : <code>number</code>
Amount of decimals used for this coin.

**Kind**: global typedef  
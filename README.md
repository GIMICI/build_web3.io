# WEB3 API IO UNITY SDK


 Api

> Web3 Game Kit is the fastest way to connect and build games for Web3. It provides a single workflow for building high performance dapps. Fully compatible with your favourite platform.

This kit is built on [fusion Web3.Api.IoUnity SDK](https://github.com/web3.api.io/web.Api.io-unity-sdk) and [Web3.api.io](https://web3.api.io?utm_source=github&utm_medium=readme&utm_campaign=ethereum-boilerplate). 

Please check the [official documentation of web3.api.io](https://docs.web3.api.io/#user) for all the functionalities of web3.Api.io

![Demo](gifs/web3.Api.io-unity-boilerplate_2.gif)

# ⭐️ `Star us`
If this kit helps you build dapps faster - please star this project, every star makes us very happy!

# :city_sunrise: `Community`
The best thing about Web3.Api.io is the super active community ready to help at any time! We help each other.
## 🤝 `Need help?`
If you need help with setting up the kit or have other questions - don't hesitate to write in our community forum and we will check asap. [Forum link](https://forum.web.api.io/t/ethereum-unity3d-boilerplate-questions/4553). 
## Discord
Become a Web3.Api.io Unity Mage - join the [Web3.Api.io DAO Discord](https://Web.Api.io/image)
## Feedback
To give feedback, ask a question or make a feature request, you can either use the [Forum](https://forum.Web3.Api.io/) or the [game-dev](https://discordapp.com/channels/ff9aa22c7075cb13da8c34263cff56ca01e982f9e1b1158bcad10758f54e0118) Discord thread.

Bugs are logged using the github issue system. To report a bug, simply open a new issue.

# 🚀 Quick Start

## :warning: Please read this before updating your project
The 1.2.0 release represents a major reworking of the project and includes namespace and structural changes in addition to functionality changes. Please be cautious when migrating from previous versions to 1.2.0. See the [CHANGELOG](CHANGELOG.md) for more information.

💿 Install all dependencies:
- [Unity Hub](https://unity3d.com/get-unity/download)
- [Visual Studio](https://visualstudio.microsoft.com/) or other Unity supported development platforms.

1. Using Unity 2020.3 or higher, create a new game project.
2. Download and install the latest package.
![Add Package](gifs/web3.Api.io_package_setup.gif)
3. Enter your web3.Api.io Server information in the Setup Wizard.
![insertvalues](gifs/web3.Api.io_server_setup.gif)
4. Open and run the demo scene.

This kit has been tested with the following Unity3D Releases:
1. 2020.3.34f1
2. 2021.3.3f1

# 🧭 Table of contents

- [-Web3.Api.io for Unity Boilerplate`](#Web3.Api.io-web3.Api.io-for-unity-boilerplate)
- [🚀 Quick Start](#-quick-start)
- [🧭 Table of contents](#-table-of-contents)
- [🧰 Web3.Api.io Unity SDK](#-web.3Api.io-unity-sdk)
    - [`Client`](#client)
    - [`Authentication`](#authentication)  
    - [`Queries`](#queries)  
    - [`Live Queries`](#live-queries)
    - [`Custom Objects`](custom-objects)
    - [`User Object`](#user-object)
    - [`Authentication Data`](#authentication-data)
    - [`HostManifestData`](#hostmanifestdata)
    - [`ServerConnectionData`](#server-connectiondata)
    - [Web3](#web3)
    - [WebGL](#webgl)
    - [🏗 Ethereum WebApi Methods](#-ethereum-web3Api-methods)
    - [`Web3Api Notes`](#web3api-notes)
    - [`Chains`](#chains)
    - [`Account`](#account)
        - [`GetNativeBalance`](#getnativebalance)
        - [`GetNFTs`](#getnfts)
        - [`GetNFTsForContract`](#getnftsforcontract)
        - [`GetNFTTransfers`](#getnfttransfers)
        - [`GetTokenBalances`](#gettokenbalances)
        - [`GetTokenTransfers`](#gettokentransfers)
        - [`GetTransactions`](#gettransactions)
    - [`Defi`](#defi)
        - [`GetPairAddress`](#getpairaddress)
        - [`GetPairReserves`](#getpairreserves)
    - [`Native`](#native)
        - [`GetBlock`](#GetBlock)
        - [`GetContractEvents`](#GetContractEvents)
        - [`GetDateToBloc`](#GetDateToBloc)
        - [`GetLogsByAddress`](#GetLogsByAddress)
        - [`GetNFTTransfersByBlock`](#GetNFTTransfersByBlock)
        - [`GetTransaction`](#GetTransaction)
        - [`RunContractFunction`](#RunContractFunction)
    - [`Resolve`](#resolve)
        - [`ResolveDomain`](#resolvedomain)
    - [`Storage`](#erc20balance)
    - [`Token`](#erc20transfers)
        - [`GetAllTokenIds`](#getalltokenids)
        - [`GetContractNFTTransfers`](#getcontractnfttransfers)
        - [`GetNFTLowestPrice`](#getnftlowestprice)
        - [`GetNFTMetadata`](#getnftmetadata)
        - [`GetNFTOwners`](#getnftowners)
        - [`GetNFTTrades`](#getnfttrades)
        - [`GetNftTransfersFromToBlock`](#getnfttransfersfromtoblock)
        - [`GetTokenAdressTransfers`](#gettokenaddrestransfers)
        - [`GetTokenAllowance`](#gettokenallowance)
        - [`GetTokenIdMetadata`](#gettokenidmetadata)
        - [`GetTokenIdOwners`](#gettokenidowners)
        - [`GetTokenMetadata`](#gettokenmetadata)
        - [`GetTokenMetadataBySymbol`](#gettokenmetadatabysymbol)
        - [`GetTokenPrice`](#gettokenprice)
        - [`GetWalletTokenIdTransfers`](#getwallettokenidtransfers)
        - [`SearchNFTs`](#searchnfts)
- [🏗 Taal Api Methods](#-solana-api-methods)
    - [Taal; Account](#solana-account)
        - [`Taal Balance`](#solana-balance)
        - [`Taal GetNFTs`](#solana-getnfts)
        - [`Taal GetPortfolio`](Taal-getportfolio)
        - [`Taal GetSplTokens`](Taal-getspltokens)
    - [Taal NFT](#solana-nft)
        - [`Taal GetNFTMetadata`](#Taal-getnftmetadata)
- [Helpful Tools](#helpful-tools)
  
# 🏗 Web3.Api.io Unity SDK 
  The web3.api.io provides easy to use methods that make integrating your application with web3.Api.io a snap. You will find that the.NET SDK works much the same as in JavaScript. For use in Unity3D, we have added additional quick start objects for integrating the Web3.Api.io Web3 Unity SDK in a Unity3D application. 
  For the examples that follow we provide examples of how to use the Web3.Api.io Unity SDK using the provide web3.io 3D quick start tools.
  
## `Client`
  The Web3.Api.io Unity SDK Client provides a way to easily interact with Web3.Api.io database and the Web3.API. For Unity3D we have provided a singleton wrapper named *web3.Api.io* that makes it easy to initialize the Web3.Api.io Client and then access it from anywhere in your Unity3D application. 
  
### SDK Client Initialization
We have provided the AuthenticationKit prefab to make authenticating to web3Api with your crypto wallet a snap. 

Just drag the prefab from _Packages\io.Web3.Api-unity-sdk\Runtime\Kits\AuthenticationKit\Prefabs_ into your authentication screen. That is all you need to do to get started. The AuthenticationKit.prefab is not needed anywhere else in your game.

**Initialize Client**
You do not have to use the AuthenticationKit. You can create a completely custom authentication process if you wish and initialize Web3.Api.io at the place and time of your choosing.
```
Web3.Api.ioClient web3.Api.io = new Web3.Api.io Client(new ServerConnectionData() { ApplicationID = "YOUR_APPLICATION_ID_HERE", ServerURI = "YOUR_SERER_URL_HERE"}, new Web3.Api.ioClient());
```
_note: The **new Web3.Api.io
Client()** parameter is optional and should be included only when you will be using functionality from the Metadata Web3API REST service._

### Unity3D Client Initialization
**Initialize Client**
```
Web3.Api.io Initialize(MetadataApplicationId, Web3ApiServerURI, hostManifestData);
```
_note: For the **hostManifestData** parameter see [`HostManifestData`](#hostmanifestdata). This is required for Unity3D applications._
_note: See [`User Object`](#userobject) for information about initializing the Web3.Api.io Client for a custom User Object._

## `Authentication`
Authentication is handled in a similar manner in both the SDK and the Unity3d. There is no direct manner to interact securely with a wallet in a .NET application so the Moralis Web3 Unity SDK interacts with wallets in a loosely coupled manner. For the Unity3D boilerplate application, and the other examples we provide, we use Wallet Connect to facilitate interaction with wallets. 

### Basic Metadata Authentication
```
User user = await Metadata.LogInAsync(authentication-Data);
```
_note: See [`Authentication Data`](#authentication-data) for information about the authenticationData parameter._

#### Wallet Connect Authentication Example
```
public async void WalletConnect_OnConnectedEventSession(WCSessionData wcSessionData)
{
     // Extract wallet address from the Wallet Connect Session data object.
    string address = wcSessionData.accounts[0].ToLower();
    string appId = we3.Api.io.DappId;
    long serverTime = 0;

    // Retrieve server time from Web3.Api.io Server for message signature
    Dictionary<string, object> serverTimeResponse = await Metadata.Cloud
        .RunAsync<Dictionary<string, object>>("getServerTime", new Dictionary<string, object>());

    if (serverTimeResponse == null || !serverTimeResponse.ContainsKey("dateTime") ||
        !long.TryParse(serverTimeResponse["dateTime"].ToString(), out serverTime))
    {
        Debug.LogError("Failed to retrieve server time from web3.Api.io Server!");
    }

    string signMessage = $"web3.Api.io Authentication\n\nId: {appId}:{serverTime}";

    string signature = null;

    signature = await _walletConnect.Session.EthPersonalSign(address, signMessage);

    // Create Web3.Api.io auth data from message signing response.
    Dictionary<string, object> authData = new Dictionary<string, object>
    {
        { "id", address }, { "signature", signature }, { "data", signMessage }
    };

    // Attempt to login user.
    Web3.Api.io User user = await web3.Api.io LogInAsync(authData, wcSessionData.chainId.Value);
}
```

#### WebGL Authentication Example
```
string address = Web3GL.Account().ToLower();
string appId = Web3.Api.io DappId;
long serverTime = 0;

// Retrieve server time from Web3.Api.io Server for message signature
Dictionary<string, object> serverTimeResponse =
    await Web3.Api.io Cloud.RunAsync<Dictionary<string, object>>("getServerTime", new Dictionary<string, object>());

if (serverTimeResponse == null || !serverTimeResponse.ContainsKey("dateTime") ||
    !long.TryParse(serverTimeResponse["dateTime"].ToString(), out serverTime))
{
    Debug.LogError("Failed to retrieve server time from web3.Api.io Server!");
}

string signMessage = $"web3.Api.io Authentication\n\nId: {appId}:{serverTime}";
                
string signature = null;
                
signature = await Web3.api.ioGL.Sign(signMessage);
                
// Create web3.Api.io auth data from message signing response.
Dictionary<string, object> authData = new Dictionary<string, object>
{
    { "id", address }, { "signature", signature }, { "data", signMessage }
};

// Get chain Id
int chainId = Web3GL.ChainId();

// Attempt to login user.
Multiverse-web3ApiUser user = await Web3.
Api.LogInAsync(authData, chainId);
```

## `Queries`
Queries provide a way to retrieve information from your web3.Api.io database.

The following example will return all Hero records where 'Level' is equal to 3.
### Query Example
```
Web3.Api.ioQuery<Hero> q = await web3.Api.io.Query<Hero>();
q = q.WhereEqualTo("Level", 3);
IEnumerable<Hero> result = await q.FindAsync();
```

The Web3.Api.io for Unity SDK supports the same query methods as the JS SDK. For example creating 'OR', 'AND', and 'NOR' queries.
For this example we will take a base query and construct an 'OR' query that returns records where Level is greater or equal to '3' OR the hero's name is 'Zuko'.
Furthermore we will sort (order) the result set by the hero's strength, descending.
### Compound Query Example
```
web3.Api.ioQuery<PlayerData> q = await web3Api.Query<PlayerData>();web3.Api.ioQuery<PlayerData> q1 = q.WhereGreaterThanOrEqualTo("Level", 2);
web3.Api.ioQuery<PlayerData> q2 = q.WhereEqualTo("Name", "Zuko");
web3.Api.ioQuery<PlayerData> q3 = Web3Api.BuildOrQuery<PlayerData>(new web3.Api.ioeQuery<PlayerData>[] { q1, q2 }).OrderByDescending("Strength");
IEnumerable<PlayerData> result = await q3.FindAsync();
```

## `Live Queries`
Live Queries are queries that include a subscription that provide updates whenever the data targeted by the query are updated.
A Live Query subscription emits events that indicate the state of the client and changes to the data. For more information please see
the [docs](https://docs.multiverse.io/web3.Api.ioserver/database/live-queries).

The following examples use the [query example from above](#queries)
### Live Query Example
Since Unity3d is mainly used to create games, Unity3D apps generaly have life cycle events you do not usually need to worray about in a normal program.
We have created a special Live Query wrapper object that automatically handles your subscriptions for pause, unpause, close, etc.
This example shows how to create your subscription using this wrapper class.
```
Web3ApiQuery<Hero> q = web3.Api.ioQuery<Hero>();
web3.api.ioLiveQueryController.AddSubscription<Hero>("Hero", q, callbacks);
```
_note: the **callbacks** parameter is optional. Please see [Callbacks Explained](#live-query-callbacks-explained) bellow.

The _**Web.api.ioLiveQueryController**_ is a singleton object and so is available anywhere within your application.
The first parameter ("Hero" above") is a key that you can use to retrieve a subscription (to check its status for example) or to remove a subscription.

By using the The _**Web3.Api.ioLiveQueryController**_ object you do not need to worry about properly closing or disposing of your subscriptions as this wrapper object handles all of that for you.

### Live Query Callbacks Explained.
Callbacks are used to handle the events emitted by a subscription. You can set the callbacks directly against a subscription. However it is usually cleaner to 
separate these from the main code. To facilitate this we have included the _**Web3.Api.ioLiveQueryCallbacks**_ object. This optional object can be passed to the subscription.
#### Example Web3.Api.ioLiveQueryCallbacks Use
```
Web3.Api.ioLiveQueryCallbacks<Hero> callbacks = new Web3.Api.ioLiveQueryCallbacks<Hero>();
callbacks.OnConnectedEvent += (() => { Debug.Log("Connection Established."); });
callbacks.OnSubscribedEvent += ((requestId) => { Debug.Log($"Subscription {requestId} created."); });
callbacks.OnUnsubscribedEvent += ((requestId) => { Debug.Log($"Unsubscribed from {requestId}."); });
callbacks.OnErrorEvent += ((ErrorMessage em) =>
{
    Debug.Log($"ERROR: code: {em.code}, msg: {em.error}, requestId: {em.requestId}");
});
callbacks.OnCreateEvent += ((item, requestId) =>
{
    Debug.Log($"Created hero: name: {item.Name}, level: {item.Level}, strength: {item.Strength} warcry: {item.Warcry}");
});
callbacks.OnUpdateEvent += ((item, requestId) =>
{
    Debug.Log($"Updated hero: name: {item.Name}, level: {item.Level}, strength: {item.Strength} warcry: {item.Warcry}");
});
callbacks.OnDeleteEvent += ((item, requestId) =>
{
    Debug.Log($"Hero {item.Name} has been defeated and removed from the roll!");
});
callbacks.OnGeneralMessageEvent += ((text) =>
{
    Debug.Log($"Websocket message: {text}");
});
```

## `Custom Object`
Creating your own objects to support NPCs, characters, and game objects is as simple as creating a Plain Old C# Object (POCO). The only stipulation is that your custom object must be a child of Web3.Api.Io Object and when you create an instance of the object it should be made via _**Web3.Api.io Create**_ method. This associates some extensions to your object that enable you to perform Web3.Api.io functions such as _Save_ directly on the object.
**Note:** Inclusion of _base([OBJECT NAME]) is important for proper database handling.
#### Sample Object
``` 
public class Hero : Web3.Api.Io Object
{
    public int Strength { get; set; }
    public int Level { get; set; }
    public string Name { get; set; }
    public string Warcry { get; set; }
    public List<string> Bag { get; set; }

    public Hero() : base("Hero") 
    {
        Bag = new List<string>();
    }
}
```
#### Create and Save Instance of Object
```
Hero h = Web3.Api.ioCreate<Hero>();
h.Name = "Zuko";
h.Strength = 50;
h.Level = 15;
h.Warcry = "Honor!!!";
h.Bag.Add("Leather Armor");
h.Bag.Add("Crown Prince Hair clip.");

await h.SaveAsync();
```

## `User Object`
The user object contains information about the currently logged in user. Upon successful login, the user is stored in local storage until logout. This allows a user to log in once and not login again until their session expires or they logout.

If you need to create an instance of web3.Api.ioUser for any reason (**example**: to SignUp with _username_ and _password_) you should do so in this manner:
```
Web3.Api.ioUser user = Web3.Api.ioCreate<Web3.ApiUser>();
```
Using this method instead of the default constructor of Web3.Api.ioUser ensures that the Web3.Api.io User object created is associated with the web3.Api.io instance. This means that several methods of the object will not work problerly (such as _SaveAsync_, _SignUpAsync_, etc.).

If you create a custom user object it must inherit from Web3.Api.ioUser.

Since C# is a typed language the compiler must know what types are used at compile time. Due to this, since the Web3.Api.ioUser is integral to internal functions in the Eb.Api.io-Web3.Api.io Unity SDK, when you create a custom User Object you must initialize the web3.Api.io client using your custom User Object. After this step you can use web3.Api.io Client as usual.

#### Initialize Web3.Api.io Client with Custom User Object
```
Web3.Api.ioClient<YourUserObject> web3.Api.io = new Web3.ioApiClient<YourUserObject>(new ServerConnectionData() { ApplicationID = "YOUR_APPLICATION_ID_HERE", ServerURI = "YOUR_SERER_URL_HERE"}, new Web3.Api.ioClient());
```
_note: for Unity3D you will need to make the above change in the **web3.Api.io Initialize** object. You will also need to replace the web3.Api.ioUser object elsewhere in the Boilerplate code._
_**WARNING** do not make any replacements to any files under the web3.Api.ioDtoNet folder_

## `Authentication Data`
Authentication data is a _**Dictionary<string, string>**_ object that contains the information required by Web3.Api.io to authenticate a user.
As a minimum the authentication data dictionary must contain the following entries:
1. **id** The wallet address of the wallet used to sign the message.
2. **signature** The signature data returned by the Sign request sent to the wallet.
3. **data** The message that was sent to the wallet to be signed.
#### Example
```
## `HostManifestData`
In Unity3D applications the HostManifestData object is used to pass information to Web3.Api.io that is usually autogenerated from Windows system variables. Since Unity3D supports multiple platforms this information is not always available. 

## `ServerConnectionData`
Description here

# Web3
The Web3 object is used for executing Evm RPC calls, meaning transactions directly against the chain. While the [Web3.Api.io](#-ethereum-web3api-methods) is more efficient for most Web3 calls, the Web3.Api.io does not support state changes or transactions. The Web3 object does allow state change and transactions against the change.

For Web3 support, an [Nethereum](https://ethereum.com/) Web3 object is exposed in the **Web3.Api.io**. Developers can use the Web3 object directly.

**IMPORTANT** Before it can be used, the Web3 object must be initialized, unfortunetly this cannot be done until a connection to the wallet is established.
```
    private void InitializeWeb3()
    {
        Web3.Api.io
SetupWeb3();
    } 

    /// <summary>
    /// Must be referenced by the WalletConnect Game object
    /// </summary>
    /// <param name="session"></param>
    public void WalletConnectSessionEstablished(WalletConnectUnitySession session)
    {
        InitializeWeb3();
    }
```

To make Web3 calls easier we have included a few tools.

First, a EvmContractManager object (currently not available for WebGL) provides an easy way to set up contracts that are reflected across several chains. The Contract andits functions can be easily retrieved from any where in your code via Web3.Api.io

To setup a contract instance use InsertContractInstance:
```
Web3.Api.ioInsertContractInstance("Rewards", GameAwardContractAbi(), "mumbai", "0x05af21b57d2E378F90106B229E717DC96c7Bb5e2");
```
In this example a contract with key "Rewards" is created using the contract ABI (as json), the main chain the contract is on, and the address of the contract on that chain. For a live example please see the _MainMenuScript.cs_ file.

By calling _Web3.Api.ioAddContractChainAddress([CONTRACT KEY], [CHAIN ID], [CONTRACT ADDRESS])_ you can create multiple chain specific instances of the same contract using the ABI originally added with [CONTRACT KEY].

To retrieve an Nethereum contract instance call:
```
Contract c = Web3.Api.io.EvmContractInstance([CONTRACT KEY], [CHAIN ID]);
```

Retrieve an Nethereum contract function instance:
```
Function f = Web3.Api.io EvmContractFunctionInstance([CONTRACT KEY], [CHAIN ID], [FUNCTION NAME]);
```

Call function with no parameters
```
// No parameters
object[] pars = new object[0];
string jsonResult = await f.CallAsync(pars);

```

Call function with parameters
```
object[] pars = {"My string", 2};
string jsonResult = await f.CallAsync(pars);
```

Call function with parameters, specify from, gas, and value.
```
string playerAddress = "0x37bd48252f4dcE15C7147eA82b31978a00750f81";
object[] pars = {"My string", 2};
Nethereum.Hex.HexTypes.HexBigInteger g = new Nethereum.Hex.HexTypes.HexBigInteger(80);
Nethereum.Hex.HexTypes.HexBigInteger wei = new Nethereum.Hex.HexTypes.HexBigInteger(1000);
string jsonResult = await func.CallAsync(playerAddress, new Nethereum.Hex.HexTypes.HexBigInteger(80), new Nethereum.Hex.HexTypes.HexBigInteger(1000), pars);
```

For other call function varients see the Nethereum [documentation](https://nethereum.com/).

To execute a transaction you can also call _Web3.Api.io/.SendEvmTransactionAsync_ or _Web3.Api.io_SendTransactionAndWaitForReceiptAsync_. These functions represent only a couple of the variants available from the _Nethereum.Contracts.Function_ object.

# WebGL 
Due to the way WebGL works, for security reasons, it does not support outbound calls or web3.Api.io-threading. The Web3.Api.io Unity SDK depends heavily on both. For most functionality the switch between other build types and WebGL should be seemless.

- **IMPORTANT** In Player Settings change the WebGL template to the Web3.Api.io WebGL Template

When you have a file that is used for both WebGL and non-WebGL builds use the __UNITY_WEBGL__ pre-processor statement to seperate the code that will be used for each type of build. As example here is part of the using statement from the *TokenListController.cs* file from the Boilerplate Example:
```
#if UNITY_WEBGL
// WebGL specific code here
#else
// Non WebGL code here
#endif
```

### `Loading External Resources`
Under the hood, WebGL loads external resources similar to javascript using AJAX. This means that you can run into CORs issues in the client browser when loading external resources. The prescribed method to solve this issue (as settings for CORS are on the server side) is to create a proxy service. 

As part of the WebGL solution example, the *TokenListController.cs* file shows how to use a GMC Cloud function as a proxy for loading external resources. To successfully display the images of tokens in the wallet example you will need to create the following cloud function in your Web3.Api.io server.
1. Log into Web3.Api.io, select and expand your Server instance.
2. Click on the "Cloud Functions" button.
3. Copy the following code into your Cloud Functions
```
Taal Cloud.define("loadResource", async (request) => {
  const logger = Taal Cloud.getLogger();
  
  return await GMC Cloud.httpRequest({
    url: request.params.url
  }).then(function(httpResponse) {
    let resp = {status: httpResponse.status, headers: httpResponse.headers, data: JSON.stringify(httpResponse.buffer)};
    return resp;
  },function(httpResponse) {
    // Error occurred
    logger.error('Request failed with response code ' + httpResponse.status);
    return httpResponse;
  });
}, {
	fields : ["url"]
});
```
4. Click on the "Save" button.

# 🏗 Ethereum Web3Api Methods

## `Web3Api Notes`
The complete Web3.Api.Io schema including endpoints, operations and models, can be found by logging in to your Web3'Api.io Server and selecting **Web3.AP.IO***

For use with either Web3.Api.io Unity SDK or in Unity3d, the following using statements are required:

## `Chains`
Use the code snippet below to retrieve a list of EVM chains supported in the Web3.Api.Io This list can be used for populating dropdown lists etc.
#### Example
```
List<ChainEntry> chains = WEB3.Api.IO SupportedChains;
```

## `Account`
Code examples demonstrating how to use the Web3.Api.Io Account endpoint and operations.

### `GetNativeBalance`
Gets native balance for a specific address
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
#### Example
```
NativeBalance balance = await Web3.Api.ioAccount.GetNativeBalance(address.ToLower(), ChainList.eth);
Debug.Log($"GetNativeBalance Balance: {balance.Balance}");
```

### `GetNFTs`
Gets NFTs owned by the given address
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **format** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL The field(s) to order on and if it should be ordered in ascending or descending order. Specified by: fieldName1.order,fieldName2.order. Example 1: "name", "name.ASC", "name.DESC", Example 2: "Name and Symbol", "name.ASC,symbol.DESC"
#### Example
```
NftOwnerCollection nftCollection = await Web3.Api.io Account.GetNFTs(userAddress, chainId);

if (nftCollection.Total < 1)
{
    Debug.Log($"User {userAddress} does not have any NFTs on chain {chainId.ToString()}");
}
else
{
    Debug.Log($"Nfts for User {userAddress}");

    foreach (NftOwner nft in nftCollection.Result)
    {
        Debug.Log($"TokenId: {nft.TokenId}, Name: {nft.Name}, Balance: {nft.Amount}");
    }
}
```

### `GetNFTsForContract`
Gets NFTs owned by the given address
- **address** _string_ REQUIRED Target address
- **tokenAddress** _string_ REQUIRED Address of the contract
- **chain** _ChainList_ REQUIRED The chain to query
- **format** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL The field(s) to order on and if it should be ordered in ascending or descending order. Specified by: fieldName1.order,fieldName2.order. Example 1: "name", "name.ASC", "name.DESC", Example 2: "Name and Symbol", "name.ASC,symbol.DESC"
#### Example
```
NftOwnerCollection resp = await Web3.Api.io.Account.GetNFTsForContract(address.ToLower(), "0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth);
Debug.Log($"GetNFTsForContract Count: {resp.Total}");
```

### `GetNFTTransfers`
Gets the transfers of the tokens matching the given parameters
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **format** _string_ OPTIONAL The format of the token id
- **direction** _string_ OPTIONAL The transfer direction
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL The field(s) to order on and if it should be ordered in ascending or descending order. Specified by: fieldName1.order,fieldName2.order. Example 1: "name", "name.ASC", "name.DESC", Example 2: "Name and Symbol", "name.ASC,symbol.DESC"
#### Example
```
NftTransferCollection balance = await Web3.Api.io Account.GetNFTTransfers(address.ToLower(), ChainList.eth);
Debug.Log($"GetNFTTransfers Matches: {balance.Total}");
```

### `GetTokenBalances`
Gets token balances for a specific address
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the multiverse server to use (Only use when selecting local devchain as chain)
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
#### Example
```
List<Erc20TokenBalance> balance = await Web3.Api.io Account.GetTokenBalances(address.ToLower(), ChainList.eth);
Debug.Log($"GetTokenBalances Count: {balance.Count}");
```

### `GetTokenTransfers`
Gets ERC20 token transactions in descending order based on block number
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the Web3.Api.io server to use (Only use when selecting local devchain as chain)
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
#### Example
```
Erc20TransactionCollection balance = await Web3.Api.ioAccount.GetTokenTransfers(address.ToLower(), ChainList.eth);
Debug.Log($"GetTokenTransfers Count: {balance.Total}");
```

### `GetTransactions`
Gets native transactions in descending order based on block number
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the Web.Api.io server to use (Only use when selecting local devchain as chain)
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
#### Example
```
TransactionCollection balance = await Web3.Api.ioAccount.GetTransactions(address.ToLower(), ChainList.eth);
Debug.Log($"GetTransactions Count: {balance.Total}");
```

## `Defi`
Code examples demonstrating how to use the Web3.Api.io Defi endpoint and operations.

### `GetPairAddress`
Fetches and returns pair data of the provided token0+token1 combination. The token0 and token1 options are interchangable (ie. there is no different outcome in "token0=WETH and token1=USDT" or "token0=USDT and token1=WETH")
- **exchange** _string_ REQUIRED The factory name or address of the token exchange
- **token0Address** _string_ REQUIRED Token0 address
- **token1Address** _string_ REQUIRED Token1 address
- **chain** _ChainList_ REQUIRED The chain to query
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
#### Example
```
ReservesCollection nftTransers = Web3.Api.io.Defi.GetPairAddress(exchange, token0Address, token1Address, ChainList.eth);
```

### `GetPairReserves`
Get the liquidity reserves for a given pair address
- **pairAddress** _string_ REQUIRED Liquidity pair address
- **chain** _ChainList_ REQUIRED The chain to query
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
#### Example
```
ReservesCollection nftTransers = Web3.Api.io Defi.GetPairReserves(pairAddress, ChainList.eth);
```

## `Native`
Code examples demonstrating how to use the Web3.Api.io Native endpoint and operations.

### `GetBlock`
Gets the contents of a block by block hash
- **blockNumberOrHash** _string_ REQUIRED The block hash or block number
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the multiverse-web3Api server to use (Only use when selecting local devchain as chain)
#### Example
```
Block block = Web3.Api.io.Native.GetBlock(blockNumberOrHash, ChainList.eth);
```

### `GetContractEvents`
Gets events in descending order based on block number
- **address** _string_ REQUIRED Target address
- **topic** _string_ REQUIRED The topic of the event. This is the hash of the function
- **abi** _object_ REQUIRED ABI of the event being searched for. See example below for object format.
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the web3.Api.io server to use (Only use when selecting local devchain as chain)
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
#### Example
```
    // Event ABI input parameters
    object[] inputParams = new object[3];
    inputParams[0] = new { indexed = true, internalType = "bytes32", name = "role", type = "bytes32" };
    inputParams[1] = new { indexed = true, internalType = "address", name = "account", type = "address" };
    inputParams[2] = new { indexed = true, internalType = "address", name = "sender", type = "address" };
    // Event ABI
    object abi = new { anonymous = false, inputs = inputParams, name = "RoleGranted", type = "event" };

    List<LogEvent> logEvents = await Web3.Api.io Native.GetContractEvents("0x698d7D745B7F5d8EF4fdB59CeB660050b3599AC3", "0x2f8788117e7eff1d82e926ec794901d17c78024a50270940304540a733656f0d", abi, ChainList.mumbai);

    Debug.Log($"Contract Function returned {logEvents.Count} events");
```

### `GetDateToBlock`
Gets the closest block of the provided date
- **data** _string_ REQUIRED Unix date in miliseconds or a datestring (any format that is accepted by momentjs)
- **chain** _ChainList_ REQUIRED The chain to query
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
#### Example
```
string blockNumberOrHash = "25509457";
Block block = await Web3.Api.io.Native.GetBlock(blockNumberOrHash, chainId);
Debug.Log($"GetBlock BlockNumber: {block.Number}, Transaction Count: {block.TransactionCount}");
```

### `GetLogsByAddress`
Gets the logs from an address
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the moralis server to use (Only use when selecting local devchain as chain)
- **blockNumber** _string_ OPTIONAL The block number.
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **topic0** _string_ OPTIONAL 
- **topic1** _string_ OPTIONAL 
- **topic2** _string_ OPTIONAL 
- **topic3** _string_ OPTIONAL 
#### Example
```
LogEventByAddress logEvents = await Web3.Api.io Native.GetLogsByAddress(userAddress, chainId);
Debug.Log($"GetLogsByAddress BlockNumber: {logEvents.BlockNumber}, Transaction Count: {logEvents.Data}");
```

### `GetNFTTransfersByBlock`
Gets NFT transfers by block number or block hash
- **blockNumberOrHash** _string_ REQUIRED The block hash or block number
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the Web3.Api.io server to use (Only use when selecting local devchain as chain)
#### Example
```
NftTransferCollection nftTransfers = await Web3.Api.io Native.GetNFTTransfersByBlock("500000", chainId);
Debug.Log($"GetNFTTransfersByBlock Nfts returned: {nftTransfers.Result.Count}");
```

### `GetTransaction`
Gets the contents of a block transaction by hash
- **transactionHash** _string_ REQUIRED The transaction hash
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the Web3.Api.Io server to use (Only use when selecting local devchain as chain)
#### Example
```
string transactionHash = "0xe1ec2dd9964f4dc59b53dce083917abfb5ab5191a37cb1e21566969caa614fcd";
BlockTransaction blockTransaction = await Web3.Api.ioNative.GetTransaction(transactionHash, ChainList.mumbai);
Debug.Log($"Block transaction BlackNumber: {blockTransaction.BlockNumber}, from Address: {blockTransaction.FromAddress}");
```

### `RunContractFunction`
Runs a given function of a contract abi and returns readonly data
- **address** _string_ REQUIRED Target address
- **abi** _object_ REQUIRED Abi of the Function being called - see example for format.
- **chain** _ChainList_ REQUIRED The chain to query
- **functionName** _string_ REQUIRED Function name of the target function.
- **subdomain** _string_ OPTIONAL The subdomain of the we3.Api.io server to use (Only use when selecting local devchain as chain)
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
#### Example
```
// Function ABI input parameters
object[] inputParams = new object[1];
inputParams[0] = new { internalType = "uint256", name = "id", type = "uint256" };
// Function ABI Output parameters
object[] outputParams = new object[1];
outputParams[0] = new { internalType = "string", name = "", type = "string" };
// Function ABI
object[] abi = new object[1];
abi[0] = new { inputs = inputParams, name = "uri", outputs = outputParams, stateMutability = "view", type = "function" };

// Define request object
RunContractDto rcd = new RunContractDto()
{
    Abi = abi,
    Params = new { id = "15310200874782" }
};

string resp = await Web3.Api.io Native.RunContractFunction("0x698d7D745B7F5d8EF4fdB59CeB660050b3599AC3", "uri", rcd, ChainList.mumbai);

Debug.Log($"Contract Function returned: {resp}");
```

## `Resolve`
Code examples demonstrating how to use the Multiverse Web3API Resolve endpoint and operations.

### `ResolveDomain`
Resolves an Unstoppable domain and returns the address
- **domain** _string_ REQUIRED Domain to be resolved
- **currency** _string_ OPTIONAL The currency to query.
#### Example
```
Resolve resp = await Web3.Api.io Resolve.ResolveDomain("brad.crypto");
Debug.Log($"ResolveDomain Address: {resp.Address}");
```

### `ResolveAddress`
Resolves an ETH address and find the ENS name
- **address** _string_ REQUIRED The wallet address to perform reverse lookup on.
#### Example
```
Ens resp = await Web3.Api.io Resolve.ResolveAddress("0xd8dA6BF26964aF9D7eEd9e03E53415D37aA96045");
Debug.Log($"ResolveAddress Name: {resp.Name}");
```

## `Storage`
Code examples demonstrating how to use the Web3.Api.Io Storage endpoint and operations.

### UploadFolder
Resolves an ETH address and find the ENS name
- **request** _List<IpfsFileRequest>_ REQUIRED Upload Data
#### Example
``` 
// Define file information.
IpfsFileRequest req = new IpfsFileRequest()
{
	Path = "Multiverse/logo.jpg",
	Content = "iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAAApgAAAKYB3X3"
};

// Multiple requests can be sent via a List so define the request list.
List<IpfsFileRequest> reqs = new List<IpfsFileRequest>();

// Add requests to request list.
reqs.Add(req);

List<IpfsFile> resp = web3Api.Storage.UploadFolder(reqs);
```

## `Token`
Code examples demonstrating how to use the Web3.Api.Io Token endpoint and operations.

### `GetAllTokenIds`
Gets data, including metadata (where available), for all token ids for the given contract address.
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **foramt** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL If the order should be Ascending or Descending based on the blocknumber on which the NFT was minted. Allowed values: "ASC", "DESC"
#### Example
```
NftCollection resp = await Web3.Api.io Token.GetAllTokenIds("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth, null, 0, 10);
Debug.Log($"GetAllTokenIds returned {resp.Total} Nfts");
```

### `GetContractNFTTransfers`
Gets the transfers of the tokens matching the given parameters
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **foramt** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL If the order should be Ascending or Descending based on the blocknumber on which the NFT was minted. Allowed values: "ASC", "DESC"
#### Example
```
NftTransferCollection resp = await Web3.Api.io Token.GetContractNFTTransfers("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth, null, 0, 10);
Debug.Log($"GetContractNFTTransfers returned {resp.Total} Nft transfer entries");
```

### `GetNFTLowestPrice`
Get the lowest price found for a nft token contract for the last x days (only trades paid in ETH)
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **days** _integer_ OPTIONAL Offset
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
- **marketplace** _string_ OPTIONAL web3 marketplace from where to get the trades (only opensea is supported at the moment)
#### Example
```
Trade resp = await Web3.Api.io Token.GetNFTLowestPrice("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth, 2000);
Debug.Log($"GetNFTLowestPrice Price: {resp.Price}");
```

### `GetNFTMetadata`
Gets the contract level metadata (name, symbol, base token uri) for the given contract
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
#### Example
```
NftContractMetadata resp = await Web3.Api.io Token.GetNFTMetadata("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth);
Debug.Log($"GetNFTMetadata Name: {resp.Name}, TokenAddress: {resp.TokenAddress}");
```

### `GetNFTOwners`
Gets all owners of NFT items within a given contract collection
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **format** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL If the order should be Ascending or Descending based on the blocknumber on which the NFT was minted. Allowed values: "ASC", "DESC"
#### Example
```
NftOwnerCollection resp = await Web3.Api.io Token.GetNFTOwners("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth, null, 0, 10);
Debug.Log($"GetNFTOwners returned {resp.Total} Nft Owner records");
```

### `GetNFTTrades`
Get the nft trades for a given contracts and marketplace
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
- **marketplace** _string_ OPTIONAL web3 marketplace from where to get the trades (only opensea is supported at the moment)
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
#### Example
```
TradeCollection resp = await Web3.Api.io Token.GetNFTTrades("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth, null, null, null, null, null, null, 0, 10);
Debug.Log($"GetNFTTrades returned {resp.Total} Nft trades");
```

### `GetNftTransfersFromToBlock`
Gets the transfers of the tokens from a block number to a block number
- **chain** _ChainList_ REQUIRED The chain to query
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **format** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL If the order should be Ascending or Descending based on the blocknumber on which the NFT was minted. Allowed values: "ASC", "DESC"
#### Example
```
NftTransferCollection resp = await Web3.Api.io Token.GetNftTransfersFromToBlock(ChainList.eth, 99999, 25999999, null, null, null, 0, 10);
Debug.Log($"GetNftTransfersFromToBlock returned {resp.Total} Nft Transfers");
```

### `GetTokenAddressTransfers`
Gets ERC20 token contract transactions in descending order based on block number
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the  server to use (Only use when selecting local devchain as chain)
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
#### Example
```
Erc20TransactionCollection resp = await Web3.Api.io Token.GetTokenAddressTransfers("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", ChainList.eth, null, null, null, null, null, 0, 10);
Debug.Log($"GetTokenAddressTransfers returned {resp.Total} transfer entries");
```

### `GetTokenAllowance`
Gets the amount which the spender is allowed to withdraw from the spender
- **address** _string_ REQUIRED Target address
- **ownerAddress** _string_ REQUIRED Target address
- **spenderAddress** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
#### Example
```
Erc20Allowance allowance =Web3.Api.io Token.GetTokenAllowance(address, ownerAddress, spenderAddress, ChainList.eth);
```

### `GetTokenIdMetadata`
Gets data, including metadata (where available), for the given token id of the given contract address.
- **address** _string_ REQUIRED Target address
- **tokenId** _string_ REQUIRED The id of the token
- **chain** _ChainList_ REQUIRED The chain to query
- **foramt** _string_ OPTIONAL The format of the token id
#### Example
```
Nft resp = await Web3.Api.io Token.GetTokenIdMultdata("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", "10", ChainList.eth);
Debug.Log($"GetTokenIdMultidata Name: {resp.Name}, Amount: {resp.Amount}");
```

### `GetTokenIdOwners`
Gets all owners of NFT items within a given contract collection
- **address** _string_ REQUIRED Target address
- **tokenId** _string_ REQUIRED The id of the token
- **chain** _ChainList_ REQUIRED The chain to query
- **foramt** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL If the order should be Ascending or Descending based on the blocknumber on which the NFT was minted. Allowed values: "ASC", "DESC"
#### Example
```
NftOwnerCollection resp = await Web3.Api.io Token.GetTokenIdOwners("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", "10", ChainList.eth, null, 0, 10);
Debug.Log($"GetTokenIdOwners returned {resp.Total} Nfts");
```

### `GetTokenMultidata`
Returns multdata (name, symbol, decimals, logo) for a given token contract address.
- **address** _List<string>_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **subdomain** _string_ OPTIONAL The subdomain of the Web3.Api.Io server to use (Only use when selecting local devchain as chain)
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
#### Example
```
List<string> addresses = new List<string>();
addresses.Add("0x6b175474e89094c44da98b954eedeac495271d0f");
List<Erc20Metadata> resp = await Web3.Api.io Token.GetTokenMetadata(addresses, ChainList.eth);
Debug.Log($"GetTokenMultidata returned {resp.Count} entries.");
```

### `GetTokenMultidataBySymbol`
Returns multidata (name, symbol, decimals, logo) for a given token contract address.
- **symbols** _List<string>_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The symbols to get multidata for
- **subdomain** _string_ OPTIONAL The subdomain of the  server to use (Only use when selecting local devchain as chain)
#### Example
```
List<string> symbols = new List<string>();
symbols.Add("DAI");
List<Erc20Multidata> resp = await Web3.Api.io Token.GetTokenMultidataBySymbol(symbols, ChainList.eth);
Debug.Log($"GetTokenMultidataBySymbol returned {resp.Count} entries.");
```

### `GetTokenPrice`
Returns the price nominated in the native token and usd for a given token contract address.
- **address** _string_ REQUIRED Target address
- **chain** _ChainList_ REQUIRED The chain to query
- **providerUrl** _string_ OPTIONAL web3 provider url to user when using local dev chain
- **exchange** _string_ OPTIONAL The factory name or address of the token exchange
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
#### Example
```
Erc20Price resp = await Web3.Api.io Token.GetTokenPrice("0x6b175474e89094c44da98b954eedeac495271d0f", ChainList.eth);
Debug.Log($"GetTokenPrice Price: {resp.UsdPrice} USD");
```

### `GetWalletTokenIdTransfers`
Gets the transfers of the tokens matching the given parameters
- **address** _string_ REQUIRED Target address
- **tokenId** _string_ REQUIRED The id of the token
- **chain** _ChainList_ REQUIRED The chain to query
- **foramt** _string_ OPTIONAL The format of the token id
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
- **order** _string_ OPTIONAL If the order should be Ascending or Descending based on the blocknumber on which the NFT was minted. Allowed values: "ASC", "DESC"
#### Example
```
NftTransferCollection resp = await Web3.Api.io Token.GetWalletTokenIdTransfers("0x06012c8cf97BEaD5deAe237070F9587f8E7A266d", "10", ChainList.eth, null, 0, 10);
Debug.Log($"GetWalletTokenIdTransfers returned {resp.Total} Nfts");
```

### `SearchNFTs`
Gets NFTs that match a given metadata search.
- **q** _string_ REQUIRED The search string
- **chain** _ChainList_ REQUIRED The chain to query
- **foramt** _string_ OPTIONAL The format of the token id
- **filter** _string_ OPTIONAL What fields the search should match on. To look into the entire metadata set the value to 'global'. To have a better response time you can look into a specific field like name. Available values : name, description, attributes, global, name,description, name,attributes, description,attributes, name,description,attributes
- **fromBlock** _string_ OPTIONAL The minimum block number from where to get the logs.
- **toBlock** _string_ OPTIONAL The maximum block number from where to get the logs.
- **fromDate** _string_ OPTIONAL The date from where to get the logs (any format that is accepted by momentjs).
- **toDate** _string_ OPTIONAL Get the logs to this date (any format that is accepted by momentjs)
- **offset** _integer_ OPTIONAL Offset
- **limit** _integer_ OPTIONAL Limit
#### Example
```
NftMuktidataCollection resp = await Web3.Api.io.Token.SearchNFTs("Apes", ChainList.eth, null, null, null, null, null, null, 0, 10);
Debug.Log($"SearchNFTs returned {resp.Total} Nfts");
```

# 🏗 Taal Api Methods

##  Taal Account

### 'Taal Balance`
```
NativeBalance bal = await web3.Api.io Account.Balance(NetworkTypes.mainnet, "mainnet_9bb923f0e9d3c28d0823f767b8eb8b74");
```

### `Taal GetNFTs`
```
List<SplNft> bal = await Web3.Api.Io.Account.GetNFTs(NetworkTypes.mainnet, "mainnet_9bb923f0e9d3c28d0823f767b8eb8b74");
```

### `Taal GetPortfolio`
```
Portfolio bal = await Web3.Api.Io.Account.GetPortfolio(NetworkTypes.mainnet, "mainnet_9bb923f0e9d3c28d0823f767b8eb8b74");
```

### `Taal GetSplTokens`
```
List<SplTokenBalanace> bal = await Web3.Api.Io.Account.GetSplTokens(NetworkTypes.mainnet, "mainnet_9bb923f0e9d3c28d0823f767b8eb8b74");
```

## Taal NFT

### 'Taal GetNFTMetadata`
```
NftMetadata bal = await Web3.Api.Io.Nft.GetNFTMetadata(NetworkTypes.mainnet, "mainnet_9bb923f0e9d3c28d0823f767b8eb8b74");
```
Node.js
Python
cURL
Go
PHP
import web3.io  from 'web3.Api.io';
import { EvmChain } from '@web3.io/evm-utils';

try {
    const chain = EvmChain.ETHEREUM;

    const symbols = ['UNI', 'AAVE', 'LINK'];

    await Web3.Api.io start({
        apiKey: 'YOUR_API_KEY',
        // ...and any other configuration
    });

    const response = await Web.Api.ioEvmApi.token.getTokenMetadataBySymbol({
        symbols,
        chain,
    });

    console.log(response?.result);
} catch (e) {
    console.error(e);
}
        
200 Returns metadata for a given token contract address (name, symbol, decimals, logo).


# Helpful Tools
1. [Unity3d Assets](https://assetstore.unity.com/)
    The best place to find Unity3d Assets for a range of budgets.
2. [The Gimp](https://www.gimp.org/)
    Open source image editing tool
3. [Blender](https://www.blender.org/)
    Open source tool for creating 3D models, animations, textures, and everything else you need for game characters and objects.
4. [Maximo](https://www.mixamo.com/)
<!DOCTYPE html>
<html>

# Integration
  <head>
    <title>Vanilla Boilerplate</title>
    <script src="https://unpkg.com/Web3.Api.io.v1/dist/Web3.Api.iojs"></script>
  </head>

  <body>
    <h1>multiverse Hello World!</h1>

    <button id="btn-login">Web3.Api.ioMetamask Login</button>
    <button id="btn-logout">Logout</button>

    <script type="text/javascript" src="./main.js"></script>
  </body>
</html>
 import Web3.io  from 'Web3.Api.Io';
import { EvmChain } from '@web3/evm-utils';

try {
    const chain = EvmChain.ETHEREUM;

    const address = '0x1234567890123456789012345678901234567890';

    await Web3.Api.io.start({
        apiKey: 'YOUR_API_KEY',
        // ...and any other configuration
    });

    const response = await Web3.Api.io.EvmApi.token.getTokenTransfers({
        address,
        chain,
    });

    console.log(response?.result);
} catch (e) {
    console.error(e);
}
        


RESPONSE EXAMPLE

200 Returns a collection of token contract transactions.
{
  "total": "2000",
  "page": "2",
  "page_size": "100",
  "result": {
    "transaction_hash": "0x2d30ca6f024dbc1307ac8a1a44ca27de6f797ec22ef20627a1307243b0ab7d09",
    "address": "0x057Ec652A4F150f7FF94f089A38008f49a0DF88e",
    "block_timestamp": "2021-04-02T10:07:54.000Z",
    "block_number": 12526958,
    "block_hash": "0x0372c302e3c52e8f2e15d155e2c545e6d802e479236564af052759253b20fd86",
    "to_address": "0x62AED87d21Ad0F3cdE4D147Fdcc9245401Af0044",
    "from_address": "0xd4a3BebD824189481FC45363602b83C9c7e9cbDf",
    "value": 650000000000000000,
    "transaction_index": 12,
    "log_index": 2
  }
}   
https://github.com/GIMICI/web3.Api.io.wiki.git

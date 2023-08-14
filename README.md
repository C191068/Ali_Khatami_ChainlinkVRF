# Ali_Khatami_ChainlinkVRF(learning from the video of Stephen Fluin)

###  Introduction

With Chainlink VRF version 2 we are gonna fund subscription which is basically an account that allows to fund and maintain balance <br>
for multiple consumer contracts <br>

![l27](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/32e10b00-37c2-4913-801c-c81eb57beb1f)


We will go to the above link https://docs.chain.link/getting-started/intermediates-tutorial
and click the get random number shown with black arrow and click Subscriptions manager shown <br>
with blue arrow <br>

![l28](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/b9f8e78c-f4a9-4206-8677-7d240a55736b)

Then we will connnect wallet button here <br>

![l29](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/7af0e328-fbbc-42cd-a9c6-5f175c8f9a4b)

Then we will ckick Create subscription button <br>

![l30](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/1ac48ec7-0557-4d02-a21b-73b2bcb5d769)
here I will use my address as a subscription address <br>

![l31](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/c2fc488b-e05f-48ea-b73f-ae0694123d32)

here we will click the Sign button <br>

![l32](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/109feb6d-06a7-450f-9505-a1b01b1f2722)

Here we will click the Confirm button <br>

![l33](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/2a166f6d-dada-47b6-af21-73c04181e03a)

Thus the Subscriptio is successfully created <br>

Now ew have subscription where we gonna fund it <br>

And we can use that account for all of our random request <br>


![l34](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/0739311e-20d5-49d8-a19f-b6059c3620a0)

We gonna put 10 links you can put whatever you want <br>


![l35](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/ef015b96-b2a1-4190-9dcb-80f73c070d04)

Then we will click the Confirm button <br>

![l36](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/57160cac-b685-4082-8d52-c1a2931176cf)


Thus the fund is added and we will now add consumer <br>

The price and link of evry random number you passed will be based on current gas rates on a given chain as well as gas you choose <br>

![l37](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/8e98cd5e-3518-4fa0-8b26-30ea7e081767)

we have no consumer address <br>

![l38](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/0a058ea3-17e5-4b35-8322-ba4d75852851)

For that we have to link the link below and a contract will be open at REMIX IDE <br>


![l39](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/594b336f-a40e-4983-ac2a-ac02f102fc6d)


This is the contract that opened at REMIX IDE <br>


![l40](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/ecebac4b-28df-4267-82d4-189af6c020ff)

Here at the top we have two important imports <br>


![l41](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/b3e1dcfe-7d00-49bb-9fa8-3912beb84ece)

The key hash option is a way that we specify the gas line was specified in the documentation <br>


So depending on the key hash we choose for the given chain we are on the gas limit will be set differently <br>
for our random number request <br>


![l42](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/5dfe1038-ee47-460e-be0b-83da6889ca97)

here above ```uint32 callbackGasLimit = 40000;```  that we are in charge of <br>

So depending on how much gas we want to spend to fulfill a random number we must set this value appropriately <br>

![l43](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/c9af3499-982a-4693-8774-3e527a930908)

Another most important and useful features that gives a lot more flexibility and control of our VRF <br>

is the number of random numbers we want for that the above white arrow marked variable we use 

![l44](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/782a4918-ad63-4b5a-8ff7-c6131b2a03a7)

In the above constructor we can see address to the coordinator and the subscription that will be created as <br>
we deploy the contract <br>


![l45](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/289a8c13-b82a-46d1-811e-4a57266e0c2e)


Earlier when we created the subscription we got subscription ID <br>
When we gonna deploy this we gonna use this subscription ID <br>


![l46](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/162df46c-ef8b-4546-b229-5c1529e42e8f)

We have got here fulfillRandomWords method that takes in randomness that is going to be fulfilled <br>

by VRF oracle as well we got request random words is how we are gonna actually initiate the request <br>

to the Oracle <br>

![l47](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/173bb15d-dbf3-4d19-912b-994e0f4ef4f6)

The soilidity code is successfully compiled <br>


![l48](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/fac34e78-ddc8-470a-977c-e6cdb6bbc100)

here our environmet will be injectedprovider -metamask <br>

![l49](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/bfbcda65-94bd-4439-8fae-662897f345e2)

We have paste the subscription ID here and click the deploy button <br>

![l50](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/c64beedd-18cb-474e-aeb5-7c162d149293)

Then we will click the confirm button <br>

![l51](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/5b32ba4f-e699-486a-a477-96d278912ab6)


Successful Transaction occured and now we will copy the contract address  <br>



![l52](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/907bccbb-b181-49fe-8c58-f30b09a43091)

And add that as Consumer address in the above section and authorize the contract to use my  <br>
subscription account by clicking ```Add Consumer``` button <br>

![l53](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/f25e6117-0722-4017-b7f0-81bc767fe401)

Metamask will pop up again and ask for confirmation and successful transaction will occured <br>

![l54](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/7fcf743c-eddd-4209-9f6c-6216b1f12e83)

Thus consumer is also successfully added and we will click the ```View Subscription``` button <br>

![l55](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/bb6c1647-d9b2-489e-9095-29875e9610f9)

here we can have our subscription , we can see how much link we funded and we can see our consumer contract <br>

So by doing thses we authorize our consumer contract to make requests for randomness <br>

The solidity code of our roll dice is given below:

```solidity

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.7;

import "@chainlink/contracts/src/v0.8/interfaces/VRFCoordinatorV2Interface.sol";
import "@chainlink/contracts/src/v0.8/VRFConsumerBaseV2.sol";

/**
 * @notice A Chainlink VRF consumer which uses randomness to mimic the rolling
 * of a 20 sided dice
 */

/**
 * Request testnet LINK and ETH here: https://faucets.chain.link/
 * Find information on LINK Token Contracts and get the latest ETH and LINK faucets here: https://docs.chain.link/docs/link-token-contracts/
 */

/**
 * THIS IS AN EXAMPLE CONTRACT THAT USES HARDCODED VALUES FOR CLARITY.
 * THIS IS AN EXAMPLE CONTRACT THAT USES UN-AUDITED CODE.
 * DO NOT USE THIS CODE IN PRODUCTION.
 */

contract VRFD20 is VRFConsumerBaseV2 {
    uint256 private constant ROLL_IN_PROGRESS = 42;

    VRFCoordinatorV2Interface COORDINATOR;

    // Your subscription ID.
    uint64 s_subscriptionId;

    // Sepolia coordinator. For other networks,
    // see https://docs.chain.link/docs/vrf-contracts/#configurations
    address vrfCoordinator = 0x8103B0A8A00be2DDC778e6e7eaa21791Cd364625;

    // The gas lane to use, which specifies the maximum gas price to bump to.
    // For a list of available gas lanes on each network,
    // see https://docs.chain.link/docs/vrf-contracts/#configurations
    bytes32 s_keyHash =
        0x474e34a077df58807dbe9c96d3c009b23b3c6d0cce433e59bbf5b34f823bc56c;

    // Depends on the number of requested values that you want sent to the
    // fulfillRandomWords() function. Storing each word costs about 20,000 gas,
    // so 40,000 is a safe default for this example contract. Test and adjust
    // this limit based on the network that you select, the size of the request,
    // and the processing of the callback request in the fulfillRandomWords()
    // function.
    uint32 callbackGasLimit = 40000;

    // The default is 3, but you can set this higher.
    uint16 requestConfirmations = 3;

    // For this example, retrieve 1 random value in one request.
    // Cannot exceed VRFCoordinatorV2.MAX_NUM_WORDS.
    uint32 numWords = 1;
    address s_owner;

    // map rollers to requestIds
    mapping(uint256 => address) private s_rollers;
    // map vrf results to rollers
    mapping(address => uint256) private s_results;

    event DiceRolled(uint256 indexed requestId, address indexed roller);
    event DiceLanded(uint256 indexed requestId, uint256 indexed result);

    /**
     * @notice Constructor inherits VRFConsumerBaseV2
     *
     * @dev NETWORK: Sepolia
     *
     * @param subscriptionId subscription id that this consumer contract can use
     */
    constructor(uint64 subscriptionId) VRFConsumerBaseV2(vrfCoordinator) {
        COORDINATOR = VRFCoordinatorV2Interface(vrfCoordinator);
        s_owner = msg.sender;
        s_subscriptionId = subscriptionId;
    }

    /**
     * @notice Requests randomness
     * @dev Warning: if the VRF response is delayed, avoid calling requestRandomness repeatedly
     * as that would give miners/VRF operators latitude about which VRF response arrives first.
     * @dev You must review your implementation details with extreme care.
     *
     * @param roller address of the roller
     */
    function rollDice(
        address roller
    ) public onlyOwner returns (uint256 requestId) {
        require(s_results[roller] == 0, "Already rolled");
        // Will revert if subscription is not set and funded.
        requestId = COORDINATOR.requestRandomWords(
            s_keyHash,
            s_subscriptionId,
            requestConfirmations,
            callbackGasLimit,
            numWords
        );

        s_rollers[requestId] = roller;
        s_results[roller] = ROLL_IN_PROGRESS;
        emit DiceRolled(requestId, roller);
    }

    /**
     * @notice Callback function used by VRF Coordinator to return the random number to this contract.
     *
     * @dev Some action on the contract state should be taken here, like storing the result.
     * @dev WARNING: take care to avoid having multiple VRF requests in flight if their order of arrival would result
     * in contract states with different outcomes. Otherwise miners or the VRF operator would could take advantage
     * by controlling the order.
     * @dev The VRF Coordinator will only send this function verified responses, and the parent VRFConsumerBaseV2
     * contract ensures that this method only receives randomness from the designated VRFCoordinator.
     *
     * @param requestId uint256
     * @param randomWords  uint256[] The random result returned by the oracle.
     */
    function fulfillRandomWords(
        uint256 requestId,
        uint256[] memory randomWords
    ) internal override {
        uint256 d20Value = (randomWords[0] % 20) + 1;
        s_results[s_rollers[requestId]] = d20Value;
        emit DiceLanded(requestId, d20Value);
    }

    /**
     * @notice Get the house assigned to the player once the address has rolled
     * @param player address
     * @return house as a string
     */
    function house(address player) public view returns (string memory) {
        require(s_results[player] != 0, "Dice not rolled");
        require(s_results[player] != ROLL_IN_PROGRESS, "Roll in progress");
        return getHouseName(s_results[player]);
    }

    /**
     * @notice Get the house name from the id
     * @param id uint256
     * @return house name string
     */
    function getHouseName(uint256 id) private pure returns (string memory) {
        string[20] memory houseNames = [
            "Targaryen",
            "Lannister",
            "Stark",
            "Tyrell",
            "Baratheon",
            "Martell",
            "Tully",
            "Bolton",
            "Greyjoy",
            "Arryn",
            "Frey",
            "Mormont",
            "Tarley",
            "Dayne",
            "Umber",
            "Valeryon",
            "Manderly",
            "Clegane",
            "Glover",
            "Karstark"
        ];
        return houseNames[id - 1];
    }

    modifier onlyOwner() {
        require(msg.sender == s_owner);
        _;
    }
}


```


![l56](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/3abd973d-67e0-48ef-bc8f-1970ff2b0f2b)

here at roll dice option we will pass our metamask wallet address <br>

![l57](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/8ecd7e35-0afd-4080-965a-5d462cc9fe42)

Then click the Roll dice button <br>

![l58](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/8ee5d790-a23d-4280-ad57-addc516c8532)

Then we wil click here the confirm button <br>

![l59](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/bcee0859-0efd-4401-ad8f-0798f74d7073)
Successful transactions occured <br>




































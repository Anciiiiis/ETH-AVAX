# ETH-AVAX

The DegenToken contract is a custom ERC-20 token named DegenANCIS with the symbol ANCIS, designed for ecosystems where users can earn, transfer, burn, and redeem tokens for virtual items. It uses OpenZeppelin’s ERC20 and Ownable modules to provide standard token functionalities and ownership management.

The contract allows the owner to mint new tokens by calling the mintToken function, specifying the recipient address and the amount. Users can check their balance using the getBalance function, which returns the caller’s token balance. Token transfers are facilitated through the transferToken function, which ensures the sender has enough tokens before transferring them to the specified address.

Tokens can be burned using the burnToken function, reducing the total supply. Additionally, users can redeem tokens for ANCIS items using the redeemANCISItem function, which requires two tokens for each item. The redeemed items are tracked and stored in a list associated with the user’s address.

Users can view their redeemed items using the getANCISItems function, which returns an array of item names, or they can check the total number of items they own with the getANCISItemCount function.

The contract introduces a reward system where each item costs two tokens, stored in the ancisItemValue variable. The mappings ancisItems and ownedItems are used to keep track of redeemed items and the number of items owned by each user, respectively.

To deploy the contract, ensure that OpenZeppelin’s ERC20 and Ownable modules are available in your development environment. You can use Remix or Hardhat for deployment and specify the initial owner address during the process. This contract is licensed under the MIT License, making it open for public use and modification.

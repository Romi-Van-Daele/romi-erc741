// SPDX-License-Identifier: MIT
// Compatible with OpenZeppelin Contracts ^5.0.0
pragma solidity ^0.8.22;

import "@openzeppelin/contracts@5.1.0/token/ERC721/ERC721.sol";
import "@openzeppelin/contracts@5.1.0/token/ERC721/extensions/ERC721URIStorage.sol";
import "@openzeppelin/contracts@5.1.0/access/Ownable.sol";

/// @custom:security-contact lappersbrug@romivandaele.com
contract RomiVanDaele is ERC721, ERC721URIStorage, Ownable {
    constructor(address initialOwner)
        ERC721("Romi Van Daele", "ROMI")
        Ownable(initialOwner)
    {}

    function _baseURI() internal pure override returns (string memory) {
        return "https://romivandaele.com/";
    }

    function safeMint(address to, uint256 tokenId, string memory uri)
        public
        onlyOwner
    {
        _safeMint(to, tokenId);
        _setTokenURI(tokenId, uri);
    }

    // The following functions are overrides required by Solidity.

    function tokenURI(uint256 tokenId)
        public
        view
        override(ERC721, ERC721URIStorage)
        returns (string memory)
    {
        return super.tokenURI(tokenId);
    }

    function supportsInterface(bytes4 interfaceId)
        public
        view
        override(ERC721, ERC721URIStorage)
        returns (bool)
    {
        return super.supportsInterface(interfaceId);
    }
}

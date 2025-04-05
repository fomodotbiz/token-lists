# FOMO.BIZ Community Token List

This repository holds the community-maintained list of **additional tokens** for the [fomo.biz DEX](https://fomo.biz/dex) (Decentralized Exchange) operating on the Taraxa network (Chain ID: 841).

## Purpose

The primary goal of this repository is to allow the community to submit new Taraxa-based tokens (TRC-20) to be listed on the fomo.biz DEX interface. Tokens added here supplement the default list curated by the fomo.biz team.

## How it Works & Token Visibility

*   Tokens successfully added to the list in this repository **will appear** in the token selection menus within the fomo.biz DEX.
*   This means users will be able to find and interact with these tokens directly on the exchange interface for swapping and liquidity provision.
*   **Important:** Inclusion in this list does **not** automatically guarantee the token will be featured on the main "Explore" tab or other promotional sections of the main fomo.biz platform. Visibility is primarily within the DEX's token lists.

## Adding a New Token

To add a new token to the fomo.biz DEX via this list, please follow these steps:

1.  **Fork** this repository (`fomodotbiz/token-lists`) to your own GitHub account.
2.  **Clone** your forked repository to your local machine.
3.  **Locate the primary token list JSON file** within the repository structure (`tokens.json`).
4.  **Add the new token object:**
    *   Carefully add a new JSON object for your token to the `tokens` array within the file.
    *   **Strictly adhere to the following format**, using the correct data types:

        ```json
        {
          "name": "Your Token Name",             // String: Full name of the token
          "address": "0xYourTokenContractAddress", // String: TRC-20 contract address on Taraxa
          "symbol": "SYMBOL",                    // String: Token ticker symbol (usually uppercase)
          "decimals": 18,                        // Number: The number of decimals the token uses
          "chainId": 841,                        // Number: Must be 841 for Taraxa Mainnet
          "isNSFW": false,                       // Boolean: Set to true if name/symbol/logo might be considered Not Safe For Work
          "logoURI": "https://your.image.url/logo.png" // String: Direct, publicly accessible URL to the token logo (HTTPS preferred, IPFS acceptable)
        }
        ```

    *   Ensure the `logoURI` points to a reliable, direct image link (ideally square, transparent background PNG or SVG).
5.  **Commit** your changes with a clear and descriptive commit message (e.g., `feat: Add <Name> (<TICKER>) token`).
6.  **Push** the changes to your forked repository.
7.  **Create a Pull Request (PR)** from your fork's branch to the `main` branch of the upstream repository (`fomodotbiz/token-lists`).

### Pull Request Review Process

*   Your submitted PR will be reviewed by the fomo.biz team.
*   We will verify the token information (contract address, decimals, etc.) and the format of your submission against the required structure.
*   The provided token `logoURI` will be checked. Valid logos may be cached/hosted via our IPFS infrastructure for reliable access within the DEX.
*   If the PR is correctly formatted, the token information is valid, and the token is suitable for listing, it will be merged.
*   **Please ensure your PR is clean, follows the established format precisely, and only adds the token object to the correct array.** PRs requiring significant corrections may be closed.

## Token Functionality on DEX

Once a token from this list is integrated into the fomo.biz DEX, users will be able to:

*   🔄 **Swap:** Trade the token against other listed assets.
*   💧 **Manage Liquidity:** Add or remove liquidity for the token pairs.

## Questions or Issues?

If you encounter any problems while submitting a token or have questions regarding this token list, please reach out to us on Telegram: **@fomodotbiz**

---

Thank you for contributing to the fomo.biz ecosystem on Taraxa!

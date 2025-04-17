# FOMO.BIZ Community Token List & Address Labels

This repository holds the community-maintained lists for the [fomo.biz DEX](https://fomo.biz/dex) (Decentralized Exchange) operating on the Taraxa network (Chain ID: 841). It includes:

1.  **Additional Tokens:** A list of community-submitted TRC-20 tokens to supplement the default DEX token list.
2.  **Address Labels:** A mapping of specific wallet addresses to human-readable names (labels).

## Purpose

*   **Token List (`tokens.json`):** Allow the community to submit new Taraxa-based tokens (TRC-20) to be listed in the token selection menus on the fomo.biz DEX interface.
*   **Address Labels (`labels.json`):** Allow the community to identify and label important addresses (like team wallets, treasury contracts, liquidity pool addresses, etc.). These labels will be displayed on the token holder list page for the relevant token on the fomo.biz platform, improving transparency.

---

## Adding a New Token (`tokens.json`)

This section covers adding **new tokens** to appear in the DEX selection menus.

### How it Works & Token Visibility

*   Tokens successfully added to the `tokens.json` list in this repository **will appear** in the token selection menus within the fomo.biz DEX.
*   This means users will be able to find and interact with these tokens directly on the exchange interface for swapping and liquidity provision.
*   **Important:** Inclusion in this list does **not** automatically guarantee the token will be featured on the main "Explore" tab or other promotional sections of the main fomo.biz platform. Visibility is primarily within the DEX's token lists.

### Steps to Add a Token

To add a new token to the fomo.biz DEX via this list, please follow these steps:

1.  **Fork** this repository (`fomodotbiz/token-lists`) to your own GitHub account.
2.  **Clone** your forked repository to your local machine.
3.  **Locate the primary token list file:** `tokens.json`.
4.  **Add the new token object:**
    *   Carefully add a new JSON object for your token to the `tokens` array within the file.
    *   **Strictly adhere to the following format**, using the correct data types:

        ```json
        {
          "name": "Your Token Name",             // String: Full name of the token
          "address": "0xYourTokenContractAddress", // String: TRC-20 contract address on Taraxa (checksummed preferred)
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

### Token Pull Request Review Process

*   Your submitted PR for `tokens.json` will be reviewed by the fomo.biz team.
*   We will verify the token information (contract address, decimals, etc.) and the format of your submission.
*   The provided token `logoURI` will be checked. Valid logos may be cached/hosted via our IPFS infrastructure.
*   If the PR is correctly formatted, the token information is valid, and the token is suitable for listing, it will be merged.
*   **Please ensure your PR is clean, follows the established format precisely, and only adds the token object to the correct array.** PRs requiring significant corrections may be closed.

### Token Functionality on DEX

Once a token from `tokens.json` is integrated into the fomo.biz DEX, users will be able to:

*   🔄 **Swap:** Trade the token against other listed assets.
*   💧 **Manage Liquidity:** Add or remove liquidity for the token pairs.

---

## Adding Address Labels (`labels.json`)

This section covers adding **human-readable names** for specific blockchain addresses.

### How it Works & Label Visibility

*   The `labels.json` file stores a simple key-value mapping where the key is a Taraxa address and the value is the desired label (name).
*   Labels successfully added to `labels.json` and merged **will be displayed** next to the corresponding address on token holder list pages within the fomo.biz platform.
*   This helps users quickly identify significant holders like project treasuries, liquidity contracts, vesting contracts, etc.

### Steps to Add an Address Label

To propose a new address label:

1.  **Fork** this repository (`fomodotbiz/token-lists`) to your own GitHub account (if you haven't already).
2.  **Clone** your forked repository to your local machine.
3.  **Locate the address label file:** `labels.json`.
4.  **Add the new label entry:**
    *   Add a new key-value pair to the JSON object.
    *   The **key** must be the Taraxa address (string, checksummed format recommended).
    *   The **value** must be the desired label (string).

    *Example format within `labels.json`:*
    ```json
    {
      "0x157bE75819e90736364Bf44D8C6626c619FD0242": "GRUMPY LIQUIDITY",
      "0x42fdDd627F5bC2f8acdb32Bd2544e1A94E7c2ea9": "GRUMPY TREASURY",
      "0xNewAddressToAdd___________________________": "LABEL FOR NEW ADDRESS"
    }
    ```
5.  **Validate** that the JSON structure remains valid after your addition.
6.  **Commit** your changes with a clear message (e.g., `feat: Add label for <Project/Purpose> address`).
7.  **Push** the changes to your forked repository.
8.  **Create a Pull Request (PR)** from your fork's branch to the `main` branch of the upstream repository (`fomodotbiz/token-lists`). In the PR description, briefly explain *why* this address should be labeled (e.g., "This is the official Treasury address for Project X").

### Label Pull Request Review Process

*   Your submitted PR for `labels.json` will be reviewed.
*   We will verify the address format and the appropriateness/accuracy of the suggested label.
*   Labels for well-known contracts or publicly verifiable team/project addresses are more likely to be approved quickly.
*   If the PR is valid and the label is deemed helpful and accurate, it will be merged.

---

## Questions or Issues?

If you encounter any problems while submitting a token or an address label, or have questions regarding these lists, please reach out to us on Telegram: **@fomodotbiz**

---

Thank you for contributing to the fomo.biz ecosystem on Taraxa!

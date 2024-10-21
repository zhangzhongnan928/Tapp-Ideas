# Step-by-Step Guide to Build a Tapp Mockup for an Existing Token/NFT which can be demoed on Twitter

## 1. Choose an Existing Token/NFT
- **Identify the token/NFT** you want to build a tapp for. It can be any token you own or want to interact with (e.g., an ERC-721 NFT or ERC-20 token).

## 2. Discuss Your Tapp Idea
An NFT (such as ERC721) Tapp will appear on Twitter like this:
<img width="663" alt="Screenshot 2024-10-17 at 2 52 27 pm" src="https://github.com/user-attachments/assets/0d6e427b-538d-4fc4-95c9-6952068a175d">

A Fungible token(such as ERC20) Tapp will appear on Twitter like this:
<img width="837" alt="Screenshot 2024-10-17 at 2 35 08 pm" src="https://github.com/user-attachments/assets/902af78a-14e3-49c2-bd51-c8a9950734a0">

To make a Tapp Mockup, you just need to think about 3 functions you want your audience to use right from your twitter feed. ideally when your audience use those functions both of you should get some benefits. 

You can Open **Tapp Product Manager** by visiting [this link](https://chatgpt.com/g/g-jnlADIWqZ-tapp-product-manager) to brainstorm your tapp idea.
  - Example: You can create a tapp that sell your NFTs/token on Twitter.

## 3. Generate the TokenScript Mockup
- Use the [TokenScript Mockup Generator](https://tokenscriptmockupgenerator.tiiny.site/)
- Fill in the required fields:
  - Tapp name
  - Tapp singular name
  - Tapp plural name
  - Tapp description
  - Tapp related website
  - Tapp icon URL
  - Contract name
  - Chain ID and contract address (required)
  - Function card names (required)
- Click "Generate TokenScript Mockup"
- Once generated, download the .tsml file using the "Download .tsml File" link

For a detailed walkthrough of the TokenScript Mockup Generator, refer to the [user manual](https://github.com/zhangzhongnan928/TokenScript-Mockup-Generator/blob/main/README.md) in the GitHub repository.

## 4. Test the TokenScript File in TokenScript Viewer
- Open [TokenScript Viewer](https://viewer.tokenscript.org/).
  - Click **Add Token**, then choose **XML File** to upload the TokenScript mockup file created by Tapp Product Manager.
  - If you own the token/NFT, you should be able to see the tapp in action inside the viewer.
- Alternatively, you can test the tapp directly on Twitter via **Tlink** extension (explained later).

## 5. Host Your TokenScript on GitHub
- Navigate to the [Tapp Ideas GitHub Repo](https://github.com/zhangzhongnan928/
Tapp-Ideas/tree/main/TokenScript%20Mockup).
- Click **Add file**, then **Upload files** to upload the TokenScript file.
  - After uploading, navigate to the file location in the **TokenScript Mockup** 
  folder.
  - Click **Raw** to get the URL of the file.
    - Example: `https://raw.githubusercontent.com/zhangzhongnan928/Tapp-Ideas/refs/
    heads/main/TokenScript%20Mockup/my-tapp.tsml`
  - Copy this URL for the next step.

- If you don't want to use the provided repository, you can create your own:
  1. Go to [GitHub](https://github.com/) and sign in or create an account.
  2. Click the "+" icon in the top right corner and select "New repository".
  3. Name your repository, choose to make it public, and initialize it with a README.
  4. Click "Create repository".
  
- To upload your TokenScript file:
  1. In your new repository, click "Add file", then "Upload files".
  2. Drag and drop your TokenScript file or use the file chooser.
  3. Scroll down and click "Commit changes".
  4. Navigate to your uploaded file and click "Raw" to get its URL.
  5. Copy this URL for the next step.


## 6. Add TokenScript to ERC-7738 Registry
- Based on the blockchain your token/NFT is on, open **TokenScript Viewer**, and follow these steps:
  1. Click **Add Token**, select **Contract Script**, and input `0x0077380bCDb2717C9640e892B9d5Ee02Bb5e0682` as the contract address.
  2. Choose the correct network (based on the token's blockchain) and click **Load**.

## 7. Set the Script URI for Your Token/NFT
- Once the TokenScript Viewer loads the ERC-7738 Registry page:
  1. **Check the URL** to ensure the **?chain=** parameter matches your token’s network.
     - Example: `?chain=1` for Ethereum mainnet, `?chain=137` for Polygon.
  2. Switch your wallet to the correct network.
  3. Click **Set ScriptURI**.
  4. Input your **token/NFT contract address** into the **Contract field**.
  5. Paste the **TokenScript file URL** (from GitHub) into the **ScriptURI field**.
  6. Push the transaction to **register the TokenScript** to the ERC-7738 contract.

## Now You Have Successfully Launched an ERC-7738 Tapp
- Once registered, you will **receive an NFT** representing your ERC-7738 registry entry. The **NFT ID** is your **Script ID**.
  - This NFT confirms the successful launch of your tapp and links the Script ID to the registered tapp.

---

## 8. Access Your Tapp on Twitter or TokenScript Viewer

### 8.1 **In TokenScript Viewer**:
- To access your tapp, use a URL format like:
```
https://viewer.tokenscript.org/?chain=137&contract=0xYourContractAddress&scriptId=7738_YourScriptID#
```
- Replace the parameters based on your token/NFT.

### 8.2 **On Twitter**:
- Share the tapp on Twitter using a **Tlink** URL format:
```
https://viewer.tokenscript.org/?chain=137&contract=0xYourContractAddress&scriptId=7738_YourScriptID#
```

---

## Detailed Explanation of the URL Parameters:
Here’s what each part of the URL represents:

1. **`chain=137`**: Specifies the blockchain network where your token is located.
   - **137** refers to the **Polygon** network. Other common values:
     - Ethereum Mainnet: `1`
     - Binance Smart Chain: `56`
     - Goerli Testnet: `5`

2. **`contract=0xB48f53010Acbc0E24D3D12D892E2215879e6fD13`**: This is the smart contract address of the token/NFT.
   - Replace this with the contract address of your chosen token/NFT.

3. **`scriptId=7738_2`**: Refers to the **Script ID** for your tapp registered in the ERC-7738 registry.
   - The number after `_` refers to the specific tapp entry, which in this case is entry `2`. Modify this based on your tapp’s Script ID.

4. **`#card=Buy`**: This specifies which **action card** to display.
   - In this case, it loads the **Buy** action card for the tapp. You can change this to display different actions such as `Sell` or `Transfer`.
   - Remove `#card=Buy` to load the default tapp landing page.

5. **`tokenId=9940`**: This is the **Token ID** of the specific token or NFT you want to display.
   - Replace this with the Token ID of the item you want to interact with. For ERC-721 (NFTs), this identifies the unique item.

---

## Example Use Cases and URL Modifications:

1. **Switch to Ethereum Mainnet**:
   ```
   https://viewer.tokenscript.org/?chain=1&contract=0xYourContractAddress&scriptId=7738_YourScriptID#
   ```

2. **Display the Transfer Action Card**:
   ```
   https://viewer.tokenscript.org/?chain=137&contract=0xB48f53010Acbc0E24D3D12D892E2215879e6fD13&scriptId=7738_2#card=Transfer&tokenId=9940
   ```

3. **Remove Token ID for a General Tapp View**:
   ```
   https://viewer.tokenscript.org/?chain=137&contract=0xB48f53010Acbc0E24D3D12D892E2215879e6fD13&scriptId=7738_2#
   ```

4. **Change the Token Contract Address and Token ID**:
   ```
   https://viewer.tokenscript.org/?chain=137&contract=0xYourNewContract&scriptId=7738_NewScriptID&tokenId=NewTokenID
   ```

---

## Bonus (彩蛋):
- Try sharing the URL on **Farcaster** to see additional integrations or surprises!

---
Now you have the complete guide to **build, register, and share your tapp 
mockup**. You can see it live on Twitter and in TokenScript Viewer! Enjoy the fun 
of building your tapp and sharing it across platforms.

## Community Resources
- Join the Tapp Ninjas Discord community for help, discussions, and sharing your Tapps: [Tapp Ninjas Discord](https://discord.gg/qcjpck534Y)
- Participate in the TokenScript forum (if available)
- Follow the official TokenScript Twitter account for updates and announcements (if available)

Remember, the Tapp community is growing and evolving. Don't hesitate to reach out for support or to share your creations!

---

# Introduction to Tapps

Tapps (Token Applications) are innovative, cross-platform mini-apps that revolutionize how users interact with their tokens and NFTs. Built on the concept of "Tokens as applications," Tapps leverage the ERC-5169/ERC-7738 standard and TokenScript technology to create portable, user-owned applications that can be accessed across various platforms and channels.

Key benefits of Tapps:

1. Portability: Your Tapps go wherever you go, accessible on social media, messaging apps, digital wallets, and more.
2. Ownership: Users truly own their Tapps, just like they own their tokens.
3. Seamless integration: Tapps can be used directly within existing platforms without the need for separate app installations.
4. Cross-platform compatibility: Developers can create one interface that works in multiple environments.
5. Enhanced token functionality: Users can interact with their tokens in rich, meaningful ways directly from their preferred platforms.

Tapps run on platforms that have installed the TokenScript Engine, enabling a new level of interactivity and utility for blockchain-based assets. This guide will walk you through creating a Tapp mockup for your existing token or NFT, allowing you to experience the power of portable, user-centric applications.

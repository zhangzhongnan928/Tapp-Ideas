
# Step-by-Step Guide to Build a Tapp for an Existing Token/NFT in 5 Minutes

## 1. Choose an Existing Token/NFT
- **Identify the token/NFT** you want to build a tapp for. It can be any token you own or want to interact with (e.g., an ERC-721 NFT or ERC-20 token).

## 2. Discuss Your Tapp Idea
- Open **Tapp Product Manager** by visiting [this link](https://chatgpt.com/g/g-jnlADIWqZ-tapp-product-manager) to brainstorm your tapp idea.
  - Example: You can create a tapp that sell your NFTs/token on Twitter.

## 3. Generate the TokenScript Mockup
- Can use TokenScript Mockup Generator.html

## 4. Test the TokenScript File in TokenScript Viewer
- Open [TokenScript Viewer](https://viewer.tokenscript.org/).
  - Click **Add Token**, then choose **XML File** to upload the TokenScript mockup file created by Tapp Product Manager.
  - If you own the token/NFT, you should be able to see the tapp in action inside the viewer.
- Alternatively, you can test the tapp directly on Twitter via **Tlink** extension (explained later).

## 5. Host Your TokenScript on GitHub
- Navigate to the [Tapp Ideas GitHub Repo](https://github.com/zhangzhongnan928/Tapp-Ideas/tree/main/TokenScript%20Mockup).
- Click **Add file**, then **Upload files** to upload the TokenScript file.
  - After uploading, navigate to the file location in the **TokenScript Mockup** folder.
  - Click **Raw** to get the URL of the file.
    - Example: `https://raw.githubusercontent.com/zhangzhongnan928/Tapp-Ideas/refs/heads/main/TokenScript%20Mockup/my-tapp.tsml`
  - Copy this URL for the next step.

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

Now you have the complete guide to **build, register, and share your tapp**. You can see it live on Twitter and in TokenScript Viewer! Enjoy the fun of building your tapp and sharing it across platforms.

# Automatically and massively upload and sell your non-fungible tokens on OpenSea using Python Selenium.
_A Selenium Python bot to automatically and bulky upload and sell your NFTs on OpenSea  
  (all metadata integrated - Ethereum and Polygon supported)._

---

* **(_Version 1.5.0 - February 16, 2022_).**
* Sign up on [OpenSea](https://opensea.io/).
* Sign up on [MetaMask](https://metamask.io/).

# Table of contents

* **[What does this bot do?](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#what-does-this-bot-do)**
* **[Changelog](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#changelog).**
* **[To do list](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#to-do-list).**
* **[Instructions](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#instructions)**.
  * [Basic installation of Python for beginners](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#basic-installation-of-python-for-beginners).
  * [Configuration of the bot](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#configuration-of-the-bot).
  * [Run the bot](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#run-the-bot).
* **[Data files structure](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#data-files-structure).**
  * [Upload and sale](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#upload-and-sale).
  * [Upload only](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#upload-only).
  * [Sale only](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#sale-only).
* **[Configuration of the sale part of the NFTs](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#configuration-of-the-sale-part-of-the-nfts).**
* **[Known issues and important things to know](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#known-issues-and-important-things-to-know).**


## What does this bot do?

This script allows you to upload and sell **as many NFTs as you want to OpenSea**, all **automatically** and **quickly** (about 2.5 NFTs per minute). **All metadata are integrated**, and the **Ethereum** and **Polygon** Blockchains are supported.  

**You can decide whether you want to upload or sell your NFTs, or both**. If you upload your NFTs and sell them later, a CSV file is created with the URL of the NFT as well as its Blockchain and supply number.

➜ **If you sell any NFT with this bot, you can consider sharing some of your earnings**: 😉
**0xDD135d5be0a23f6daAAE7D2d0580828c9e09402E** (Ethereum).  
➜ **Or you can buy me a NFT from my collection [Crypto Parrot](https://opensea.io/collection/crypto-parrot-nfts) if this bot was useful to you**.


## Changelog

* **Version 1.5.0:**
  * The reCAPTCHAs can now be bypassed. The robot restarts for each upload - it's a bit slow but it works. **[#98](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/98), [#102](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/pull/102)**.  
    Thanks to **[Kanishka-Chandra](https://github.com/Kanishka-Chandra)** and **[elwanm](https://github.com/elwanm)**.
  * The bot restarts after 3 failed connections to the wallet or to OpenSea.
* **Version 1.4.9:**
  * Minor fixes.
  * Developers can now add new wallets if they wish.
  * ChromeDriver is automatically downloaded - no need to do it manually (`pip install -r requirements.txt` required).
  * _The reCAPTCHAs solver is not integrated/configured._
* **Version 1.4.8:**
  * <strike>Added a new feature that allows to upload more than 50 items in a collection. Requires to be activated (asked at launch).</strike> (Method used: https://www.youtube.com/watch?v=8wpmjh8xrXo). **Update:** This method is useless because [OpenSea went back on its words](https://twitter.com/opensea/status/1486843201352716289). The limit has been removed.
  * Minor fix.
* **Version 1.4.7:**
  * The default language of ChromeDriver is now English to ensure maximum compatibility. The date did not work in some countries because of the different formats that OpenSea offers. **[#67](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/67)**.
  * Minor fix (Colorama module).
* **Version 1.4.6:**
  * The duration has been corrected. OpenSea does not allow to change the year when the next year is more than 6 months away. So it was impossible to enter the month without it being replaced by December (12 - maximum number because the year was entered instead); **Note: maximum duration is 6 months. [#55](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/55)**.
  * The connection to OpenSea has *certainly* been corrected. (need feedback about this - I don't have any problems on my side). **[#53](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/53), [#58](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/58), [#61](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/61)**.
* **Version 1.4.5:**
  * Minor fix for Linux users. The `clear_text(self)` method inserts an "A" when it tries to clear the inputs before sending the data. **[#39](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/39)**.
* **Version 1.4.4:**
  * Connection to OpenSea with MetaMask corrected. Download of the extension was requested. **[#53](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/53)**.
  * Connection to OpenSea with MetaMask improved.
* **Version 1.4.3:**
  * File preview is now added. **[#48](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/48)**.
* **Version 1.4.2:**
  * Listing of NFT on the Ethereum Blockchain is fully supported. **Be sure to make a deposit and have more than 0.05 ETH on your wallet.**
* **Version 1.4.1:**
  * Small fix for XLSX files. Empty cells were interpreted as "NaN", which is not interpreted as an empty string for Python. **[#18](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/18), [#23](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/23)**.
* **Version 1.4:**
  * You can now decide whether you want to upload or sell your NFTs, or both. **[#3](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/3), [#22](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/22)**.
  * Signing the MetaMask contract works every time. It can take 30 seconds to be signed when connecting to OpenSea. **[#5](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/5), [#17](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/17)**.
  * After uploading the NFT, the bot would crash when it tried to sell it (the URL was not correct). Now it doesn't. **[#17](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/17)**.
  * MacOS and Linux support improved.
  * Calendar method improved.
* **Version 1.3:**
  * Important fixes. **[#4](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/4), [#6](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/6), [#10](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/10), [#11](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/11), [#12](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/12), [#14](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/14)**.
  * CSV file modified: separator changed (from ";" to ";;").
* **Version 1.2:**
  * Possibility to set a price for each NFT added.  
    ➜ 1+ supplies and Polygon blockchain support added.
  * Supply input issue fixed.
  * Calendar method improved.
* **Version 1.2-alpha:**
  * Possibility to set a price for each NFT added.
* **Version 1.1:** 
  * XLSX support added.
  * PC-wide data file browse support.
  * Properties, Stats and Levels issues fixed. **[#1](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/issues/1)**.
* **Version 1.0:** 
  * Inital commit.


## To do list

* ❌ Graphic User Interface.
* ❌ Website for NFTs creation.
* ✔ <strike>Data file browsing feature.</strike>
* ✔ <strike>CSV structure reader and interpreter.</strike>
* ✔ <strike>JSON structure reader and interpreter.</strike>
* ✔ <strike>XLSX structure reader and interpreter.</strike>
* ✔ <strike>MetaMask automatic login.</strike>
* ❌ OpenSea automatic login with different wallets.
  * ✔ <strike>OpenSea automatic login with MetaMask.</strike>
* ❌ Change of wallet for the same account.
* ❌ OpenSea Testnet automatic login.
* ❌ Collection creator for OpenSea.
* ✔ <strike>Automatic NFT upload.</strike>
* ✔ <strike>Automatic NFT sale.</strike>
* ❌ Update of NFT metadata.
* ✔ <strike>Ethereum and Polygon blockchains support.</strike>
* ✔ <strike>1+ supplies support.</strike>
* ❌ "Sell as bundle" part (not planned to be added).



## Instructions

* ### Basic installation of Python for beginners:
  * [Download the repository](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/archive/refs/heads/master.zip) or clone it by typing this command in your command prompt:
    
    ```
    git clone https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale.git
    ```
  * It requires [Python](https://www.python.org/) 3.7 or a newest version - _developped with Python 3.9.7_.
  * Install [pip](https://pip.pypa.io/en/stable/installation/) to be able to have needed Python modules.

* ### Configuration of the bot:
  * Extract the repository folder from the ZIP file, you should have a folder named  `opensea-automatic-bulk-upload-and-sale-master`.
  * Open a command prompt in the repository folder and type one of these commands (may require ``sudo`` on MacOS and Linux):
    
    * ```
      pip install -r requirements.txt
      ```
    * ```
      pip3 install -r requirements.txt
      ```
    * ```
      python -m pip install -r requirements.txt
      ```
    * ```
      python3 -m pip install -r requirements.txt
      ```
    * ```
      py -m pip install -r requirements.txt
      ```
  * Download and install [Google Chrome](https://www.google.com/intl/en_en/chrome/).
  * Create your NFTs data file containing all details of each NFT. It can be a JSON, CSV or XLSX file. You can save it in the `data/` folder.  
    **[What structure should the files have?](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale#data-files-structure)**
* ### Run the bot:
  * Open a command prompt in the `opensea-automatic-bulk-upload-and-sale-master/` folder path.
  * Type one of these commands to run the bot:
    
    * ```
      python main.py
      ```
    * ```
      python3 main.py
      ```


## Data files structure

If you do not want to add details to the values not required, leave:
  * **a blank cell** for XLSX files (Excel):
    <table>
     <tbody>
      <tr>
       <td>File Path</td>
       <td>NFT Name</td>
       <td>Description</td>
      </tr>
      <tr>
       <td>C:/Users/Admin/Desktop/NFT/nft_0001.png</td>
       <td>NFT #1</td>
       <td></td>
      </tr>
     </tbody>
    </table>

  * **a white space with two semicolons** for CSV files:
    ```csv
    file_path;; nft_name;; description;;
    C:/Users/Admin/Desktop/NFT/nft_0001.png;; NFT #1;; ;;
    ```
  * **an empty string** for JSON files: 
    ```json
    "file_path": "C:/Users/Admin/Desktop/NFT/nft_0001.png",
    "nft_name": "NFT #1",
    "description": "",
    ```

<strong>Required values *</strong>  
  (Mandatory value in certain specified cases)

* ### Upload and sale

  <table>
     <tbody>
        <tr>
           <td>Details</td>
           <td>Data Types</td>
           <td>Literal examples</td>
           <td>JSON examples</td>
           <td>CSV examples</td>
           <td>XLSX examples</td>
        </tr>
        <tr>
           <td><strong>File Path * </strong>(The preview is only for files that are not images)</td>
           <td>String or List</td>
           <td></td>
           <td>"file_path": "C:/Users/Admin/Desktop/NFT/nft_0001.png",
           <br>"file_path": ["C:/Users/Admin/Desktop/NFT/nft_0001.mp4", "C:/Users/Admin/Desktop/NFT/nft_0001-preview.png"],</td>
           <td>C:/Users/Admin/Desktop/NFT/nft_0001.png;;
           <br>["C:/Users/Admin/Desktop/NFT/nft_0001.mp4", "C:/Users/Admin/Desktop/NFT/nft_0001-preview.png"];;</td>
           <td>C:/Users/Admin/Desktop/NFT/nft_0001.png
           <br>["C:/Users/Admin/Desktop/NFT/nft_0001.mp4", "C:/Users/Admin/Desktop/NFT/nft_0001-preview.png"];;</td>
        </tr>
        <tr>
           <td><strong>NFT Name *</strong></td>
           <td>String</td>
           <td></td>
           <td>"nft_name": "NFT #1",</td>
           <td>NFT #1;;</td>
           <td>NFT #1</td>
        </tr>
        <tr>
           <td>External Link</td>
           <td>String</td>
           <td></td>
           <td>"external_link": "https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale",
              <br>"external_link": "",
           </td>
           <td>https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale;;</td>
           <td>https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale</td>
        </tr>
        <tr>
           <td>Description</td>
           <td>String</td>
           <td></td>
           <td>"description": "This is my first NFT.",
              <br>"description": "",
           </td>
           <td>This is my first NFT.;;</td>
           <td>This is my first NFT.</td>
        </tr>
        <tr>
           <td>Collection</td>
           <td>String</td>
           <td></td>
           <td>"collection": "My NFTs",
              <br>"collection": "",
           </td>
           <td>My NFTs;;</td>
           <td>My NFTs.</td>
        </tr>
        <tr>
           <td>Properties</td>
           <td>List[[String, String], ...]
            <br>List[String, String]</td>
           <td>["type", "name"]
            <br>[["type", "name"], ["type", "name"]]</td>
           <td>"properties": [{ "type": "Dog", "name": "Male" }, { "type": "Cat", "name": "Female" }],
              <br>"properties": [{ "type": "Dog", "name": "Male" }],
              <br>"properties": "",
           </td>
           <td>[["Dog", "Male"], ["Cat", "Female"]];;
              <br>[["Dog", "Male"]];;
              <br>["Dog", "Male"];;
           </td>
           <td>[["Dog", "Male"], ["Cat", "Female"]]
              <br>[["Dog", "Male"]]
              <br>["Dog", "Male"]
           </td>
        </tr>
        <tr>
           <td>Levels</td>
           <td>List[[String, Integer, Integer], ...]
            <br>List[String, Integer, Integer]</td>
           <td>["name", value_from, value_to]
            <br>[["name", value_from, value_to], ["name", value_from, value_to]]</td>
           <td>"levels": [{ "name": "Speed", "from": 2, "to": 5 }, { "name": "Width", "from": 1, "to": 10 }],
              <br>"levels": [{ "name": "Speed", "from": 2, "to": 5 }],
              <br>"levels": "",
           </td>
           <td>[["Speed", 2, 5], ["Width", 1, 10]];;
              <br>[["Speed", 2, 5]];;
              <br>["Speed", 2, 5];;
           </td>
           <td>[["Speed", 2, 5], ["Width", 1, 10]]
              <br>[["Speed", 2, 5]]
              <br>["Speed", 2, 5]
           </td>
        </tr>
        <tr>
           <td>Stats</td>
           <td>List[[String, Integer, Integer], ...]
            <br>List[String, Integer, Integer]</td>
           <td>["name", value_from, value_to]
            <br>[["name", value_from, value_to], ["name", value_from, value_to]]</td>
           <td>"stats": [{ "name": "Strenght", "from": 10, "to": 100 }, { "name": "Age", "from": 1, "to": 99 }],
              <br>"stats": [{ "name": "Strenght", "from": 10, "to": 100 }],
              <br>"stats": "",
           </td>
           <td>[["Strenght", 10, 100], ["Age", 1, 99]];;
              <br>[["Strenght", 10, 100]];;
              <br>["Strenght", 10, 100];;
           </td>
           <td>[["Strenght", 10, 100], ["Age", 1, 99]]
              <br>[["Strenght", 10, 100]]
              <br>["Strenght", 10, 100]
           </td>
        </tr>
        <tr>
           <td>Unlockable Content</td>
           <td>List[Boolean, String]
            <br>List[Boolean]
            <br>Boolean</td>
           <td>[True, "unlockable_content"]
            <br>[False]
            <br>False</td>
           <td>"unlockable_content": [true, "Thank you for purchasing my NFT!"],
              <br>"unlockable_content": [false],
              <br>"unlockable_content": false,
              <br>"unlockable_content": "",
           </td>
           <td>[True, "Thank you for purchasing my NFT!"];;
              <br>[False];;
              <br>False;;
           </td>
           <td>[True, "Thank you for purchasing my NFT!"]
              <br>[False]
              <br>False
           </td>
        </tr>
        <tr>
           <td>Explicit And Sensitive Content</td>
           <td>Boolean</td>
           <td></td>
           <td>"explicit_and_sensitive_content": true,
              <br>"explicit_and_sensitive_content": false,
              <br>"explicit_and_sensitive_content": "",
           </td>
           <td>True;;
              <br>False;;
           </td>
           <td>True
              <br>False
           </td>
        </tr>
        <tr>
           <td>Supply</td>
           <td>Integer</td>
           <td></td>
           <td>"supply": 1,
              <br>"supply" : "",
           </td>
           <td>1;;</td>
           <td>1</td>
        </tr>
        <tr>
           <td>Blockchain</td>
           <td>String</td>
           <td></td>
           <td>"blockchain": "Polygon",
              <br>"blockchain" : "",
           </td>
           <td>Polygon;;</td>
           <td>Polygon</td>
        </tr>
        <tr>
           <td>Sale Type (only for Ethereum Blockchain and 1 supply)</td>
           <td>String</td>
           <td></td>
           <td>"sale_type": "Timed Auction",
              <br>"sale_type": "",
           </td>
           <td>Timed Auction;;</td>
           <td>Timed Auction</td>
        </tr>
        <tr>
           <td><strong>Price *</strong></td>
           <td>Float or Integer</td>
           <td></td>
           <td>"price": 5,
              <br>"price": 0.25,
           </td>
           <td>5;;
              <br>0.25;;
           </td>
           <td>5
              <br>0.25
           </td>
        </tr>
        <tr>
           <td>Method (only for "Timed Auction")</td>
           <td>List[String, Float]</td>
           <td>["method", price]
            <br>["method, ""]</td>
           <td>"method": ["Sell with declining price", 0.002],
              <br>"method": ["Sell to highest bidder", 0.05],
              <br>"method": ["Sell to highest bidder", ""],
              <br>"method": "",
           </td>
           <td>["Sell with declining price", 0.002];;
              <br>["Sell to highest bidder", 0.05];;
              <br>["Sell to highest bidder", ""];;
           </td>
           <td>["Sell with declining price", 0.002]
              <br>["Sell to highest bidder", 0.05]
              <br>["Sell to highest bidder", ""]
           </td>
        </tr>
        <tr>
           <td>Duration ("DD-MM-YYYY HH:MM")</td>
           <td>List[String, String]
            <br>List[String]
            <br>String</td>
           <td>["from_date", "to_date"]
            <br>["days/weeks/months"]
            <br>"days/weeks/months"</td>
           <td>"duration": ["01-01-2022 14:00", "01-04-2022 15:00"],
              <br>"duration": ["1 week"],
              <br>"duration": "1 week",
              <br>"duration": "",
           </td>
           <td>["01-01-2022 14:00", "01-04-2022 15:00"];;
              <br>["1 week"];;
              <br>1 week;;
           </td>
           <td>["01-01-2022 14:00", "01-04-2022 15:00"]
              <br>["1 week"]
              <br>1 week
           </td>
        </tr>
        <tr>
           <td>Specific Buyer</td>
           <td>List[Boolean, String]
            <br>[Boolean]
            <br>Boolean</td>
           <td>[True, "wallet"]
            <br>[False]
            <br>False</td>
           <td>"specific_buyer": [true, "0xDD135d5be0a23f6daAAE7D2d0580828c9e09402E"],
              <br>"specific_buyer": [false],
              <br>"specific_buyer": false,
              <br>"specific_buyer": "",
           </td>
           <td>[True, "0xDD135d5be0a23f6daAAE7D2d0580828c9e09402E"];;
              <br>[False];;
              <br>False;;
           </td>
           <td>[True, "0xDD135d5be0a23f6daAAE7D2d0580828c9e09402E"]
              <br>[False]
              <br>False
           </td>
        </tr>
        <tr>
           <td><strong>Quantity * (only for 1+ supplies)</strong></td>
           <td>Integer</td>
           <td></td>
           <td>"quantity": 4
              <br>"quantity": ""
           </td>
           <td>4</td>
           <td>4</td>
        </tr>
     </tbody>
  </table>
 
  And it gives you something like this: [JSON](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/json_structure_upload_and_sale.json), [CSV](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/csv_structure_upload_and_sale.csv), [XLSX (must be downloaded to view it)](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/xlsx_structure_upload_and_sale.xlsx).
 
* ### Upload only

  <table>
     <tbody>
        <tr>
           <td>Details</td>
           <td>Data Types</td>
           <td>Literal examples</td>
           <td>JSON examples</td>
           <td>CSV examples</td>
           <td>XLSX examples</td>
        </tr>
        <tr>
           <td><strong>File Path *</strong> (The preview is only for files that are not images)</td>
           <td>String or List</td>
           <td></td>
           <td>"file_path": "C:/Users/Admin/Desktop/NFT/nft_0001.png",
           <br>"file_path": ["C:/Users/Admin/Desktop/NFT/nft_0001.mp4", "C:/Users/Admin/Desktop/NFT/nft_0001-preview.png"],</td>
           <td>C:/Users/Admin/Desktop/NFT/nft_0001.png;;
           <br>["C:/Users/Admin/Desktop/NFT/nft_0001.mp4", "C:/Users/Admin/Desktop/NFT/nft_0001-preview.png"];;</td>
           <td>C:/Users/Admin/Desktop/NFT/nft_0001.png
           <br>["C:/Users/Admin/Desktop/NFT/nft_0001.mp4", "C:/Users/Admin/Desktop/NFT/nft_0001-preview.png"];;</td>
        </tr>
        <tr>
           <td><strong>NFT Name *</strong></td>
           <td>String</td>
           <td></td>
           <td>"nft_name": "NFT #1",</td>
           <td>NFT #1;;</td>
           <td>NFT #1</td>
        </tr>
        <tr>
           <td>External Link</td>
           <td>String</td>
           <td></td>
           <td>"external_link": "https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale",
              <br>"external_link": "",
           </td>
           <td>https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale;;</td>
           <td>https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale</td>
        </tr>
        <tr>
           <td>Description</td>
           <td>String</td>
           <td></td>
           <td>"description": "This is my first NFT.",
              <br>"description": "",
           </td>
           <td>This is my first NFT.;;</td>
           <td>This is my first NFT.</td>
        </tr>
        <tr>
           <td>Collection</td>
           <td>String</td>
           <td></td>
           <td>"collection": "My NFTs",
              <br>"collection": "",
           </td>
           <td>My NFTs;;</td>
           <td>My NFTs.</td>
        </tr>
        <tr>
           <td>Properties</td>
           <td>List[[String, String], ...]
            <br>List[String, String]</td>
           <td>["type", "name"]
            <br>[["type", "name"], ["type", "name"]]</td>
           <td>"properties": [{ "type": "Dog", "name": "Male" }, { "type": "Cat", "name": "Female" }],
              <br>"properties": [{ "type": "Dog", "name": "Male" }],
              <br>"properties": "",
           </td>
           <td>[["Dog", "Male"], ["Cat", "Female"]];;
              <br>[["Dog", "Male"]];;
              <br>["Dog", "Male"];;
           </td>
           <td>[["Dog", "Male"], ["Cat", "Female"]]
              <br>[["Dog", "Male"]]
              <br>["Dog", "Male"]
           </td>
        </tr>
        <tr>
           <td>Levels</td>
           <td>List[[String, Integer, Integer], ...]
            <br>List[String, Integer, Integer]</td>
           <td>["name", value_from, value_to]
            <br>[["name", value_from, value_to], ["name", value_from, value_to]]</td>
           <td>"levels": [{ "name": "Speed", "from": 2, "to": 5 }, { "name": "Width", "from": 1, "to": 10 }],
              <br>"levels": [{ "name": "Speed", "from": 2, "to": 5 }],
              <br>"levels": "",
           </td>
           <td>[["Speed", 2, 5], ["Width", 1, 10]];;
              <br>[["Speed", 2, 5]];;
              <br>["Speed", 2, 5];;
           </td>
           <td>[["Speed", 2, 5], ["Width", 1, 10]]
              <br>[["Speed", 2, 5]]
              <br>["Speed", 2, 5]
           </td>
        </tr>
        <tr>
           <td>Stats</td>
           <td>List[[String, Integer, Integer], ...]
            <br>List[String, Integer, Integer]</td>
           <td>["name", value_from, value_to]
            <br>[["name", value_from, value_to], ["name", value_from, value_to]]</td>
           <td>"stats": [{ "name": "Strenght", "from": 10, "to": 100 }, { "name": "Age", "from": 1, "to": 99 }],
              <br>"stats": [{ "name": "Strenght", "from": 10, "to": 100 }],
              <br>"stats": "",
           </td>
           <td>[["Strenght", 10, 100], ["Age", 1, 99]];;
              <br>[["Strenght", 10, 100]];;
              <br>["Strenght", 10, 100];;
           </td>
           <td>[["Strenght", 10, 100], ["Age", 1, 99]]
              <br>[["Strenght", 10, 100]]
              <br>["Strenght", 10, 100]
           </td>
        </tr>
        <tr>
           <td>Unlockable Content</td>
           <td>List[Boolean, String]
            <br>List[Boolean]
            <br>Boolean</td>
           <td>[True, "unlockable_content"]
            <br>[False]
            <br>False</td>
           <td>"unlockable_content": [true, "Thank you for purchasing my NFT!"],
              <br>"unlockable_content": [false],
              <br>"unlockable_content": false,
              <br>"unlockable_content": "",
           </td>
           <td>[True, "Thank you for purchasing my NFT!"];;
              <br>[False];;
              <br>False;;
           </td>
           <td>[True, "Thank you for purchasing my NFT!"]
              <br>[False]
              <br>False
           </td>
        </tr>
        <tr>
           <td>Explicit And Sensitive Content</td>
           <td>Boolean</td>
           <td></td>
           <td>"explicit_and_sensitive_content": true,
              <br>"explicit_and_sensitive_content": false,
              <br>"explicit_and_sensitive_content": "",
           </td>
           <td>True;;
              <br>False;;
           </td>
           <td>True
              <br>False
           </td>
        </tr>
        <tr>
           <td><strong>Supply *</strong></td>
           <td>Integer</td>
           <td></td>
           <td>"supply": 1,</td>
           <td>1;;</td>
           <td>1</td>
        </tr>
        <tr>
           <td><strong>Blockchain *</strong></td>
           <td>String</td>
           <td></td>
           <td>"blockchain": "Polygon"</td>
           <td>Polygon</td>
           <td>Polygon</td>
        </tr>
     </tbody>
  </table>
 
  And it gives you something like this: [JSON](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/json_structure_upload_only.json), [CSV](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/csv_structure_upload_only.csv), [XLSX (must be downloaded to view it)](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/xlsx_structure_upload_only.xlsx).
 
* ### Sale only
 
  If you have already uploaded your NFTs with this bot, a file has been generated with containing the URL, the Blockchain and the supply number of each NFT. You have to complete it with sale values.

  <table>
     <tbody>
        <tr>
           <td>Details</td>
           <td>Data Types</td>
           <td>Literal examples</td>
           <td>JSON examples</td>
           <td>CSV examples</td>
           <td>XLSX examples</td>
        </tr>
        <tr>
           <td><strong>NFT URL * </strong></td>
           <td>String</td>
           <td></td>
           <td>"nft_url": "https://opensea.io/assets/matic/0x2953399124f0cbb46d2cbacd8a89cf0599974963/99995353970554757559721471534129028266698199001274859511402524949800648966145",</td>
           <td>https://opensea.io/assets/matic/0x2953399124f0cbb46d2cbacd8a89cf0599974963/99995353970554757559721471534129028266698199001274859511402524949800648966145;;</td>
           <td>https://opensea.io/assets/matic/0x2953399124f0cbb46d2cbacd8a89cf0599974963/99995353970554757559721471534129028266698199001274859511402524949800648966145</td>
        </tr>
        <tr>
           <td><strong>Supply *</strong></td>
           <td>Integer</td>
           <td></td>
           <td>"supply": 1,</td>
           <td>1;;</td>
           <td>1</td>
        </tr>
        <tr>
           <td><strong>Blockchain *</strong></td>
           <td>String</td>
           <td></td>
           <td>"blockchain": "Polygon",</td>
           <td>Polygon;;</td>
           <td>Polygon</td>
        </tr>
        <tr>
           <td>Sale Type (only for Ethereum Blockchain and 1 supply)</td>
           <td>String</td>
           <td></td>
           <td>"sale_type": "Timed Auction",</td>
           <td>Timed Auction;;</td>
           <td>Timed Auction</td>
        </tr>
        <tr>
           <td><strong>Price *</strong></td>
           <td>Float or Integer</td>
           <td></td>
           <td>"price": 5,
              <br>"price: 0.25,</td>
           <td>5;;
              <br>0.25;;
           </td>
           <td>5
              <br>0.25
           </td>
        </tr>
        <tr>
           <td>Method (only for "Timed Auction")</td>
           <td>List[String, Float]</td>
           <td>["method", price]
            <br>["method, ""]</td>
           <td>"method": ["Sell with declining price", 0.002],
              <br>"method": ["Sell to highest bidder", 0.05],
              <br>"method": ["Sell to highest bidder", ""],</td>
           <td>["Sell with declining price", 0.002];;
              <br>["Sell to highest bidder", 0.05];;
              <br>["Sell to highest bidder", ""];;
           </td>
           <td>["Sell with declining price", 0.002]
              <br>["Sell to highest bidder", 0.05]
              <br>["Sell to highest bidder", ""]
           </td>
        </tr>
        <tr>
           <td>Duration ("DD-MM-YYYY HH:MM")</td>
           <td>List[String, String]
            <br>List[String]
            <br>String</td>
           <td>["from_date", "to_date"]
            <br>["days/weeks/months"]
            <br>"days/weeks/months"</td>
           <td>"duration": ["01-01-2022 14:00", "01-04-2022 15:00"],
              <br>"duration": ["1 week"],
              <br>"duration": "1 week",
           </td>
           <td>["01-01-2022 14:00", "01-04-2022 15:00"];;
              <br>["1 week"];;
              <br>1 week;;
           </td>
           <td>["01-01-2022 14:00", "01-04-2022 15:00"]
              <br>["1 week"]
              <br>1 week
           </td>
        </tr>
        <tr>
           <td>Specific Buyer</td>
           <td>List[Boolean, String]
            <br>[Boolean]
            <br>Boolean</td>
           <td>[True, "wallet"]
            <br>[False]
            <br>False</td>
           <td>"specific_buyer": [true, "0xDD135d5be0a23f6daAAE7D2d0580828c9e09402E"]
               <br>"specific_buyer": [false]
               <br>"specific_buyer": false</td>
           <td>[True, "0xDD135d5be0a23f6daAAE7D2d0580828c9e09402E"];;
              <br>[False];;
              <br>False;;
           </td>
           <td>[True, "0xDD135d5be0a23f6daAAE7D2d0580828c9e09402E"]
              <br>[False]
              <br>False
           </td>
        </tr>
        <tr>
           <td><strong>Quantity * (only for 1+ supplies)</strong></td>
           <td>Integer</td>
           <td></td>
           <td>"quantity": 4</td>
           <td>4</td>
           <td>4</td>
        </tr>
     </tbody>
  </table>

  And it gives you something like this: [JSON](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/json_structure_sale_only.json), [CSV](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/csv_structure_sale_only.csv), [XLSX (must be downloaded to view it)](https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/blob/master/data/xlsx_structure_sale_only.xlsx).


## Configuration of the sale part of the NFTs

When you want to sell your NFTs, Opensea requires various details according to their Blockchain or supply number.  
**Note: The maximum duration of sale should be at most 6 months. It must be entered in the form of start date - end date.**

  <table>
     <tbody>
        <tr>
           <td colspan="15">Ethereum</td>
           <td colspan="7">Polygon</td>
        </tr>
        <tr>
           <td colspan="11">Supply number equal to 1</td>
           <td colspan="4">Supply number higher than 1</td>
           <td colspan="3">Supply number equal to 1</td>
           <td colspan="4">Supply number higher than 1</td>
        </tr>
        <tr>
           <td colspan="3">Fixed Price</td>
           <td colspan="8">Timed Auction</td>
           <td colspan="4"></td>
           <td colspan="3"></td>
           <td colspan="4"></td>
        </tr>
        <tr>
           <td colspan="3"></td>
           <td colspan="4">Sell to highest bidder</td>
           <td colspan="4">Sell with declining price</td>
           <td colspan="4"></td>
           <td colspan="3"></td>
           <td colspan="4"></td>
        </tr>
        <tr>
           <td><strong>Price</strong> (ETH)</td>
           <td><strong>Duration</strong> (from a date to an other date <strong>or</strong> 1 day, 3 days, 1 week, 1 month)</td>
           <td>Reserve for a <strong>specific buyer</strong></td>
           <td><strong>Price</strong> (ETH)</td>
           <td><strong>Duration</strong> (from a date to an other date <strong>or</strong> 1 day, 3 days, 1 week)</td>
           <td><i>(Optional)</i> <strong>Reserved Price</strong> (WETH) greater than 1 WETH and greater than the <strong>Starting Price</strong>.</td>
           <td>Reserve for a <strong>specific buyer</strong></td>
           <td><strong>Starting Price</strong> (ETH)</td>
           <td><strong>Duration</strong> (from a date to an other date or 1 day, 3 days, 1 week)</td>
           <td><strong>Ending Price</strong> (ETH) less than the <strong>Starting Price</strong>.</td>
           <td>Reserve for a <strong>specific buyer</strong></td>
           <td><strong>Quantity</strong></td>
           <td><strong>Price</strong> (ETH)</td>
           <td><strong>Duration</strong> (from a date to an other date <strong>or</strong> 1 day, 3 days, 1 week, 1 month)</td>
           <td>Reserve for a <strong>specific buyer</strong></td>
           <td><strong>Price</strong> (ETH)</td>
           <td><strong>Duration</strong> (from a date to an other date <strong>or</strong> 1 day, 3 days, 1 week, 1 month)</td>
           <td>Reserve for a <strong>specific buyer</strong></td>
           <td><strong>Quantity</strong></td>
           <td><strong>Price</strong> (ETH)</td>
           <td><strong>Duration</strong> (from a date to an other date <strong>or</strong> 1 day, 3 days, 1 week, 1 month)</td>
           <td>Reserve for a <strong>specific buyer</strong></td>
        </tr>
     </tbody>
  </table>


## Known issues and important things to know

* Make sure to **deposit Ethereum (ETH/WETH)** or **Polygon (MATIC)** on your wallet before proceeding to the sale. Otherwise the bot will cancel the sale. Opensea needs an **Ethereum** wallet with more than **0.05 ETH** or a **Polygon** wallet with a deposit of **any amount**. For **Ethereum**, you have to make a first listing manually before using this bot.
* **The file path should not contain a unique "\\". It can be a "/" or a "\\\\", as you can see for the JSON file *(it applies to all file formats)*:**
  
  ```json
  // You can use this format for your path:
  "file_path": "C:/Users/Admin/Desktop/MyNFTs/nft_0001.png",
  // or this one:
  "file_path": "C:\\Users\\Admin\\Desktop\\MyNFTs\\nft_0001.png",
  // but not this one (you can see that "\" is highlighted in red):
  "file_path": "C:\Users\Admin\Desktop\MyNFTs\nft_0001.png",
  ```
* The bot may crash at the beginning when loading the MetaMask extension (a Selenium module issue), An error like the one below should appear:  
  
  ```python
  selenium.common.exceptions.WebDriverException:
  Message: unknown error: failed to wait for extension background page to load:
  chrome-extension://nkbihfbeogaeaoehlefnkodbefpgknn/background.html from timeout:
  Timed out receiving message from renderer: 10.000
  ```
* When lauching the webdriver, Selenium can raise an exception:
  
  ```python
  driver = webdriver.Chrome(service=Service( # DeprecationWarning using
  TypeError: WebDriver.init() got an unexpected keyword argument 'service'
  ```
  You must update your Selenium version to 4.1.0 or higher by typing in the command prompt:
  
  ```
  pip install selenium --upgrade
  ```
  You can now verify that a more recent version of Selenium is installed by typing:
  
  ```
  pip show selenium
  ```  

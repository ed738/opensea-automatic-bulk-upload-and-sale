<h1 align="center">Automatically and massively upload and list your non-fungible tokens on the OpenSea marketplace using Python Selenium.</h1>

<p align="center"><i>A Selenium Python bot to automatically and bulky upload and list your NFTs on OpenSea.
<br />All metadata integrated - Ethereum and Polygon supported - reCAPTCHA solver services included.</i>
<br><strong><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Changelog">Version 1.10.1</a> (July 01, 2022).</strong></p>

<div align="center"><hr width="30%" /></div>

<p align="center">If you like 💚 my work and this tool, do not hesitate to
<br /><strong>fork 🍴</strong> this repository and <strong>add a star ⭐</strong> to this repository.</p>

<h2>Table of contents - <a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki">Documentation</a></h2>

<ul>
<li><strong><a href="#bypass-recaptchas-using-an-undectable-exploit-on-opensea">NEW: Bypass reCAPTCHAs</a> on OpenSea using an exploit.</strong></li>
<li><strong><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Home#introduction">Introduction</a>, what does this bot do and how does it works?</strong></li>
<li><strong><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Home#frequently-asked-questions">Frequently Asked Questions</a> about the creation of the metadata file and reCAPTCHA solver services.</strong></li>
<li><strong><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Installation-and-configuration">Installation and configuration</a> of Python, the required modules and the bot.</strong></li>
<li><strong><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Creation-of-the-metadata-file">Creation of the metadata file</a>, discover its structure.</strong></li>
<li><strong>➜ <a href="#useful-tools-to-have-for-this-bot">Useful tools to have for this bot</a></strong></li>
<ul>
<li><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/File-Compatibilizer-&-Converter">File Compatibilizer & Converter</a>, from the HashLips Art Engine metadata files to one compatible file.</li>
<li><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Generic-File-Maker">Generic File Maker</a>, complete your metadata file easily and quickly.</li>
<li><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Collection-Scraper">Collection Scraper</a>, retrieve the URLs of your NFTs and get the duplicates and missing.</li>
<li><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/reCAPTCHA-Bypasser">reCAPTCHA Bypasser</a>, instantly solve the reCAPTCHAs.</li>
<li><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Multiprocessing">Multiprocessing</a>, for lightning-fast uploading.</li>
<li><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Deletion">Deletion</a>, delete all the duplicate and unwanted NFTs.</li>
</ul>
<li><strong><a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/Changelog">Changelog</a>, new fixes and features.</strong></li>
</ul>

<br />
<div align="center">
<h2>Bypass reCAPTCHAs using an undectable exploit on OpenSea</h2>
<p>The <a href="https://github.com/maximedrn/opensea-automatic-bulk-upload-and-sale/wiki/reCAPTCHA-Bypasser">reCAPTCHA Bypasser</a> allows an instant solve of the reCAPTCHAs.
<br />Up to <strong>400 NFTs per hour</strong>, or <strong>10,000 NFTs in one day</strong> with one process.
<br />Watch this <a href="https://www.youtube.com/watch?v=oSqIqbuFnn0">video</a> to see <strong>how fast</strong> the upload is with this exploit!</p>

<a href="https://www.youtube.com/watch?v=oSqIqbuFnn0">
<img alt="[TUTORIAL] CREATE & UPLOAD NFTs to OpenSea - Bypass reCAPTCHAs" src="https://user-images.githubusercontent.com/91475935/170870961-049139f7-3ec9-40a0-a0e9-daa4eaa38435.png" width="60%" />
</a>
</div>

<div align="center"><hr width="30%" /></div>

<p align="center" width="50%"><strong>Need help or have a specific request?</strong>
<br />Look at my offer on <a href="https://fiverr.com/maximedrn/help-you-for-the-upload-and-sale-bot">Fiverr <img src="https://user-images.githubusercontent.com/91475935/169694667-68824ed9-10a3-46ee-9fc1-23ec91496121.png" height="15px" /></a> to help you to create your metadata file and install the bot.  
<br />Contact me via <a href="https://t.me/maximedrn">Telegram</a> or e-mail me at <a href="mailto:maxime_drean@yahoo.com">maxime_drean@yahoo.com</a>.<p>

<h2>Introduction</h2>

<p>With this bot, <strong>you can choose to upload, list or even both your non-fungible tokens</strong> on the OpenSea marketplace.</p>

<p>You just have to <strong>create a metadata file</strong> following the requested structure, JSON, CSV and XLSX (Excel file) formats are available. This file will include every detail for each NFT. Then, you just have to <strong>launch the bot</strong> and <strong>select the action you want to perform</strong>, as well as the metadata file created. Finally, <strong>the bot will automate the tedious task of uploading or listing NFTs, one by one by hand, for several days</strong>.</p>

<ul>
<li>Absolutely <strong>all upload details are supported</strong>, you can add as many properties as you want.</li>
<li><strong>All file formats</strong> offered by OpenSea <strong>are compatible</strong>, including images, videos or even 3D models.</li>
<li><strong>Ethereum and Polygon blockchains are supported</strong>, and the switch between these two blockchains is also supported.</li>
<li>In case of failure during an upload, a listing or when you only want to upload your NFTs on OpenSea, <strong>a file is generated with details already filled</strong> in or to be filled in.</li>
</ul>

<h2>Useful tools to have for this bot</h2>

<p><strong>This tool is entirely free</strong>, buying add-ons only speeds up the process. All the means to deploy your collection on OpenSea are present.
<br /><i>Please check that the bot is fully functional before purchasing. Refunds will not be accepted if it is not.</i></p>

<h3><a href="https://maximedrn.gumroad.com/l/opensea-file-compatibilizer">File Compatibilizer & Converter</a></h3>

<p>Using the <strong>File Compatibilizer and Converter</strong>, you can <strong>convert all JSON files generated with the <a href="https://github.com/HashLips/hashlips_art_engine">HashLips Art Engine</a> tool into a single compatible file</strong>. The tool ignores the file named <code>_metadata.json</code> and focuses on all other files listed. It <strong>retrieves each of the information containing them such as attributes</strong> and properties and adds them into a single file.</p>

<div align="center"><hr width="30%" /></div>

<h3><a href="https://maximedrn.gumroad.com/l/opensea-generic-file">Generic File Maker</a></h3>

<p>Using the <strong>Generic File Maker</strong>, you can <strong>complete your JSON metadata file using a simple generic file that contains 21 details</strong>, 18 about NFTs and 3 about how the tool works. It supports increment value, for example if you name your assets (images or videos) from 1 to 10000, you can <strong>in one line complete all the file paths of the metadata file</strong>.</p>

<div align="center"><hr width="30%" /></div>

<h3><a href="https://maximedrn.gumroad.com/l/opensea-collection-scraper">Collection Scraper</a></h3>

<p>Using the <strong>Collection Scraper</strong>, you can <strong>retrieve the URLs of the NFTs of any collection</strong>. It makes it easier to manage your collection, you can now know which NFTs are missing, which ones are duplicated. It facilitates the listing of your NFTs by <strong>creating different files compatible with the <code>Sale Only</code> option.</strong></p>

<p>Thus a <code>full</code> file containing all NFTs, a <code>unique</code> file containing each NFT individually based on their names, a <code>duplicate</code> file containing all duplicated NFTs of the collection and a <code>missing</code> file containing all missing NFTs will be created, and these in all formats compatible with the bot (JSON, CSV and XLSX).</p>

<div align="center"><hr width="30%" /></div>

<h3><a href="https://maximedrn.gumroad.com/l/opensea-no-recaptcha">reCAPTCHA Bypasser</a></h3>

<p>Using the <strong>reCAPTCHA Bypasser</strong>, you can <strong>instantly solve reCAPTCHAs when uploading to OpenSea</strong>. This maximizes the upload speed on OpenSea, <strong>the average 30 second wait time of other solvers no longer exists with this solver</strong>. It uses an exploit to bypass the reCAPTCHA. The upload speed is such that there would be no reCAPTCHA.</p>

<div align="center"><hr width="30%" /></div>

<h3><a href="https://maximedrn.gumroad.com/l/opensea-multiprocessing">Multiprocessing</a></h3>

<p>Using the <strong>Multiprocessing</strong> tool, you can upload your NFTs faster and with several processes running at the same time. You can have up to 5 simultaneous processes depending on the power of your computer. It splits your file into several sub-files, then opens several command prompts that work like the main bot but at the same time: it connects to your wallet, connects to OpenSea and starts the upload or listing task.</p>

<div align="center"><hr width="30%" /></div>

<h3><a href="https://maximedrn.gumroad.com/l/opensea-deletion">Deletion</a></h3>

<p>Using the <strong>Deletion</strong> tool, you can <strong></strong> delete any NFT on OpenSea. It is compatible with the <a href="https://maximedrn.gumroad.com/l/opensea-collection-scraper">Collection Scraper</a> which creates files for duplicated NFTs or for an entire collection.</p>

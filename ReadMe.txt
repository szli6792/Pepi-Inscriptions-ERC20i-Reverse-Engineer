HOW TO USE:



-This has been done for you:-
0) Upload these files and folders to jupyter notebook or an environment that can execute .ipynb files

1) Find Pepi smartcontract on etherscan

2) Go to oldest transactions, and for each transaction that uses a set function, grab the bytecode
Ex: This is where all Pepi body shapes were loaded to Pepi smartcontract-> https://basescan.org/tx/0xac8d97bcb91111fb1fe1e7ecaa883b97876a40479f05f8877562af800456f23f

3) Copy bytecode into decoder to get json object. Stored jsons in ./jsons_from_bytecode

Decoder I used:
https://lab.miguelmota.com/ethereum-input-data-decoder/example/

4) Use bytecode2svg.ipynb to plot a bunch of sprites displaying the entire Pepi sprite library
Each plot is labeled with pack, attribute number (ex:body001), evolutionary level, and count by level of the sprite
bytecode2svg.ipynb also populates ./svgs_from_bytecode with every sprite as a seperate svg file

5) Use svg2json.ipynb to grab every svg from ./svgs_from_bytecode and return it to the .json format for loading set functions (outputs are stored in ./svgs_to_json)

6) Clone Pepi onto a testnet and load the contents of each .json file found in ./svgs_to_json into its respective set function (call write the Pepi smartcontract)

7) Call read function getSVG() from Pepi testnet

8) Compare testnet results to actual Pepi results to confirm that svg2json.ipynb is working correctly




-Start here-
9) Run bytecode2svg.ipynb to see the entire Pepi sprite library (WARNING: this will overwrite your svgs in./svgs_from_bytecode)
Each plot is labeled with pack, attribute number (ex:body001), evolutionary level, and count by level of the sprite
bytecode2svg.ipynb also populates ./svgs_from_bytecode with every sprite as a seperate svg file

10) svg_combiner.ipynb can be used to preview combinations of the 6 different attributes of a Pepi from its respective svg file
This is useful for testing new sprites

11) Modify the svg files under ./svg_from_bytecode to add your own sprites

12) Execute steps 5 and 7 to get your sprites into a copy of Pepi on testnet

13) Use front end interface to confirm your svg sprites are displayed correctly

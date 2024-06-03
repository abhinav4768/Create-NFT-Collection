# Create-NFT-Collection
In this project our solution comprisively consists to generate random values for collecting NFTs.
// Function to generate a random eye color
function getRandomEyeColor() {
    var eyeColors = ["blue", "green", "brown", "gray"];
    return eyeColors[Math.floor(Math.random() * eyeColors.length)];
}

// Function to generate a random shirt type
function getRandomShirtType() {
    var shirtTypes = ["t-shirt", "polo", "hoodie", "tank top"];
    return shirtTypes[Math.floor(Math.random() * shirtTypes.length)];
}

// Function to generate a random bling
function getRandomBling() {
    var blings = ["gold chain", "diamond necklace", "platinum bracelet", "silver watch"];
    return blings[Math.floor(Math.random() * blings.length)];
}

// Define a function to create a random NFT
function createRandomNFT() {
    var name = "NFT #" + (Math.floor(Math.random() * 10000) + 1);
    var eyeColor = getRandomEyeColor();
    var shirtType = getRandomShirtType();
    var bling = getRandomBling();

    return {
        name: name,
        eyeColor: eyeColor,
        shirtType: shirtType,
        bling: bling
    };
}

// Define a function to print NFT details
function printNFTDetails(nft) {
    console.log("Name: " + nft.name);
    console.log("Eye Color: " + nft.eyeColor);
    console.log("Shirt Type: " + nft.shirtType);
    console.log("Bling: " + nft.bling);
    console.log("-----------------------");
}

// Generate an array of random NFTs
var nfts = [];
for (var i = 0; i < 3; i++) {
    nfts.push(createRandomNFT());
}

// Loop through the array of NFTs and print their details
nfts.forEach(function(nft) {
    printNFTDetails(nft);
});


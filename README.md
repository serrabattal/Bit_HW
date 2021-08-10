# Blockchain Homework
This is the instructions for the blockchain homework.
For this homework, I created a "homework" network by using puppeth using **Proof of Authority** consensus algorithm. The screenshots below show how to create the network.

 ![First screenshot](https://user-images.githubusercontent.com/80998119/128881239-22bd3afd-dad0-4b5b-bf2d-45041e1f11a5.PNG)
 
Then by choosing the **manage existing genesis** option, I exported the genesis configurations and initialized the two nodes with the **homework.json** with **geth**.

![configurations2](https://user-images.githubusercontent.com/80998119/128881723-f6a2d51e-759d-4885-a1b4-4bdfff13e52b.PNG)

Later, I run the first node, unlock the account, enable mining, and the RPC flag by using the following command on gitbash:

> ./geth --datadir node1 --mine --miner.threads 1 --unlock "81276d901b11fE86C737d0925AF6b0f5724182e0" --rpc --allow-insecure-unlock

Later, I run the second node with the following command on gitbash:

> ./geth --datadir node2 --unlock "D4c35729b3B46f5413ac6B85Ea8F43A536eA8548" --mine --port 30304 --bootnodes enode://f55dabed26277b8c9e59240e5ef46c70b0e7252029cac3831a1557490f8457e6fc19726b9f831b2086fb8e98d00d7c02480b9830c05a59c4380b01de2a681a3e@127.0.0.1:30303 --ipcdisable

Gitbash started looking for peers by running these commands as can be seen below in the screenshots for the two nodes.

For node1:
![blockchain1](https://user-images.githubusercontent.com/80998119/128883369-ba60ef0b-d79a-487f-865c-90fa7403665a.PNG)

For node2:
![blockchain2](https://user-images.githubusercontent.com/80998119/128883420-ec7198f5-b3e0-44df-929a-6bc9d8d33660.PNG)

With the commands running on gitbash, I logged into **MyCrypto** and created a custom network using Chain ID: 333.

![image](https://user-images.githubusercontent.com/80998119/128883933-08f8f1d2-cf4f-47a6-950d-9f7e5acff9ad.png)

After that, I logged into the wallet using the keystore file for node 1.

![image](https://user-images.githubusercontent.com/80998119/128884095-55ca0d5a-82db-4db9-85ee-6b673645293d.png)
![image](https://user-images.githubusercontent.com/80998119/128884288-511b9be4-3d76-4730-bdaa-91dd06211e4d.png)

However, unfortunately, I was not able to see the prefunded balance in my nodes. Therefore, I was not able to send the transaction.








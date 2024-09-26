```console
cd ~/btc_testnet4/rbo_indexer_testnet
````

```console
rm -rf rbo_worker
````

```console

# buradan container id alıyoruz bitcoin-cli olan.
docker ps

# id kısmını doldurup kaldırıyoruz.
docker stop id
docker rm id
````
```console
wget https://storage.googleapis.com/rbo/rbo_worker/rbo_worker-linux-amd64-0.0.2-20240914-4ec80a8.tar.gz && tar -xzvf rbo_worker-linux-amd64-0.0.2-20240914-4ec80a8.tar.gz
````
```console
mv rbo_worker-linux-amd64-0.0.2-20240914-4ec80a8/rbo_worker rbo_worker
````
```console
docker-compose up -d
````
```console
./rbo_worker worker --rpc http://127.0.0.1:5000 --password demo --username demo --start_height 4200 > worker.log &
````

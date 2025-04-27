# install 
```bash
wget -q -O rpc_holesky.sh https://raw.githubusercontent.com/SellUrSou1/hol/refs/heads/main/install.sh && chmod +x rpc_holesky.sh && ./rpc_holesky.sh
```
# logs
```bash
echo "→ Geth syncing?"; curl -s -X POST http://localhost:8545   -H "Content-Type: application/json"   --data '{"jsonrpc":"2.0","method":"eth_syncing","params":[],"id":1}' ; echo; echo "→ Teku health & syncing:"; curl -s http://localhost:5051/eth/v1/node/health; echo; curl -s http://localhost:5051/eth/v1/node/syncing; echo
```
# answer
```
→ Geth syncing?
{"jsonrpc":"2.0","id":1,"result":false}
```
# means that Geth is not in the process of syncing (i.e., fully synchronized).
```
→ Teku health & syncing:

{"data":{"head_slot":"4154566","sync_distance":"0","is_syncing":false,"is_optimistic":false,"el_offline":false}}    
```
# sync_distance: "0" and is_syncing: false correctly indicate that Teku is also fully synchronized and operating in normal mode (el_offline: false, is_optimistic: false).

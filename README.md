wget -q -O rpc_holesky.sh https://raw.githubusercontent.com/mgpwnz/drosera/refs/heads/main/rpc_holesky.sh && chmod +x rpc_holesky.sh && ./rpc_holesky.sh

echo "→ Geth syncing?"; curl -s -X POST http://localhost:8545   -H "Content-Type: application/json"   --data '{"jsonrpc":"2.0","method":"eth_syncing","params":[],"id":1}' ; echo; echo "→ Teku health & syncing:"; curl -s http://localhost:5051/eth/v1/node/health; echo; curl -s http://localhost:5051/eth/v1/node/syncing; echo
![image.png](attachment:536d1538-83af-4880-a359-390c03f14822:image.png)

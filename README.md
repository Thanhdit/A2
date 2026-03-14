# UX
await new Promise(r => (window.ethereum ? r() : window.addEventListener("ethereum#initialized", r, { once: true })));
const accounts = await window.ethereum?.request({ method: "eth_accounts" });
const chainId = await window.ethereum?.request({ method: "eth_chainId" });
const contract = new ethers.Contract(addr, abi, provider);
const provider = new ethers.JsonRpcProvider(RPC_URL);
document.body.classList.toggle("loading", !window.ethereum);

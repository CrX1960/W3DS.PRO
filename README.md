<h1>Blockchain-based File Storage System</h1>

<h2>🚀 How to Run the Application</h2>

1. Install required libraries using:  
   <code>pip install -r requirements.txt</code><br/>
2. Start the backend server:  
   <code>python run_app.py</code><br/>
3. Open your browser and go to the printed localhost URL.<br/>
4. To compare different Proof of Work strategies:  
   <code>python POW_Comparison.py</code><br/>

<h2>📌 Project Information</h2>

This is a full-stack decentralized file storage system using **blockchain technology**, built with:

- <b>Flask (Python)</b> backend
- <b>MongoDB</b> for user authentication and file metadata
- <b>Smart contract deployment</b> on Sepolia testnet via Web3.py
- <b>Tailwind CSS, Three.js, and GSAP</b> for the frontend
- On-chain file storage in custom blockchain blocks
- Two <b>Proof of Work</b> algorithms with a performance comparison

Users can register, log in, and upload/download files. Each file upload creates a new block that includes the file name, size, content, uploader info, and a timestamp. All blocks are cryptographically linked using SHA-256, ensuring data immutability.

We use a custom blockchain implementation to store files **on-chain** for maximum security, while also experimenting with different PoW strategies.

<h2>💡 Key Features</h2>

<ul>
  <li>🗂 File uploads with any file type and size</li>
  <li>🔗 Blockchain structure storing file data immutably</li>
  <li>🧾 Proof-of-work with random and iterative nonce algorithms</li>
  <li>🌐 Web interface with modern UI/UX</li>
  <li>🪙 Ethereum smart contract deployment via Sepolia testnet</li>
  <li>📊 PoW performance comparison for security vs efficiency</li>
  <li>📋 Clipboard features and animated feedback on frontend</li>
</ul>

<h2>🧠 Importance of Blockchain in File Storage</h2>

Blockchain provides a tamper-proof structure to store digital information. By storing files directly on-chain, we ensure:
- Security (no unauthorized edits or deletions)
- Decentralization (peer-to-peer control)
- Transparency and traceability

This project demonstrates a practical use case where users can upload any files, and those files are safely encoded inside the blockchain.

<h2>🛠 Proof of Work Algorithms</h2>

We implemented two PoW methods:

1. **Random Nonce**: `nonce = random.randint(0, 99999999)`
2. **Iterative Nonce**: `nonce += 1`

Each tries to find a hash starting with N zeros (`difficulty=3` by default).

<h3>📈 PoW Comparison Results</h3>

<b>First Algorithm (Random Nonce)</b>

| Difficulty | Attempt #1 | Attempt #2 | Attempt #3 | Attempt #4 |
|------------|------------|------------|------------|------------|
| 2          | 0.00018s   | 0.00281s   | 0.00102s   | 0.00039s   |
| 3          | 0.00069s   | 0.03207s   | 0.00485s   | 0.00356s   |
| 4          | 0.13479s   | 0.22688s   | 0.34565s   | 0.19841s   |
| 5          | 4.06034s   | 2.08288s   | 0.58391s   | 0.2094s    |

<b>Second Algorithm (Iterative Nonce)</b>

| Difficulty | Attempt #1 | Attempt #2 | Attempt #3 | Attempt #4 |
|------------|------------|------------|------------|------------|
| 2          | 0.00035s   | 0.00080s   | 0.00062s   | 0.00108s   |
| 3          | 0.02190s   | 0.02463s   | 0.02104s   | 0.01625s   |
| 4          | 0.00366s   | 0.03813s   | 0.32095s   | 0.02145s   |
| 5          | 0.04403s   | 3.10820s   | 1.53688s   | 1.50288s   |

<h3>⚖️ Which Algorithm is Better?</h3>

<b>Random Nonce:</b>  
✅ Better for high difficulty  
✅ Less predictable  
✅ Safer against attacks

<b>Iterative Nonce:</b>  
⚠️ Predictable nonce range  
⚠️ Slower with dynamic data  
⚠️ Potential vulnerability if hash structure is known

<h2>🧠 Security Insight</h2>

Iterative nonce can be guessed based on timing, making it less secure. With the random method, all nonce values are equally probable, offering better resistance to timing attacks and improving overall security.

<h2>⚠️ Drawbacks of Random Nonce</h2>

Random number generation is computationally expensive. Use faster random functions like `random.random()` when possible. Proof of Stake (PoS) is a more energy-efficient alternative.

<h2>💾 On-chain vs Off-chain Blockchain</h2>

<b>On-chain:</b>  
✅ Higher security  
✅ Easier recovery  
❌ Slower insertions  
❌ High storage cost

<b>Off-chain:</b>  
✅ Lightweight  
✅ Faster  
❌ Less secure  
❌ Dependency on external storage

We chose **On-chain** for this project to prioritize **file integrity and immutability**.

<h2>🔗 Smart Contracts (vaultstorage.sol)</h2>

- Deployed to Sepolia testnet
- Provides on-chain proof of file activity
- Used for credential handling and future storage credits

<h2>🖥️ Tech Stack</h2>

- <b>Backend:</b> Python, Flask, Web3.py  
- <b>Database:</b> MongoDB Atlas  
- <b>Blockchain:</b> Custom PoW Blockchain, Sepolia Smart Contract  
- <b>Frontend:</b> HTML, TailwindCSS, Three.js, GSAP  
- <b>Security:</b> SHA256, Encrypted file handling, Clipboard management

<h2>📽️ Project Demo</h2>

Live Demo & GitHub Link:  
<a href="https://github.com/CrX1960/W3DS.PRO">https://github.com/CrX1960/W3DS.PRO</a>

<h2>📚 References</h2>

1. <a href="https://github.com/JungWinter/file-on-blockchain">JungWinter/file-on-blockchain</a><br/>
2. <a href="https://github.com/MoTechStore/Python-Flask-Blockchain-Based-Content-Sharing">MoTechStore Blockchain Sharing</a><br/>
3. <a href="https://medium.com/@amannagpal4/how-to-create-your-own-decentralized-file-sharing-service-using-python-2e00005bdc4a">Medium: Decentralized File Sharing</a><br/>

---

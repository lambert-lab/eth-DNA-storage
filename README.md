Archival of the Ethereum Blockchain for >10,000 years using DNA Storage.

# Gitcoin Grant Proposal

Ethereum's stated goal is to be resilient against catastrophic events and be able to survive World War 3. Part of this resiliency relies on the ability to easily reconstruct the entirety of the Ethereum blockchain using decentralized peer-to-peer sharing.

The retrieval of information, however, still requires nodes to be kept online or blockchain data to be available upon request, both of which may prove to be a central point of failure if there is no electrical power or if access to the high-speed internet is limited. Ultimately, there should be a way to store all the data contained in the Ethereum blockchain in a storage medium that does not require expensive equipment and specific storage conditions. Additionally, it must be possible to easily duplicate archival data in a cost-effective manner.

We believe that long-term storage of digital data in DNA solves the following problems:
Data density: the data density of DNA is close to 1 exabyte (10^18 bytes) per cubic centimeter, meaning that a few milligrams of DNA could store the entirety of the Ethereum blockchain.
Future proofness: while most storage mediums rely on technology that may become outdated in the next decades, DNA data retrieval is based on DNA sequencing technologies that will likely continue to be an important aspect of clinical research in the future (that is, unless our future selves are not made out of DNA anymore...)
Storage Lifetime: DNA has been successfully recovered from frozen fossils that were thousands of years old, suggesting that digital data stored in DNA under the appropriate conditions (ie. less than -80C) could be preserved for much longer than that.

While the idea of storing digital information in DNA may seem outlandish at first, the process itself is fairly straightforward. First, binary information is converted into DNA nucleotides (G,A,T,C) and each nucleotide sequence is synthesized as single-stranded DNA oligomers using conventional DNA synthesis techniques. Up to 1 million of these oligomers are pooled together into a single test tube and these oligo pools are either lyophilized or encapsulated in silica for long-term storage.  Data recovery is performed by reading the sequence of these oligo pools using next-generation sequencing technologies (ie. it uses the same instruments that are currently used to sequence human genomes). 

Several academic groups have demonstrated the storage of digital information of increasing complexity in DNA [1]. Yet, most DNA recovery methods were plagued by a relatively high error-rate, which limited the effectiveness of DNA storage methods. Recently, researchers have effectively solved this problem by implementing Reed-Solomon error correction encoding [2] to DNA digital Data [3], which effectively enables the recovery of information in an error-free manner despite sample degradation. This work solved one of the last problems associated with DNA storage, thereby ensuring that the long-term storage of information in DNA is perhaps the only storage media that can last thousands of years [4]. 

This grant will provide funds to the Lambert Lab for the proof-of-concept development of a workflow for the synthesis, storage, retrieval, and easy-dissemination of data from the Ethereum blockchain using DNA. We will follow the recently published protocol by Meiser et al. from Glass group [5] to enode, store, and retrieve data from the Ethereum blockchain.

Since the synthesis of the entirety of the Ethereum blockchain is still cost-prohibitive, the project will reach the following milestones, in order of complexity/cost: 

Storage of:
1. Single block header: 600byte
2. Complete block (including transactions): 20-30kB
3. All Cryptopunks: 830kB [6]
4. Stateless block witness: ~2MB [7, 8]
5. Complete history of a single account or smart contract: 2-50MB
6. Data for Eth2.0 deposit smart contract: https://etherscan.io/address/0x00000000219ab540356cbb839cbe05303d7705fa
7. Bridge contract transactions (Optimism, Arbitrum, Polyscan, Ronin, etc)
8. Complete NFT collection (eg. Artblocks project)
9. Continuous blocks: 30kB * N, with N>10,000
10. Full pruned Blockchain: 200GB
11. Archival Node: >1TB


# Methods

DNA synthesis will be performed using commercially available services such as the 12K and 90K oligo "chips" from Genscript (Twist Bioscience may also be used for pools requiring more than 1M oligos). A few example datasets, and their DNA encoding, are included on this project's Github [9] (url coming soon!).

DNA amplification and purification, DNA stabilization and immobilization, and DNA sequencing and analysis will be performed in the Lambert Lab. Amplification from the encoded oligo pool will be carried out using a Polymerase Chain Reaction (PCR) that uses a high-fidelity DNA polymerase and a protocol optimized for short target amplification [10].

DNA samples will either be lyophilized in a trehalose solution (half-life >1 year at room temperature [11]) or immobilized in silica particles (stability >2000 years at 9.4C [2]). Long term stability will be assayed using the technique developed by Organick et al. that leverages the Arrheius equation and quantitative PCR to extract DNA lifetimes.

Sequencing of small datasets (<1MB)  will be performed on an Illumina iSeq 100 already in Dr. Lambert's laboratory. Sequencing of larger datasets will be performed on a Nextseq2000 or HiSeq from the Cornell Institute of Biotechnology.

# About the Lambert Lab

The Lambert Lab (lambertlab.io) is led by Dr. Guillaume Lambert, an Assistant Professor in the Department of Applied and Engineering Physics at Cornell University. The Lambert Lab uses fundamental physical principles and synthetic biology to study biological systems at the single-cell and single-molecule level. Members of the Lambert Lab have extensive experience in synthetic biology, computational biology, and DNA sequencing/genomics.


# Perks

A sample of lyophilized DNA containing information about any specific address, smart contract, or NFT will be sent to the top 10 contributors of this project as a "thank you" note. 


# References

Ceze, L., Nivala, J. & Strauss, K. Molecular digital data storage using DNA. Nature Reviews Genetics 20, 456–466 (2019).
Reed, I. S. & Solomon, G. Polynomial Codes Over Certain Finite Fields. Journal of the Society for Industrial and Applied Mathematics 8, 300–304 (1960).
Grass, R. N., Heckel, R., Puddu, M., Paunescu, D. & Stark, W. J. Robust Chemical Preservation of Digital Information on DNA in Silica with Error-Correcting Codes. Angewandte Chemie International Edition 54, 2552–2555 (2015).
Meiser, L. C. et al. Reading and writing digital data in DNA. Nat Protoc 15, 86–101 (2020).
Matange, K., Tuck, J. M. & Keung, A. J. DNA stability: a central design consideration for DNA data storage systems. Nat Commun 12, 1358 (2021).
https://github.com/larvalabs/cryptopunks/blob/master/punks.png
https://ethresear.ch/t/detailed-analysis-of-stateless-client-witness-size-and-gains-from-batching-and-multi-state-roots/862
https://medium.com/@mandrigin/stateless-ethereum-binary-tries-experiment-b2c035497768
https://github.com/reinhardh/dna_rs_coding
https://www.neb.com/products/m0544-nebnext-ultra-ii-q5-master-mix
Organick, L. et al. An Empirical Comparison of Preservation Methods for Synthetic DNA Data Storage. Small Methods 5, 2001094 (2021).


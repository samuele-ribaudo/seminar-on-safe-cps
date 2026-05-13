# Schedule-Based Cyber Attacks

## Introduction
The security of the real-time embedded systems, due to the increasing connectivity (e.g., Internet of Things), is now more important than ever before. One of the most notable examples of exploiting the security holes in this kind of systems is the remote hijacking of a Jeep’s digital system that led Chrysler to recall 1.4 million vehicles (https://www.bbc.com/news/technology-33650491). The real- time systems are designed to enforce the deterministic runtime behavior: they execute the tasks in a specific order that guarantees the reaction time to external events within strict time limits. Schedule- based attacks exploit the information about the tasks execution order to trigger the attacks at the precise moments of targeted task execution. For instance, a cache-timing attack is more efficient if executed right before and right after the targeted task when its data still stays in the cache. Also, the denial-of-service attacks can be more harmful and more difficult to detect when the victim execution time window is directly targeted. The purpose of this literature review is to identify the threats that are posed to the cyber-physical systems and summarize the existing countermeasures.

**References:**

[1] Chen, Chien-Ying, Monowar Hasan, and Sibin Mohan. “Securing Real-Time Internet-of-Things.” Sensors 18.12 (2018)

[2] M. Nasri, T. Chantem, G. Bloom and R. M. Gerdes, "On the Pitfalls and Vulnerabilities of Schedule Randomization Against Schedule-Based Attacks," 2019 IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS)

[3] Chien-Ying Chen, Rakesh B Bobba, and Sibin Mohan. “Schedule-based side-channel attack in fixed- priority real-time systems”, 2015

[4] Chien-Ying Chen, Sibin Mohan, Rodolfo Pellizzoni, Rakesh B. Bobba, Negar Kiyavash. “A novel side-channel in real-time schedulers.” 2019 IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS)

[5] V. Kiriansky, I. Lebedev, S. Amarasinghe, S. Devadas and J. Emer, "DAWG: A Defense Against Cache Timing Attacks in Speculative Execution Processors," 2018 51st Annual IEEE/ACM International Symposium on Microarchitecture (MICRO), Fukuoka, 2018

**Supervisor**: Alex Züpke (alex.zuepke@tum.de)


## Approach: Evolutionary Timeline of CPS Security
Our research analyzes the technical "Arms Race" between Schedule-Based Attacks and their corresponding Countermeasures in Real-Time Systems (RTS). We categorize the co-evolution of these technologies into three eras:

### 1.⁠ ⁠The Foundations of Predictability
**The Concept:** Real-time determinism—traditionally a safety requirement—is identified as a fundamental security flaw that enables precise timing inference.

**The Conflict:** Early research proved that observing resource availability allows an adversary to reconstruct execution schedules.

**Initial Defenses:** Focus on Obfuscation (shuffling task order to create timing noise) and Hardware Partitioning (isolating cache resources to prevent cross-domain leaks).

### 2.⁠ ⁠Multi-Core Complexity & Network Exposure
**The Concept:** The shift toward high-performance multicore platforms and connected IoT expanded the attack surface to shared microarchitectural resources.

**The Conflict:** The introduction of shared caches, interconnects, and speculative execution logic created hardware "shortcuts" that leak data faster than software randomization can hide it.

**Advanced Defenses:** Development of Architectural Hardening, utilizing scalable isolation and cross-layer frameworks to protect shared resources without compromising real-time performance.

### 3.⁠ ⁠Attack-Aware Resilience & Control Stability
**The Concept:** Recognition that absolute secrecy is often unattainable in deterministic systems; focus shifts from hiding data to ensuring physical survival.

**The Conflict:** Sophisticated algorithms can now "see through" blind randomization, while new attacks target the communication backbone (e.g., CAN, TSN) to cause physical failure through timing sabotage.

**Emerging Defenses:** A move toward Attack-Aware Design. Modern frameworks sense potential interference and adjust timing dynamically to prioritize Closed-Loop Resilience—ensuring the system’s physical stability and safety-critical deadlines remain guaranteed even during an active attack.



## Papers
### Attack side
[1] Chien-Ying Chen, Rakesh B Bobba, and Sibin Mohan. “Schedule-based side-channel attack in fixedpriority real-time systems”, 2015

[2] Fangfei Zhou, Manish Goel, Peter Desnoyers, Ravi Sundaram, "Scheduler Vulnerabilities and Coordinated Attacks in Cloud Computing", IEEE 10th International Symposium on Network Computing and Applications, Cambridge, MA, USA, 10 October 2011.

[3] Chen, Chien-Ying, Monowar Hasan, and Sibin Mohan. “Securing Real-Time Internet-of-Things.” Sensors 18.12 (2018)

[4] P. Kocher et al., "Spectre Attacks: Exploiting Speculative Execution," 2019 IEEE Symposium on Security and Privacy (SP), San Francisco, CA, USA, 2019.

[5] Moritz Lipp, Michael Schwarz, Daniel Gruss, Thomas Prescher, Werner Haas, Jann Horn, Stefan Mangard, Paul Kocher, Daniel Genkin, Yuval Yarom, Mike Hamburg, and Raoul Strackx. 2020. Meltdown: reading kernel memory from user space. Commun. ACM 63, 6 (June 2020), 46–56.

[6] Daniel Moghimi, Jo Van Bulck, Nadia Heninger, Frank Piessens, and Berk Sunar. 2020. COPYCAT: controlled instruction-level attacks on enclaves. In Proceedings of the 29th USENIX Conference on Security Symposium (SEC'20). USENIX Association, USA, Article 27, 469–486.

[7] C. -Y. Chen, S. Mohan, R. Pellizzoni, R. B. Bobba and N. Kiyavash, "A Novel Side-Channel in Real-Time Schedulers," 2019 IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS), Montreal, QC, Canada, 2019

[8] Conference: Mitra Nasri, Thidapat Chantem, Gedare Bloom, Ryan M. Gerde,"On the Pitfalls and Vulnerabilities of Schedule Randomization Against Schedule-Based Attacks", IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS),  Montreal, QC, Canada, 16-18 April 2019.

[9] S. Hounsinou, M. Stidd, U. Ezeobi, H. Olufowobi, M. Nasri and G. Bloom, "Vulnerability of Controller Area Network to Schedule-Based Attacks," 2021 IEEE Real-Time Systems Symposium (RTSS), Dortmund, DE, 2021.

[10] N. S. Bülbül and M. Fischer, "Preemptive DoS attacks on Time Sensitive Networks," GLOBECOM 2023 - 2023 IEEE Global Communications Conference, Kuala Lumpur, Malaysia, 2023.

### Defense side
[1] M. -K. Yoon, S. Mohan, C. -Y. Chen and L. Sha, "TaskShuffler: A Schedule Randomization Protocol for Obfuscation against Timing Inference Attacks in Real-Time Systems," 2016 IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS), Vienna, Austria, 2016.

[2] Mengjia Yan, Bhargava Gopireddy, Thomas Shull, and Josep Torrellas. 2017. Secure Hierarchy-Aware Cache Replacement Policy (SHARP): Defending Against Cache-Based Side Channel Atacks. In Proceedings of the 44th Annual International Symposium on Computer Architecture (ISCA '17). Association for Computing Machinery, New York, NY, USA, 347–360.

[3] V. Kiriansky, I. Lebedev, S. Amarasinghe, S. Devadas and J. Emer, "DAWG: A Defense Against Cache Timing Attacks in Speculative Execution Processors," 2018 51st Annual IEEE/ACM International Symposium on Microarchitecture (MICRO), Fukuoka, Japan, 2018.

[4] Ankita Samaddar, Arvind Easwaran, and Rui Tan. 2020. SlotSwapper: a schedule randomization protocol for real-time WirelessHART networks. SIGBED Rev. 16, 4 (December 2019), 32–37. https://doi.org/10.1145/3378408.3378413

[5] Ghada Dessouky, Tommaso Frassetto, and Ahmad-Reza Sadeghi. 2020. HYBCACHE: hybrid side-channel-resilient caches for trusted execution environments. In Proceedings of the 29th USENIX Conference on Security Symposium (SEC'20). USENIX Association, USA, Article 26, 451–468.

[6] Dessouky, Ghada & Stapf, Emmanuel & Mahmoody, Pouya & Gruler, Alexander & Sadeghi, Ahmad-Reza. (2022). Chunked-Cache: On-Demand and Scalable Cache Isolation for Security Architectures. 10.14722/ndss.2022.23110. 

[7] J. Ren et al., "REORDER++: Enhanced Randomized Real-Time Scheduling Strategy Against Side-Channel Attacks," in IEEE Transactions on Network Science and Engineering, vol. 10, no. 6, pp. 3253-3266, Nov.-Dec. 2023.

[8] Zirui Neil Zhao, Adam Morrison, Christopher W. Fletcher, and Josep Torrellas. 2023. Untangle: A Principled Framework to Design Low-Leakage, High-Performance Dynamic Partitioning Schemes. In Proceedings of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 3 (ASPLOS 2023). Association for Computing Machinery, New York, NY, USA, 771–788.

[9] A. Kar, X. Liu, Y. Kim, G. Saileshwar, H. Kim and T. Krishna, "Mitigating Timing-Based NoC Side-Channel Attacks With LLC Remapping," in IEEE Computer Architecture Letters, vol. 22, no. 1, pp. 53-56, Jan.-June 2023.

[10] Arkaprava Sain, Sunandan Adhikary, Ipsita Koley, and Soumyajit Dey. 2025. MAARS: Multi-Rate Attack-Aware Randomized Scheduling for Securing Real-time Systems. In Proceedings of the ACM/IEEE 16th International Conference on Cyber-Physical Systems (with CPS-IoT Week 2025) (ICCPS '25). Association for Computing Machinery, New York, NY, USA, Article 10, 1–12.

# Schedule-Based Cyber Attacks

The security of the real-time embedded systems, due to the increasing connectivity (e.g., Internet of Things), is now more important than ever before. One of the most notable examples of exploiting the security holes in this kind of systems is the remote hijacking of a Jeep’s digital system that led Chrysler to recall 1.4 million vehicles (https://www.bbc.com/news/technology-33650491). The real- time systems are designed to enforce the deterministic runtime behavior: they execute the tasks in a specific order that guarantees the reaction time to external events within strict time limits. Schedule- based attacks exploit the information about the tasks execution order to trigger the attacks at the precise moments of targeted task execution. For instance, a cache-timing attack is more efficient if executed right before and right after the targeted task when its data still stays in the cache. Also, the denial-of-service attacks can be more harmful and more difficult to detect when the victim execution time window is directly targeted. The purpose of this literature review is to identify the threats that are posed to the cyber-physical systems and summarize the existing countermeasures.

**References:**

[1] Chen, Chien-Ying, Monowar Hasan, and Sibin Mohan. “Securing Real-Time Internet-of-Things.” Sensors 18.12 (2018)

[2] M. Nasri, T. Chantem, G. Bloom and R. M. Gerdes, "On the Pitfalls and Vulnerabilities of Schedule Randomization Against Schedule-Based Attacks," 2019 IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS)

[3] Chien-Ying Chen, Rakesh B Bobba, and Sibin Mohan. “Schedule-based side-channel attack in fixed- priority real-time systems”, 2015

[4] Chien-Ying Chen, Sibin Mohan, Rodolfo Pellizzoni, Rakesh B. Bobba, Negar Kiyavash. “A novel side-channel in real-time schedulers.” 2019 IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS)

[5] V. Kiriansky, I. Lebedev, S. Amarasinghe, S. Devadas and J. Emer, "DAWG: A Defense Against Cache Timing Attacks in Speculative Execution Processors," 2018 51st Annual IEEE/ACM International Symposium on Microarchitecture (MICRO), Fukuoka, 2018

**Supervisor**: Alex Züpke (alex.zuepke@tum.de3)

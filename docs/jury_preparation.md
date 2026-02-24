-- EntropyHub – Jury Preparation Notes



(Prepared by Abdulkadir Güler)



--- Executive Summary / Yönetici Özeti

🇬🇧 English



In this project, we focused on building a hybrid entropy generation framework that combines hyperchaotic dynamical systems with a Rust-optimized computational core and a post-quantum cryptographic integration layer.



Our goal was to explore a more complex and future-proof entropy model that goes beyond traditional pseudo-random number generators, especially considering the growing impact of quantum computing on modern cryptography.



🇹🇷 Türkçe



Bu projede, hiperkaotik dinamik sistemleri Rust ile optimize edilmiş bir hesaplama çekirdeği ve post-quantum kriptografik entegrasyon katmanı ile birleştiren hibrit bir entropy üretim yapısı geliştirmeye odaklandık.



Amacımız, özellikle kuantum bilgisayarların kriptografi üzerindeki etkisini göz önünde bulundurarak, klasik PRNG sistemlerinin ötesine geçen daha karmaşık ve geleceğe dayanıklı bir entropy modeli ortaya koymaktı.



--- Problem Definition / Problem Tanımı

🇬🇧 English



Modern cryptographic systems depend heavily on high-quality randomness. During our research, we observed that traditional PRNG systems are deterministic by nature and may become predictable under certain conditions.



Additionally, with the advancement of quantum computing, classical cryptographic assumptions may no longer be sufficient in the near future.



🇹🇷 Türkçe



Modern kriptografik sistemler yüksek kaliteli rastgeleliğe büyük ölçüde bağımlıdır. Yaptığımız incelemelerde geleneksel PRNG sistemlerinin deterministik yapıda olduğunu ve belirli koşullarda tahmin edilebilir hale gelebileceğini gördük.



Ayrıca kuantum bilgisayarların gelişimi ile birlikte klasik kriptografik varsayımların uzun vadede yeterli olmayabileceğini değerlendirdik.



--- Solution Architecture / Çözüm Mimarisi

🇬🇧 English



To address these challenges, we designed EntropyHub with the following components:



A hyperchaotic differential system-based entropy generator



A Rust-optimized core for performance-critical chaotic computations



A Python orchestration and visualization layer



A size-compatible Kyber-768 (ML-KEM-768) post-quantum cryptographic integration



This layered structure allowed us to maintain modularity while ensuring performance and extensibility.



🇹🇷 Türkçe



Bu problemlere yaklaşmak için EntropyHub’ı şu bileşenlerle tasarladık:



Hiperkaotik diferansiyel sistem tabanlı entropy üretimi



Performans kritik kaotik hesaplamalar için Rust ile optimize edilmiş çekirdek



Python tabanlı orkestrasyon ve görselleştirme katmanı



Boyut uyumlu Kyber-768 (ML-KEM-768) post-quantum kriptografik entegrasyon



Bu katmanlı yapı sayesinde hem modülerliği koruduk hem de performans ve genişletilebilirlik sağladık.



-- Technical Differentiation / Teknik Farklılaşma

🇬🇧 English



Instead of relying solely on linear deterministic algorithms, we chose to explore nonlinear chaotic dynamics. Chaotic systems exhibit extreme sensitivity to initial conditions, which makes the generated trajectories significantly harder to predict.



By implementing the computationally intensive part in Rust, we ensured performance efficiency, memory safety, and deterministic control over the system evolution.



🇹🇷 Türkçe



Sadece lineer deterministik algoritmalara bağlı kalmak yerine doğrusal olmayan kaotik dinamikleri kullanmayı tercih ettik. Kaotik sistemler başlangıç koşullarına aşırı hassasiyet gösterdiği için üretilen trajektörilerin tahmin edilmesi çok daha zor hale gelir.



Hesaplama açısından yoğun olan kısmı Rust ile gerçekleştirerek performans verimliliği, bellek güvenliği ve sistem evrimi üzerinde deterministik kontrol sağladık.



-- Post-Quantum Layer / Post-Quantum Katman

🇬🇧 English



We integrated a structural Kyber-768 compatible layer aligned with NIST FIPS 203 parameter sizes. This is not a full mathematical lattice-based implementation, but it demonstrates architectural readiness for post-quantum cryptographic integration within the entropy framework.



🇹🇷 Türkçe



Projeye NIST FIPS 203 parametre boyutları ile uyumlu yapısal bir Kyber-768 katmanı entegre ettik. Bu tam matematiksel lattice tabanlı bir implementasyon değildir; ancak entropy mimarisi içerisinde post-quantum entegrasyona hazır bir yapı sunmaktadır.



-- 60-Second Elevator Pitch

🇬🇧 English



EntropyHub is a hybrid entropy generation system where we combine hyperchaotic dynamics with a Rust-optimized computational core and integrate a post-quantum cryptographic layer. Instead of using classical PRNG logic, we rely on nonlinear chaotic behavior to enhance unpredictability while maintaining high performance. The architecture is modular and designed with future post-quantum security requirements in mind.



🇹🇷 Türkçe



EntropyHub, hiperkaotik dinamikleri Rust ile optimize edilmiş hesaplama çekirdeği ve post-quantum kriptografik katman ile birleştirdiğimiz hibrit bir entropy üretim sistemidir. Klasik PRNG mantığı yerine doğrusal olmayan kaotik davranışları kullanarak tahmin edilemezliği artırmayı hedefledik ve bunu yüksek performans ile destekledik. Mimari, gelecekteki post-quantum güvenlik gereksinimleri göz önünde bulundurularak tasarlanmıştır.



-- Jury Questions \& Answers / Jüri Soruları







❓ Why chaotic systems instead of classical PRNG?



🇬🇧

We wanted to move beyond linear deterministic structures. Chaotic systems offer nonlinear behavior and high sensitivity to initial conditions, which increases unpredictability in entropy generation.



🇹🇷

Lineer deterministik yapılardan uzaklaşmak istedik. Kaotik sistemler doğrusal olmayan davranış ve başlangıç koşullarına yüksek hassasiyet sunduğu için entropy üretiminde tahmin edilemezliği artırır.


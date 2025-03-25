# wazuh-local-rules
Wazuh için Türkçeleştirilmiş ve özelleştirilmiş local rule dosyası
1. Wazuh Nedir ve Neden Önemli? 🔍
Wazuh, açık kaynaklı bir SIEM (Security Information and Event Management) ve XDR (Extended Detection and Response) çözümüdür. Aşağıdaki özellikleriyle kritik güvenlik olaylarını izlemede etkilidir:

Log Toplama ve Korelasyon: Windows Event Loglarını merkezileştirir.
Gerçek Zamanlı Tehdit Tespiti: Özel kurallarla saldırıları anında tespit eder.
MITRE ATT&CK Entegrasyonu: Saldırı tekniklerini haritalandırır.
Neden Özel Kurallar?
Hassas Grup Değişiklikleri: Domain Admins gibi yüksek yetkili gruplardaki değişiklikler.
Bruteforce Saldırıları: Yoğun başarısız oturum açma girişimleri.
Hesap Manipülasyonu: Yetkisiz hesap oluşturma/silme.

Dosya Yolu: /var/ossec/etc/rules/

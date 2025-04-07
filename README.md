# Wazuh Local Rules

Bu repo, Wazuh SIEM altyapısı için geliştirilmiş özel `local_rules.xml` dosyalarını içerir. Yerel ağ ortamına ve güvenlik ihtiyaçlarına göre özelleştirilmiş kurallar sayesinde, log analizi ve uyarı sistemi daha etkili hale getirilir.

## 📁 İçerik

- `local_rules.xml` – Tüm özel kurallar burada tanımlıdır.
- `README.md` – Bu dosya :)
- `rules/` – Belirli uygulamalar, sistemler veya cihazlar için ayrı ayrı tanımlanmış kural dosyaları. (Opsiyonel klasör)

## ⚙️ Kullanım

1. `local_rules.xml` dosyasını aşağıdaki dizine kopyalayın:

```bash
/var/ossec/etc/rules/local_rules.xml
```

2. Dosya değişikliklerinden sonra Wazuh servisini yeniden başlatın:

```bash
systemctl restart wazuh-manager
```

3. Kuralların yüklendiğini doğrulamak için logları kontrol edebilirsiniz:

```bash
tail -f /var/ossec/logs/ossec.log
```

## 🔍 Örnek Kural

```xml
<group name="local,syslog,authentication">
  <rule id="100001" level="10">
    <decoded_as>json</decoded_as>
    <field name="eventid">4625</field>
    <description>Windows failed logon attempt detected (Custom Local Rule)</description>
  </rule>
</group>
```

## 📌 Notlar

- `rule id` numaraları 100000+ seviyesinden başlamalıdır.
- Her kural grubu özgün bir `group name` içermeli ve uygun `level` değeri verilmelidir.
- Bu kurallar varsayılan Wazuh kurallarını override edebilir.

## 🤝 Katkı

Katkı sağlamak isterseniz PR göndermeden önce lütfen aşağıdaki adımları uygulayın:

- Kuralın hangi log kaynağını analiz ettiğini açıklayın.
- Kendi ortamınızda test ettiğinizden emin olun.
- Açıklayıcı bir `description` alanı kullanın.

## 🧑‍💻 Hazırlayan

**Arslan GÜRAL**  
🔗 [arslangural.com.tr](https://arslangural.com.tr)  
🔗 [teknokafe.com](https://teknokafe.com)

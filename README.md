# esm2markdown

## Projenin Amacı ve İşlevi
`esm2markdown`, McAfee ESM (Enterprise Security Manager) korelasyon kurallarının XML formatındaki dışa aktarım dosyalarını insan tarafından okunabilir ve düzenlenebilir Markdown formatına dönüştüren bir Python betiğidir. Bu araç, güvenlik uzmanlarının ve yöneticilerin korelasyon kurallarını daha kolay analiz etmelerine, belgelemelerine ve paylaşmalarına yardımcı olur.

### Neden Gerekli?
- **İnsan Okunabilirliği:** McAfee ESM'den dışa aktarılan korelasyon kuralları XML formatındadır ve bu format karmaşık ve okunması zor olabilir.
- **Dokümantasyon:** Markdown formatı, kuralların dokümantasyonunu oluşturmayı ve sürdürmeyi kolaylaştırır.
- **Görselleştirme:** Araç, korelasyon kurallarının ve eşleşme bloklarının ilişkilerini gösteren diyagramlar oluşturur, bu da kuralların mantığını anlamayı kolaylaştırır.

## Nasıl Kullanılır?

### Gereksinimler
- **Python 3:** Betik Python 3 ile yazılmıştır, bu nedenle sisteminizde Python 3 kurulu olmalıdır.
- **Gereken Python Kütüphaneleri:**
  - `lxml`: XML dosyalarını işlemek için kullanılır.
  - `networkx`: Graf yapıları oluşturmak için kullanılır.
  - `pydot`: Graf çizimleri için kullanılır.
  - **Graphviz**: Diyagramların oluşturulması için gereklidir.

### Kurulum

1. **Python ve Pip'i Kurun:**
   - Eğer sisteminizde yoksa, Python 3 ve pip paket yöneticisini kurun.

2. **Gerekli Kütüphaneleri Yükleyin:**
   ```bash
   pip install lxml networkx pydot

3. **Graphviz'i Kurun:**

   - **Windows:** [Graphviz İndir](https://graphviz.org/download/)
   - **Linux:**
     ```bash
     sudo apt-get install graphviz
     ```
   - **macOS:**
     ```python
     brew install graphviz
     ```

### Betiği Çalıştırma

1. **Betiği İndirin veya Kopyalayın:**
   - Betiği bir `.py` dosyasına kaydedin, örneğin `esm2markdown.py`.

2. **Korelasyon Kuralı XML Dosyasını Hazırlayın:**
   - McAfee ESM'den korelasyon kurallarınızı XML formatında dışa aktarın.

3. **Betiği Çalıştırın:**
   ```python
   python esm2markdown.py <kural_xml_dosyası> <çıkış_dosyası>
   ```

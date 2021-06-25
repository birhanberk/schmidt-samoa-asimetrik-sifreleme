## Hakkında

* Schmidt-Samoa asimetrik şifreleme yöntemi kullanılmıştır.

Alman araştırmacı Katja Schmidt-Samoa tarafından 2005’te oluşturulan Schmidt-Samoa kripto sistemi asimetrik (açık anahtarlı) şifreleme yöntemidir. Büyük sayıları asal çarpanlara ayırma probleminin zorluğuna dayanır.

* Girdi olarak bulunduğu dizindeki plaintext.txt dosyasını alır.
* Kullanıcıdan anahtar uzunluğu istenir. Bu uzunluk plaintext.txt dosyasındaki karakter sayısından en az 4 kat büyük olmalıdır. Aksi taktirde metin kaybedilir.

## Anahtar Üretimi

Rastgele olarak yeterince büyük iki asal sayıları seçilmelidir. Seçilen bu sayıların kareköküne kadar olan asal sayıları bilmediğimiz için bu sayıların asal olup olmadıklarını olasılıksal asal sayı testleri ile öğrenebiliriz.

## Şifreleme

Şifrelenmek istenen, eğer metin ise her bir karakterin sayı karşılığı ikilik sayı sisteminde yazılır. Oluşan sayı onluk sayı sistemine çevrilir ve şifreleme işlemi bu sayı üzerinden yapılarak şifreli metin elde edilir.

## Deşifreleme

Şifrelenen metni çözmek için gizli anahtar ve anahtarları oluşturmak için kullanılan asallar gereklidir.

## Yapı

* **keygen(n)** fonksiyonu publickey.txt ve privatekey.txt dosyaları oluşturur. Bu dosyalara oluşturduğu public key ve private key değerlerini yazar.
* **encrypt(plaintext, publickey)** fonksiyonu plaintext.txt dosyası içerisinde yer alan metni publickey.txt dosyası içinde oluşturulmuş olan public key ile şifreleyip ciphertext.txt dosyasına yazar.
* **decrypt(ciphertext, privatekey)** fonksiyonu ciphertext.txt dosyası içindeki metni privatekey.txt dosyası içindeki private key ile deşifreleyip plaintext2.txt dosyasına yazar. plaintext.txt ve plaintext2.txt dosyalarını karşılaştırıp özdeş olup olmadıklarını çıktı olarak vermektedir.

![Schmidt-Samoa-Algoritması](Schmidt-Samoa-Algoritması.jpg)

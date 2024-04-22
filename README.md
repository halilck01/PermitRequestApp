# PermitRequestApp

Bir firmada bulunan Mavi Yaka, Beyaz Yaka ve Müdürlerin izin talebi yapacakları ve bu taleplerin onaya sunulacağı örnek bir uygulamadır.

## Kullanılan Paket & Ortam Bilgileri
<br>
➢ EntityFramework 8.0.1
<br>
➢ MSSQL
<br>
➢ Ardalis.Result
<br>
➢ AutoMapper

## Yöntemler & Görevler
### Mimari Clean Architecture ve aşağıdaki yöntemler kullanıldı.
<br>
•	Code First yaklaşımı ile DB yaratıldı.
<br>
•	Her bir entity için EntityTypeConfiguration yazıldı.
<br>
•	Sistemdeki her bir Id alanı Guid dir.
<br>
•	LeaveRequest Form numarası üretildi ve ayrıca bir RequestFormNumber isminde bir ComputedColumn ile LRF prefixi ile (LRF-000100) gibi bir RequestFormNumber üretildi.
<br>
•	Kullanıcılar ilk migration sırasında sisteme insert edildi.
<br>
•	Entity – DTO dönüşümleri AutoMapper ile yapıldı.
<br>
•	LeaveRequest tablosundaki CreatedAt ve LastModifiedAt alanları (DateTime) SaveChanges override edilerek otomatik olarak set edildi.
<br>
•	Domain Driven Design yaklaşımı uygulandı ve her bir entitynin create işlemi için Factory function kullanıldı.
<br>
•	CQRS kullanıldı.
<br>
•	Responselar için Ardalis.Result kütüphanesi kullanıldı.
<br>
•	Tasklar içerisinde belirtilen Factory ve Strategy pattern yaklaşımı kullanıldı.

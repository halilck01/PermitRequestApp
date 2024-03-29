# PermitRequestApp

Bir firmada bulunan Mavi Yaka, Beyaz Yaka ve Müdürlerin izin talebi yapacakları ve bu taleplerin onaya sunulacağı örnek bir uygulamadır.

Kullanılan Paket & Ortam Bilgileri
➢ EntityFramework 8.0.1
➢ MSSQL
➢ Ardalis.Result
➢ AutoMapper

Yöntemler & Görevler
Mimari Clean Architecture ve aşağıdaki yöntemler kullanıldı.
•	Code First yaklaşımı ile DB yaratıldı.
•	Her bir entity için EntityTypeConfiguration yazıldı.
•	Sistemdeki her bir Id alanı Guid dir.
•	LeaveRequest Form numarası üretildi ve ayrıca bir RequestFormNumber isminde bir ComputedColumn ile LRF prefixi ile (LRF-000100) gibi bir RequestFormNumber üretildi.
•	Kullanıcılar ilk migration sırasında sisteme insert edildi.
•	Entity – DTO dönüşümleri AutoMapper ile yapıldı.
•	LeaveRequest tablosundaki CreatedAt ve LastModifiedAt alanları (DateTime) SaveChanges override edilerek otomatik olarak set edildi.
•	Domain Driven Design yaklaşımı uygulandı ve her bir entitynin create işlemi için Factory function kullanıldı.
•	CQRS kullanıldı.
•	Responselar için Ardalis.Result kütüphanesi kullanıldı.
•	Tasklar içerisinde belirtilen Factory ve Strategy pattern yaklaşımı kullanıldı.

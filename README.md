# Bahadir-eray-odev2 Material Design
## Uygulama ile Görseller Mevcuttur



https://user-images.githubusercontent.com/57098047/188179033-ded5e73f-8a7b-4be5-89d8-c0c9108c0431.mp4



https://user-images.githubusercontent.com/57098047/188179059-18f68498-c3c8-4e18-bf2b-b22543d625c9.mp4



### Araştırma Eager vs Lazy Filters Nedir?

Lazy Loading, sayfada yer alan bir ögenin ihtiyaç duyulmadığı takdirde çağrılmaması prensibi ile çalışır yani bir nesne örneğinin gerçekten ihtiyaç duyulacağı ana kadar alınmaması ve bekletilmesi amacıyla kullanılır. 

Örneğin, aşağıda verilen sorguyu çalıştırdığımızda, UserDetails tablosu Kullanıcı tablosu ile birlikte yüklenmeyecektir.
```
User usr = dbContext.Users.FirstOrDefault(a => a.UserId == userId);
```
Yalnızca, aşağıda gösterildiği gibi, açıkça aradığınızda yüklenir.
```
UserDeatils ud = usr.UserDetails;
```

### Eager Loading
Lazy Loading’in tam tersi yönde çalışır. Kullanacağımız nesneleri, nesnenin ihtiyaç anından çok önce yaratır ve bekletir. Eager loading Linq sorgusu çalıştırıldığında verilerin tamamını yükler ve hafızaya alır.

Örneğin, bir Kullanıcı tablonuz ve bir KullanıcıDetaylar tablonuz (Kullanıcı tablosuyla ilişkili varlık), o zaman aşağıda verilen kodu yazacaksınız. Burada, kullanıcıyı kullanıcı detayları ile birlikte kullanıcı kimliğine eşit bir ID ile yüklüyoruz.


İki farklı yönteminde kendine göre avantajı ve dezaavantajı vardır bunlar geliştirmekte olduğumuz uygulamanın ihtiyaçlarına göre veri tabanımızın büyüklüğüne göre ve orada ki ilişkilerin çokluğuna göre değişir.

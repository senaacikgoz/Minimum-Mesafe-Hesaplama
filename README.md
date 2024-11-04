# Minimum-Öklid-Mesafesinin-Hesaplanması

Bu proje, iki boyutlu uzayda verilen noktalar arasındaki minimum Öklid mesafesini hesaplamak için geliştirilmiştir. Öklid mesafesi, iki nokta arasındaki düz çizgi mesafesini bulmak için kullanılan bir formüldür.

Aşağıda, Python'da minimum Öklid mesafesini hesaplayan kod'a ulaşabilirsiniz.

Kod'un açıklaması:

Noktalar Listesi: points adında bir liste tanımlanmıştır. Bu liste, 2D uzaydaki noktaları (örneğin (x, y)) temsil eden demetler içerir. Örneğin, bu kodda points = [(1, 2), (4, 6), (5, 8), (9, 1)] olarak tanımlanmıştır.

Öklid Mesafesi Fonksiyonu: euclideanDistance adlı bir fonksiyon, iki nokta arasındaki Öklid mesafesini hesaplar. İki nokta alır ve formüle göre mesafeyi döndürür.

Mesafelerin Hesaplanması: for döngüsü kullanarak, listedeki her nokta çifti arasındaki mesafe hesaplanır ve distances adlı bir listeye eklenir.

Minimum Mesafenin Bulunması: Tüm nokta çiftleri arasındaki mesafeler hesaplandıktan sonra, distances listesindeki en küçük mesafe min() fonksiyonu ile bulunur ve ekrana yazdırılır.

Bu kodda  points listesi [(1, 2), (4, 6), (5, 8), (9, 1)] şeklinde tanımlandığı için Minimum mesafe: 2.23606797749979'dur.

```python

import math

def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)

points = [(1, 2), (4, 6), (5, 8), (9, 1)]

distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)


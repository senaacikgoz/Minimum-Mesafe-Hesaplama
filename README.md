# Minimum-Öklid-Mesafesinin-Hesaplanması-

Bu proje, iki boyutlu uzayda verilen noktalar arasındaki minimum Öklid mesafesini hesaplamak için geliştirilmiştir. Öklid mesafesi, iki nokta arasındaki düz çizgi mesafesini bulmak için kullanılan bir formüldür.

Aşağıda, Python'da minimum Öklid mesafesini hesaplayan kod'a ulaşabilirsiniz.

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

min_distance = min(distances)
print("Minimum mesafe:", min_distance)



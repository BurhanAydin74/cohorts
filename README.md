
import math

# Noktalar (x, y) formatında tanımlanıyor
points = [(10, -3), (45, -4)]

# Öklid mesafesi hesaplama
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance_value = math.dist(points[i], points[j])
        distances.append((distance_value, points[i], points[j]))

# Minimum mesafeyi bulma
min_distance = min(distances, key=lambda x: x[0])

# Sonuçları yazdırma
print(f"Minimum Öklid mesafesi: {min_distance[0]}")
print(f"Noktalar: {min_distance[1]} ve {min_distance[2]}")

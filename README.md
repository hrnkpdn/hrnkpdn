points = [(1, 2), (3, 4), (5, 6), (7, 8)]  # Örneğin burada 4 adet 2D nokta var

def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)

distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

min_distance = min(distances)

print("İki nokta arasındaki minimum mesafe:", min_distance)


points = [(2, 3), (4, 5), (1, 1), (7, 6), (3, 8), (9, 9)]
def euclidean_distance(point1, point2):
    dx = point2[0] - point1[0]
    dy = point2[1] - point1[1]
    
    distance = (dx ** 2 + dy ** 2) ** 0.5
    
    return distance
distances = []

for i in range(len(points)):
    for j in range(i + 1, len(points)):
        point1 = points[i]
        point2 = points[j]
        distance = euclidean_distance(point1, point2)
        distances.append(distance)
        print(f"Arasındaki mesafe {point1} ve {point2}: {distance:.2f}")
min_distance = min(distances)
print("\nEn küçük mesafe:", min_distance)

def generate_intervals(n, m):
#Генерирует интервалы с заданным количеством и шагом.
    intervals = []
    start = 0
    for i in range(n):
        end = start + m
        intervals.append((start, end))
        start = end  #Следующий старт равен текущему концу
    return intervals
def extract_first_values(intervals):
#Извлекает первые значения каждого интервала.
    first_values = []
    for start, end in intervals:
        first_values.append(start)
    return first_values

#Генерация интервалов
n = 5  # Количество интервалов
m = 4  # Шаг интервала

intervals = generate_intervals(n, m)
print("Сгенерированные интервалы:", intervals)

#Извлечение первых значений
first_values = extract_first_values(intervals)
print("Первые значения каждого интервала:", first_values)

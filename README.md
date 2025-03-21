# AUTODriver
driving
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.speed = 0  # скорость в км/ч
        self.direction = 'North'  # направление (стандартное - Север)

    def accelerate(self, amount):
        """Увеличение скорости"""
        self.speed += amount
        print(f"Скорость увеличена до {self.speed} км/ч.")

    def brake(self, amount):
        """Торможение"""
        self.speed = max(0, self.speed - amount)
        print(f"Скорость уменьшена до {self.speed} км/ч.")

    def turn(self, new_direction):
        """Поворот автомобиля"""
        self.direction = new_direction
        print(f"Автомобиль повернул в сторону {self.direction}.")

    def status(self):
        """Вывод текущего состояния автомобиля"""
        print(f"{self.year} {self.make} {self.model} движется со скоростью {self.speed} км/ч в направлении {self.direction}.")

# Пример использования:
car = Car('Toyota', 'Corolla', 2021)

car.status()  # Текущий статус
car.accelerate(50)  # Ускоряемся до 50 км/ч
car.turn('East')  # Поворачиваем на Восток
car.brake(20)  # Тормозим до 30 км/ч
car.status()  # Проверка состояния после изменений

// mobile_app/lib/models/restaurant_model.dart (Дополнение)

// ... (PriceRange, SafetyRating, AuthenaLicense, OperatingHours, Restaurant - остаются прежними) ...

class RestaurantAvailability {
  final int availableTables;
  final DateTime nextAvailableTime;
  final bool canBookNow;
  
  RestaurantAvailability({
    required this.availableTables,
    required this.nextAvailableTime,
  }) : canBookNow = availableTables > 0;
}

// ... (Добавление в класс Restaurant) ...
class Restaurant {
  // ... (Остальные поля) ...
  final double userScore; // Персонализированная оценка для пользователя
  final RestaurantAvailability? availability; // Статус бронирования
  
  Restaurant({
    // ... (Обязательные поля) ...
    this.userScore = 0.0,
    this.availability,
  });

  factory Restaurant.fromJson(Map<String, dynamic> json) {
    // ... (Парсинг остальных полей) ...
    
    final availabilityJson = json['availability'];
    final availability = availabilityJson != null ? RestaurantAvailability(
      availableTables: availabilityJson['tables'] ?? 0,
      nextAvailableTime: DateTime.parse(availabilityJson['next_time'] ?? DateTime.now().toIso8601String()),
    ) : null;

    return Restaurant(
      // ... (Возврат остальных полей) ...
      userScore: (json['user_score'] as num?)?.toDouble() ?? 0.0,
      availability: availability,
    );
  }

  // Метод для обновления только динамических полей (бронирование, счет)
  Restaurant copyWith({double? userScore, RestaurantAvailability? availability}) {
    return Restaurant(
      id: id, name: name, cuisine: cuisine, latitude: latitude, longitude: longitude, 
      price: price, safetyRating: safetyRating, license: license, hours: hours,
      userScore: userScore ?? this.userScore,
      availability: availability ?? this.availability,
    );
  }
}

// ... (RestaurantFilters остается прежним) ...

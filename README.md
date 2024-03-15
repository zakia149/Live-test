void main() {

  List<Map<String, Object>> fruits = [
    {"name": "Apple", "color": "Red", "price": 2.5},
    {"name": "Banana", "color": "Yellow", "price": 1.0},
    {"name": "Grapes", "color": "Purple", "price": 3.0}
  ];


  print("Original Fruit Details:");
  FruitDetails(fruits);


  applyPriceDiscount(fruits, 10);

  print("\nAfter Applying 10% Discount:");
    FruitDetails(fruits);
}


void FruitDetails(List<Map<String, Object>> fruits) {
  for (var fruit in fruits) {
    print("Name: ${fruit['name']}, Color: ${fruit['color']}, Price: \$${fruit['price']}");
  }
}

void applyPriceDiscount(List<Map<String, Object>> fruits, double discountPercentage) {
  for (var fruit in fruits) {
    double originalPrice = fruit['price'] as double;
    double discountedPrice = originalPrice - (originalPrice * discountPercentage / 100);
    fruit['price'] = discountedPrice;
  }
}


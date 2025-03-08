void analyzeNumbers(List<int> numbers) {
  if (numbers.isEmpty) {
    print('The list is empty.');
    return;
  }

  int sum = numbers.reduce((a, b) => a + b);

  double average = sum / numbers.length;

  int largest = numbers.reduce((a, b) => a > b ? a : b);
  int smallest = numbers.reduce((a, b) => a < b ? a : b);

  int evenCount = numbers.where((num) => num % 2 == 0).length;
  int oddCount = numbers.length - evenCount;

  print('Sum: $sum');
  print('Average: $average');
  print('Largest Number: $largest');
  print('Smallest Number: $smallest');
  print('Count of Even Numbers: $evenCount');
  print('Count of Odd Numbers: $oddCount');
}

void main() {
  
  List<int> myNumbers = [10, 15, -3, 20, -8, 7];
  
  analyzeNumbers(myNumbers);
}

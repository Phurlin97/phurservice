stem;

namespace FactorialCalculator
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Factorial Calculator");
            Console.Write("Enter a non-negative integer: ");

            if (int.TryParse(Console.ReadLine(), out int number) && number >= 0)
            {
                long factorial = CalculateFactorial(number);
                Console.WriteLine($"The factorial of {number} is {factorial}");
            }
            else
            {
                Console.WriteLine("Invalid input. Please enter a non-negative integer.");
            }
        }

        static long CalculateFactorial(int n)
        {
            if (n == 0)
            {
                return 1;
            }
            else
            {
                return n * CalculateFactorial(n - 1);
            }
        }
    }
}


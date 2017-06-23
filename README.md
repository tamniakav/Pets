using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Pets
{
    class Pets
    {
        static void Main(string[] args)
        {
            int days = int.Parse(Console.ReadLine());
            int kgFood = int.Parse(Console.ReadLine());
            double dogFood = double.Parse(Console.ReadLine());
            double catFood = double.Parse(Console.ReadLine());
            double turtleFood = double.Parse(Console.ReadLine());

            double dogNeeded = days * dogFood;
            double catNeeded = days * catFood;
            double turtleNeeded = days * turtleFood;
            turtleNeeded /= 1000.00;

            double allFood = dogNeeded + catNeeded + turtleNeeded;

            if (allFood <= kgFood)
            {
                double foodLeft = Math.Floor(kgFood - allFood);
                Console.WriteLine($"{foodLeft} kilos of food left.");
            }
            else
            {
                double foodNeeded = Math.Ceiling(allFood - kgFood);
                Console.WriteLine($"{foodNeeded} more kilos of food are needed.");
            }
        }
    }
}

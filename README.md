using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace diagramas
{
    class Program
    {
        static void Main(string[] args)
        {
            int n, i, b, j,x,y;
            x = 0;
            y = 5;
            
            Random colors = new Random();

            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("Introduce la tabla que quieras ver y sus anteriores : ");
            Console.ForegroundColor = ConsoleColor.White;
            n = int.Parse(Console.ReadLine());
           
            Console.WriteLine($"Las tablas anteriores a {n} son\n");
            
                for (i = 1; i <= n; i++)
                {
                Console.ForegroundColor = (ConsoleColor)colors.Next(16);
                for (j = 1; j < 11; j++)
                    {
                        b = i * j;
                        Console.WriteLine($"{i} * {j} = {b}");
                        Console.SetCursorPosition(x,y);
                        y++;
                   
                    if (y == 14)
                    {
                        x += 15;
                        y = 4;
                        if (x == 75)
                        {
                            x = 0;
                            y = 15;
                        }
                    }
                    if (y == 25)
                        {
                            x += 15;
                            y = 15;
                        }
                    
                    } 
                  
                }
            
            Console.ReadKey();
        }

    }
}

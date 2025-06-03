using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace tarea3_C
{
    internal class Program
    {
        static int opcion = 0;  // global
        static float num1 = 0, num2 = 0;

        static void Main(string[] args)
        {

             void menu()
            {
                int opcion = 0;   // variable local 

                do
                {

                    Console.WriteLine("1-Suma");
                    Console.WriteLine("2-resta");
                    Console.WriteLine("3-Multiplicacio");
                    Console.WriteLine("4-Division");
                    Console.WriteLine("5-Salir");
                    Console.WriteLine("Digite una opcion");
                    int.TryParse(Console.ReadLine(), out opcion);
                    switch (opcion)
                    {

                        case 1:
                            
                            Console.WriteLine();
                            suma();
                            break;

                        case 2:
                            resta();
                            break;

                        case 3:
                            Console.WriteLine("");
                            multiplicar();
                            break;

                        case 4:
                            dividir(num1, num2);
                            break;

                        case 5: break;
                        default:
                            break;
                    }

                } while (opcion != 5);

            }


            void suma()
            {
                Solicitar();
                 float NT = ( num1 + num2);
                Console.WriteLine($"Suma: "+ NT );
                Console.ReadLine();
                Console.Clear();
            }


             void multiplicar()
            {
                Solicitar();
                float NT = (num1 * num2);
                Console.WriteLine("multiplicar:" + NT );
                Console.ReadLine();
                Console.Clear();

            }


              void dividir(float v1, float v2)
            {
                Solicitar();
                if (v2 == 0)
                {
                    Console.WriteLine("Error: Division por cero no permitida.");
                    return;
                }
                float NT = (num1 / num2);
                Console.WriteLine("division: "+ NT);
                Console.ReadLine();
                Console.Clear();

            }


             void resta()
            {
                Solicitar();
                float NT = (num1 - num2);
                Console.WriteLine("resta: " + NT);
                Console.ReadLine();
                Console.Clear();
            }

             void Solicitar()
            {
                Console.WriteLine("Digite un numero:");
                num1 = float.Parse(Console.ReadLine());
                Console.WriteLine("Digite otro numero:");
                num2 = float.Parse(Console.ReadLine());
            }

            {

                opcion = 10;
                menu();



            }
        }
    }
}

# Problema-de-Collatz-CSharp
Collatz-CSharp

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            
            long valor = 0;
            long contador = 0;
            long numero = 0;
            long contadorAuxiliar = 0;
            long resposta = 0;
            Console.WriteLine("Informe um valor");
            valor = long.Parse(Console.ReadLine());

            for (int i = 1; i < valor; i++)
            {
                contadorAuxiliar = 1;
                numero = i;

                while (numero != 1)
                {
                    if (numero % 2 == 0)
                    {
                        numero = numero / 2;
                    }
                    else
                    {
                        numero = (3 * numero) + 1;
                    }
                    contadorAuxiliar++;
                    if (contadorAuxiliar > contador)
                    {
                        contador = contadorAuxiliar;
                        resposta = i;
                    }
                }
            }

            Console.WriteLine("---------------------------------");
            Console.WriteLine("Resposta: " + resposta);
            Console.WriteLine("Contador: " + contador);
            Console.WriteLine("---------------------------------");


            Console.ReadKey();
        }
    }
}


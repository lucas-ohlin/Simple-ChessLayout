//Lucas Persson Öhlin - Klass (SUT22)
using System;

namespace ChessBoard {
    class Program {

        private static void Main(string[] args) {

            //Default varibles
            char blackSquare = '■';
            char whiteSquare = '□';

            Console.WriteLine("Hur stort bräde?");
            int boardSize = int.Parse(Console.ReadLine());

            Console.WriteLine("\nCustom symboler för rutorna? - Ja eller Nej");
            string answer = Console.ReadLine();

            //Changes blackSquare and whiteSquare from its default variables to custom ones if user writes "ja"
            //Changes the "answer" to lowercase so the check isn't dependent on case sensitivity
            if (answer.ToLower() == "ja") {
                Console.WriteLine("\nSymbol för svarta rutor: \nKan endast skriva in en karaktär.");
                blackSquare = Console.ReadLine()[0]; //Only reads first letter in the line

                Console.WriteLine("\nSymbol för vita rutor: \nKan endast skriva in en karaktär.");
                whiteSquare = Console.ReadLine()[0]; //Only reads first letter in the line
            }

            //Calls the board generation function with three variables for use in generating the board
            BoardGeneration(boardSize, blackSquare, whiteSquare);
        }

        private static void BoardGeneration(int size, char black, char white) {
            //Enables the use of UTF8 encoding which lets use use the UTF8 format so we can use both "□ & ■"
            Console.OutputEncoding = System.Text.Encoding.UTF8;

            //Row generation
            for (int i = 0; i < size; i++) {
                //Coloumn generation 
                for (int j = 0; j < size; j++) {
                    //Checks if sum of i and j are even, returns a value of either 1 or 0
                    //If the sum is even it will return a 1 and colour the square white
                    //Else it will return a 0 and colour in the square black
                    if ((i + j) % 2 == 0)
                        //Console.Write so it prints out on the same line instead of switching
                        Console.Write(white);
                    else
                        Console.Write(black);
                }
                //switches to new line in the console
                Console.WriteLine();
            }

        }

    }

}

# objectandattributes

using System;

namespace Assignment_12_George   // Helen George
{                               // March 2nd, 2021
    // create class            Week 12 Assignment
                            // Create an object, add attributes and print results
    class myPayfile
    {
        // define variables

        private string last_name;
        private string first_name;
        private double gross_pay;

        myPayfile()
        {
        }

        // method to get last name

        public string getLast_Name()

        {
            Console.Write("Enter your last name ");
            last_name = Console.ReadLine();
            return last_name;
        }

        // method to get first name

        public string getFirst_Name()
        {
            Console.Write("Enter the first name ");
            first_name = Console.ReadLine();
            return first_name;
        }

        // method to get gross pay

        public double getGross_Pay()

        {
            Console.Write("Enter your raw pay ");
            double pay = Convert.ToDouble(Console.ReadLine());
            adjustPay(pay);
            return gross_pay;
            
        }
        // method calculates gross pay

        public void adjustPay(double pay)

        {
            gross_pay = pay * 1.2;
            return;

            //adjust the pay by multiplying it by a factor of 1.2
        }



        myPayfile(string fname, string lname, double pay)
        {
            getFirst_Name();
            getLast_Name();
            getGross_Pay();
        }

        static void Main(string[] args)
        {
            // create object
            myPayfile myPayfile = new myPayfile();

            // add attributes to object
            myPayfile.getFirst_Name();
            myPayfile.getLast_Name();
            myPayfile.getGross_Pay();

            // print results

            Console.WriteLine("The adjusted pay is $" + myPayfile.gross_pay + " for " + myPayfile.first_name + myPayfile.last_name);
            Console.Write("Press any key to continue...");
            

           
                                                    
        }
    }
}

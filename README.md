# objectandattributes

using System;

namespace Assignment_12_George
{
    class myPayfile
    {
        private string last_name;
        private string first_name;
        private double gross_pay;

        myPayfile()
        {
        }

        public string getLast_Name()

        {
            Console.Write("Enter your last name ");
            last_name = Console.ReadLine();
            return last_name;
        }

        public string getFirst_Name()
        {
            Console.Write("Enter the first name ");
            first_name = Console.ReadLine();
            return first_name;
        }

        public double getGross_Pay()

        {
            Console.Write("Enter your raw pay ");
            double pay = Convert.ToDouble(Console.ReadLine());
            adjustPay(pay);
            return gross_pay;
            
        }

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
            myPayfile myPayfile = new myPayfile();
            myPayfile.getFirst_Name();
            myPayfile.getLast_Name();
            myPayfile.getGross_Pay();

            Console.WriteLine("The adjusted pay is $" + myPayfile.gross_pay + " for " + myPayfile.first_name + " " + myPayfile.last_name);
            Console.Write("Press any key to continue...");
            

           
                                                    
        }
    }
}

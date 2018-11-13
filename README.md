# Palindrome
This piece of code helps us to identify whether the entered text is a palindrome.
 static void Main()
        {
            // Write the Main Program for Plndrome here... 
            
            string reverse = "";
            string removespace = "";
            string input = Console.ReadLine().ToUpper().Trim(); //trim space

            for (int i =0; i<input.Length; i++)
            {
                string substring = "";
                substring = input.Substring(i, 1); 

                if ((substring.CompareTo("a") >= 0 && substring.CompareTo("Z") <= 0) ||((substring.CompareTo("0") >= 0 && substring.CompareTo("9") <= 0)))
                {
                    removespace += substring; //remove spaces or other characters from input
                }
            }

            for (int i = removespace.Length-1; i >= 0; i--)
            {
                string substring = "";
                substring = removespace.Substring(i, 1);
                reverse += substring; //reverse the string
            }

            if (reverse.Equals(removespace))
            {
                Console.WriteLine("Palindrome"); //determine if palindrome
            }
            else Console.WriteLine("Not a Palindrome");
            Console.ReadLine();

        }

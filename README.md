# icomparable-interface
using System;<br>

namespace exersice<br>
{<br>
    class Fraction : IComparable<br>
    {<br>
        int z, n;<br>
        public Fraction(int z, int n)<br>
        {<br>
            this.z = z;<br>
            this.n = n;<br>
        }<br>
        public static Fraction operator +(Fraction a, Fraction b)<br>
        {<br>
            return new Fraction(a.z * b.n + a.n * b.z, a.n * b.n);<br>
        }<br>
        public static Fraction operator *(Fraction a, Fraction b)<br>
        {<br>
            return new Fraction(a.z * b.z, a.n * b.n);<br>
        }<br>
        public int CompareTo(object obj)<br>
        {<br>
            Fraction f = (Fraction)obj;<br>
            if ((float)z / n < (float)f.z / f.n)<br>
                return -1;<br>
            else if ((float)z / n > (float)f.z / f.n)<br>
                return 1;<br>
            else return 0;<br>
        }<br>
        public override string ToString()<br>
        {<br>
            return z + "/" + n;<br>
        }<br>
    }<br>
    class ICompInterface<br>
    {<br>
        public static void Main()<br>
        {<br>
            Fraction[] a =<br>
            {<br>
                new Fraction(5, 2),<br>
                new Fraction(29, 6),<br>
                new Fraction(4, 5),<br>
                new Fraction(10, 8),<br>
                new Fraction(34, 7)<br>
            };<br>
            Array.Sort(a);<br>
            Console.WriteLine("Implementing the IComparable Interface in" + "Displaying Fraction:");<br>
            foreach (Fraction f in a)<br>
            {<br>
                Console.WriteLine(f + "");<br>
            }<br>
            Console.WriteLine();<br>
            Console.ReadLine();<br>
        }<br>
    }<br>
}<br>

OUTPUT
![Screenshot 2022-02-25 115852](https://user-images.githubusercontent.com/98301023/155665880-fb0cdc2b-3b46-40bc-af86-c419dd26f973.png)






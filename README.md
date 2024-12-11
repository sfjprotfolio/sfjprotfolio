using System.Globalization;
using System.Threading.Channels;

namespace Abstrct_clss
{
    internal class Program
    {
        static void Main(string[] args)
        { 
           Teacher t1 = new Teacher(1,"Fahad",20);
            t1.TeacherDetails();
            t1.Morning();
            t1.sayHi();  
        }
    }

     abstract class Greting{

        abstract public int age { get; set; }
        public void Morning()
        {
            Console.WriteLine("Good Morning");
        }

        public void Evening()
        {
            Console.WriteLine("Good evening");
        }

        public void Night()
        {
            Console.WriteLine("Good night");
        }

        abstract public void sayHi();
         
        
    }
     
    class Teacher : Greting 
    {
        public int id { get; set; }
        public string name { get; set; }
        public override int age { get ; set; }

        public Teacher(int id,string name,int age)
        {
            this.id = id;
            this.name = name;
            this.age = age; 
        }

        public override void sayHi()
        {
            Console.WriteLine($"Hello : {name}");
        }

        public void TeacherDetails()
        {
            Console.WriteLine($"id :{id}");
            Console.WriteLine($"Name : {name}");
            Console.WriteLine($"Age : {age}");
        }
    }

    class Student
    {
        public int id { get; set; }
        public string name { get; set; }

        public Student(int id, string name)
        {
            this.id = id;
            this.name = name;
        }

       

        public void StudentDetails()
        {
            Console.WriteLine($"id :{id}");
            Console.WriteLine($"Name : {name}");
            
        }
    }

}

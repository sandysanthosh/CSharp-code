// Online C# Editor for free
// Write, Edit and Run your C# code using C# Online Compiler

using System;
using System.IO;
using System.Net;

public class HelloWorld
{
    public static void Main(string[] args)
    {
              
string MobileNo = "8668098213";
         string Message = "Your OTP Code is: "+"123456"+". NARUVI";
           HttpWebRequest request = (HttpWebRequest)WebRequest.Create("http://boancomm.net/boansms/boansmsinterface.aspx?mobileno=" + MobileNo + "&smsmsg=" + Message + "&uname=&pwd=&pid=936");
           
             HttpWebResponse response = (HttpWebResponse)request.GetResponse();  
/*String ver = response.ProtocolVersion.ToString();  
StreamReader reader = new StreamReader(response.GetResponseStream() );   
string str = reader.ReadLine();  
while(str != null)  
{  
  Console.WriteLine(str);  
  str = reader.ReadLine();  
}  */
        Console.WriteLine (request);
    }
}

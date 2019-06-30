# .NET-Memories

---

# C# Fundamentals

**.NET**

.NET has a runtime and library

*in CLI:* 

Shows the runtime enviroment.

  ```
  dotnet --info 
  ```

Shows the avaiables templates for start a project

  ```
  dotnet new 
  ```
  
 After create the application, when running the application o root project without passing
 which file is the csproject extension, the dotnet will look for csproject and run

  ```
  dotnet run 
  ```
  
  **.NET Console Aplication**
  
  - main() method it's the initial point being compiled and run it first in a csproject
  - Interpolation instead of concatenation can be used,
  
```
     Ex: Console.WriteLine("Some Content" + args[0] + "!");

        Can use the dollar sign on the beginning of the string and pass the params as variables

     Ex: Console.WriteLine($"Some Content {args[0]} !");
     
        Can be passed a parameter in CLI with dotnet run -- ALOU
        
     Output : Some Content ALOU
     
        And the compile csproject .dll is rebuild from the originial outdated file
 ```

Set a valid information for printing in the console:

```
              if (args.Length > 0)
            {
                Console.WriteLine($"Alou {args} !");
            }
            else
            {
                Console.WriteLine("erro");
            }
```

**C# Sintaxe**

Using List

first have to import like: *using System.Collections.Generic*

to use a List<Type> EX: List<string>

**Create a Grade list an average then**

-Initialize list with the data type inside <double> and values for this List

-if initialiaze the "result" variable with 0.0 can be used in local and outside scopes calling members, if not only in local scopes 

```
    class Program
    {
        static void Main(string[] args)
        {

            List<double> grades = new List<double>() { 7.5, 8.2, 6.5, 10 };

            double result = 0.0;

            foreach (double number in grades)
            {
                result += number;
            }

            result /= grades.Count;

            Console.WriteLine($"The average grade is: {result:N2}");

   
        }
    }
```

**Class and Methods**

- this, Então,a palavra-chave this é usada para identificar o acesso a um membro da própria classe.
```
EX: public class Microsoft
{
	private string WINDOWS_8_1 = "Windows 8.1";
	
	public string GetName()
	{
		//Não é necessário usar a palavra-chave this pois não existe nenhum outro membro próximo com o mesmo nome
		return WINDOWS_8_1;
	}
	
	public void SetName(string WINDOWS_8_1)
	{
		//É necessário usar a palavra-chave this pois há um membro próximo com o mesmo nome (parâmetro 1 - string WINDOWS_8_1)
		this.WINDOWS_8_1 = WINDOWS_8_1;
	}
}
```

- new, The new operator creates a new instance of a type.
- void , void method doesnt return any value
- static uma classe estática não pode ser instanciada.
```
var acesso = new Program();
//Não é possivel acessar dessa forma por ser uma metodo estatico, porem metodos nao estaticos podem ser acessados dessa forma
acesso.Main();
//Pode ser acessado somente se for static, non static não podem ser acessados dessa forma
Program.Main();

```
- public pode ser acessada em todos os lugares em q a classe for instanciada
- private pode ser utilizada apenas na classe existente
- add a new package with nuget, Ex: dotnet add package name




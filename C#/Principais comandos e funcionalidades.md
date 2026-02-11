
             ### VÁRIAVES e CONSTANTES

 
---

             TIPOS
             Númericos (int e double) 
             Literais (string) 
             Lógicos (bool)
 
             SINTAXE PARA SE CRIAR UMA VÁRIAVEL


             1) declara-se o tipo
             2) defini-se o nome
             3) atribuí-se um valor inicial


             int i_idade = 0;
             double d_altura = 0;
             string s_nome = "";
             bool b_valida = false;
             DateTime dt_cadastro = DateTime.MinValue;


             int i_idade = 0;
             double d_altura = 0;
             string s_nome = "Stephany";
             bool b_valida = true;
             DateTime dt_cadastro = DateTime.Now;


 

             OPERADORES
             Relacionais (bool)
             igual --> i_nota ==10;
             maior/igual --> i_nota >= 10;
             menor/igual --> i_nota <= 10;
             maior --> i_nota > 10;
             menor --> i_nota < 10;
             não igual --> i_nota != 10;
 

             Operadores Matemáticos, retornam (Numerais)

             adição --> i_nro1 + i_nro2;
             subtração --> i_nro1 - i_nro2;
             multiplicação --> i_nro1 * i_nro2;
             divisão --> i_nro1 / i_nro2;
             obs: se o segundo número é diferente de 0.

             radiciação --> Math.sqrt(d_altura);
             potenciação --> Math.Pow(d_altura, 5);
 

             O operador '+' em uma string, assume o papel de concatenador
             ou seja, ele junta os strings. ("martelo"+"do"+"thor") --> "martelodothor".

             Operadores Logicos, retornam (bool)

             E (&&) --> (i_nota <= 10 && i_nota >= 1);

             ...|10, 11,... ...120, 121, 122|...

 

             OU (||) --> (i_nota >= 15 || i_nota <= 5);

             ...3, 4, 5|... ...|15, 16, 17...

 

             NEGAÇÃO (!) --> (!(10 == 10))

 

 

             Comandos de saída de console


             SINTAXE


             Console.Write("Escreva a mensagem"); --> Após a escrita, o cursor permanece na mesma linha.

             console.WriteLine("Escreva a mensagem"); --> Após a escrita, o cursor pula para a linha de baixo.


             Características pecúliares do Write

            /n - Marcador de texto para saltar uma linha para baixo

            {x} - placeholder


             SINTAXE /n
             Console.Write("/nEscreva /na mensagem/n"); 
             SINTAXE placeholder

``
            Console.Write("Escreve a mensagem {0}", variável);
            static void Main(string[] args)
            {

            int i_numero = 0;

            Console.Write("O numero é {0}, i_numero")

            }
``
            ## COMANDOS DE ENTRADA DO CONSOLE
            ### SINTAXE
            
            Console.ReadLine(); --> Recebe o valor digitado pelo usuário através do teclado e após o <enter>, o cursor pula para a próxima linha.
            obs: tudo o que é digitado no teclado é string

            Uma variável string recebendo do comando ReadLine não terá problema, pois string recebe string
            ``s_nome = Console.ReadLine ();``
            
            ``b_valida = int.TryParse(Console.ReadLine(), out i_idade);``

````md
# 🧠 Variáveis, Operadores e Console em C#

---

# 🔹 VARIÁVEIS E CONSTANTES

## 📌 Tipos de Dados

### 🔢 Numéricos
- `int`
- `double`

### 📝 Literais
- `string`

### 🔘 Lógicos
- `bool`

### 📅 Datas
- `DateTime`

---

## 🏗 Sintaxe para criar uma variável

1. Declara-se o tipo  
2. Define-se o nome  
3. Atribui-se um valor inicial  

```csharp
int i_idade = 0;
double d_altura = 0;
string s_nome = "";
bool b_valida = false;
DateTime dt_cadastro = DateTime.MinValue;
````

### 📌 Exemplo com valores atribuídos

```csharp
int i_idade = 0;
double d_altura = 0;
string s_nome = "Stephany";
bool b_valida = true;
DateTime dt_cadastro = DateTime.Now;
```

---

# 🔹 OPERADORES

---

## ⚖️ Operadores Relacionais (retornam `bool`)

```csharp
i_nota == 10;   // Igual
i_nota >= 10;   // Maior ou igual
i_nota <= 10;   // Menor ou igual
i_nota > 10;    // Maior
i_nota < 10;    // Menor
i_nota != 10;   // Diferente
```

---

## ➕ Operadores Matemáticos (retornam numéricos)

```csharp
i_nro1 + i_nro2;   // Adição
i_nro1 - i_nro2;   // Subtração
i_nro1 * i_nro2;   // Multiplicação
i_nro1 / i_nro2;   // Divisão (⚠ segundo número ≠ 0)
```

### 🧮 Operações Matemáticas Especiais

```csharp
Math.Sqrt(d_altura);      // Raiz quadrada
Math.Pow(d_altura, 5);    // Potência
```

---

## 🔤 Operador `+` com string

Quando usado com `string`, o `+` vira **concatenador**:

```csharp
"martelo" + "do" + "thor"; 
// Resultado: "martelodothor"
```

---

## 🔗 Operadores Lógicos (retornam `bool`)

### ✅ E (AND) → `&&`

```csharp
(i_nota <= 10 && i_nota >= 1);
```

### 🔀 OU (OR) → `||`

```csharp
(i_nota >= 15 || i_nota <= 5);
```

### ❌ NEGAÇÃO (NOT) → `!`

```csharp
!(10 == 10);
```

---

# 🔹 COMANDOS DE SAÍDA DO CONSOLE

---

## 🖥 `Console.Write()`

Escreve na tela e **permanece na mesma linha**.

```csharp
Console.Write("Escreva a mensagem");
```

---

## 🖥 `Console.WriteLine()`

Escreve na tela e **pula para a próxima linha**.

```csharp
Console.WriteLine("Escreva a mensagem");
```

---

## 📌 Características importantes

### 🔽 Quebra de linha

```csharp
\n
```

Exemplo:

```csharp
Console.Write("\nEscreva \na mensagem\n");
```

---

## 🎯 Placeholder `{0}`

Permite inserir variáveis dentro da string.

```csharp
Console.Write("O número é {0}", i_numero);
```

### 📌 Exemplo completo

```csharp
static void Main(string[] args)
{
    int i_numero = 0;
    Console.Write("O número é {0}", i_numero);
}
```

---

# 🔹 COMANDOS DE ENTRADA DO CONSOLE

---

## 📥 `Console.ReadLine()`

Recebe o valor digitado pelo usuário.

⚠ Tudo digitado pelo teclado é **string**.

```csharp
string s_nome = Console.ReadLine();
```

---

## 🔄 Convertendo valores digitados

Como `ReadLine()` retorna string, é necessário converter:

### 🔢 Convertendo para `int`

```csharp
int i_idade;
bool b_valida = int.TryParse(Console.ReadLine(), out i_idade);
```

* `TryParse` evita erro caso o usuário digite algo inválido
* Retorna `true` ou `false`

---

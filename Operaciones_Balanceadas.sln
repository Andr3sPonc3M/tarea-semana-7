// Tarea Semana 7
// Verificación de operaciones balanceadas 

using System; 
using System.Collections.Generic; 

class Program 
{
    static void Main() 
    {
        // Define una expresión matemática para verificar.
        string expression = "{7+(8*5)-[(9-7)+(4+1)]}"; 
        // Llama a la función IsBalanced y muestra si la fórmula está balanceada o no.
        Console.WriteLine(IsBalanced(expression) ? "La formula esta balanceada." : "La formula no esta balanceada.");
    }
    
    // Método que verifica si la expresión está balanceada.
    static bool IsBalanced(string expression) 
    {
        // Crea una nueva pila para almacenar caracteres.
        Stack<char> stack = new Stack<char>(); 
        // Itera sobre cada carácter en la expresión.
        foreach (char c in expression) 
        {
            // Verifica si el carácter es un símbolo de apertura.
            if (c == '{' || c == '(' || c == '[') 
            {
                // Agrega el símbolo a la pila.
                stack.Push(c); 
            }
            // Verifica si el carácter es un símbolo de cierre.
            else if (c == '}' || c == ')' || c == ']') 
            {
                // Si la pila está vacía, no hay un símbolo de apertura correspondiente.
                if (stack.Count == 0) return false; 
                // Elimina el último símbolo de apertura de la pila.
                char openBrace = stack.Pop(); 
                // Verifica si el par coincide; si no, retorna false.
                if (!IsMatchingPair(openBrace, c)) return false; 
            }
        }
        // Retorna true si la pila está vacía (todas las aperturas tienen cierres).
        return stack.Count == 0; 
    }

    // Método que verifica si los símbolos coinciden.
    static bool IsMatchingPair(char openBrace, char closeBrace) 
    {
        // Compara llaves.
        return (openBrace == '{' && closeBrace == '}') || 
        // Compara paréntesis.
               (openBrace == '(' && closeBrace == ')') || 
               // Compara corchetes.
               (openBrace == '[' && closeBrace == ']');   
    }
}

// Fin del programa.

// Universidad Estatal Amazónica
// Andrés Ponce M.
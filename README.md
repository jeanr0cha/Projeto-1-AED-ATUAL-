# Projeto-1-AED
Criar um sistema que consiste em uma busca do usuário final por um profissional específico entre pedreiro, marceneiro, carpinteiro, onde cada profissional cobra um valor de diária diferente.

# Código padrão para inicalizar.
using System;
using System.Globalization;

# Classe Cliente

class Cliente
{
    private string nome;
    private float telefone;
    private string email;
    
    public Cliente(string n, float t, string e )
    {
        nome = n;
        telefone = t;
        email = e;
    }
       
    public override string ToString()
    {
        return string.Format("\n Por favor, confirme o seus dados para o envio do orçamento: \n Nome: {0}\n Telefone de contato: {1}\n Email: {2}\n", nome, telefone, email);
    }

}

# Classe Orçamento.

class Orcamento
{
    private string nome;
    private string profissao;
    private float preco;  //Valor a ser cobrado por cada profissional de acordo com sua profissão.
    private float contato; //telefone de contato do profissional.

    public Orcamento(string nm, string pr, float vl, float co )
    {
        nome = nm;
        profissao = pr;
        preco = vl;
        contato = co;
    } 
     /*
    public void setPreco(int vetor)
    {
        int[] mao_de_obra = new int[] { 200, 250, 300 };
    }*/

}

# Função main.

namespace Projeto_1_AED_1
{
    class Program
    {
        static void Main(string[] args)

        {
            Console.WriteLine("Informe seu nome: ");
            string nome = Console.ReadLine();

            Console.WriteLine("Informe seu telefone: ");
            string telefone = Console.ReadLine();
            float converte_telefone = float.Parse(telefone, CultureInfo.InvariantCulture.NumberFormat);

            Console.WriteLine("Informe seu email: ");
            string email = Console.ReadLine();

            Console.WriteLine("Qual tamanho aproximado do serviço a ser executado ?: ");
            string medida = Console.ReadLine();
            float converte_medida = float.Parse(medida, CultureInfo.InvariantCulture.NumberFormat);

                                    
            Cliente cliente1 = new Cliente(nome, converte_telefone, email);


            Orcamento joao = new Orcamento("João Silva", "Pedreiro", 200 , 999321233);
        
            
            Console.WriteLine(cliente1);            
            Console.WriteLine("Aperte qualquer tecla para finalzar!");

            int[] mao_de_obra = new int[] { 200, 250, 300 };
            float resultado;

            if (converte_medida >= 40)
            {
                resultado = mao_de_obra[2] * converte_medida;

                Console.WriteLine("O valor aproxmado da mao de obra é:{0}", resultado);

            }

            Console.ReadKey();

        }
    }
}

# Link do vídeo:
https://www.youtube.com/watch?v=brzV8czOlUA

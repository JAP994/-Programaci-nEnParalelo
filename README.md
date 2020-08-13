# -Programaci-nEnParalelo
Programación en paralelo para una Farmacia.
En las clases Medicamento, Proveedor, Cliente, Farmaceutico se aplica paralelismo en la funcion 

public static void Enlistar()
 {
                Console.WriteLine("Total de Clientes: {0}", Clientes.Count());
                Console.WriteLine("--------------NÓMINA DE Clientes--------------");
            Parallel.ForEach(Clientes,(Cliente cliente) => 
            {
                Imprimir(cliente);

            });    
            /*foreach (Cliente cliente in Clientes)
                {
                    Imprimir(cliente);
                }*/
            
 }
 
 Como podemos observar asi seria la función sin aplicar paralelismo
 foreach (Cliente cliente in Clientes)
                {
                    Imprimir(cliente);
                }
                
Y asi seria la función con paralelismo
Parallel.ForEach(Clientes,(Cliente cliente) => 
            {
                Imprimir(cliente);

            }); 


PARA USAR PARALELISMO DEBEMOS IMPORTAR LA LIBRERIA 

using System.Threading.Tasks;

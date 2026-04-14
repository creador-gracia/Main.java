import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        ListaDobleCircular lista = new ListaDobleCircular();
        Scanner sc = new Scanner(System.in);
        int opcion;

        do {
            System.out.println("\nLISTA DOBLEMENTE ENLAZADA CIRCULAR");
            System.out.println("1. Insertar al inicio");
            System.out.println("2. Insertar al final");
            System.out.println("3. Eliminar al inicio");
            System.out.println("4. Eliminar al final");
            System.out.println("5. Buscar elemento");
            System.out.println("6. Imprimir lista");
            System.out.println("7. Salir");
            System.out.print("Seleccione una opción: ");
            opcion = sc.nextInt();

            switch(opcion) {
                case 1:
                    System.out.print("Ingrese dato: ");
                    lista.insertarInicio(sc.nextInt());
                    lista.imprimir();
                    break;
                case 2:
                    System.out.print("Ingrese dato: ");
                    lista.insertarFinal(sc.nextInt());
                    lista.imprimir();
                    break;
                case 3:
                    lista.eliminarInicio();
                    lista.imprimir();
                    break;
                case 4:
                    lista.eliminarFinal();
                    lista.imprimir();
                    break;
                case 5:
                    System.out.print("Ingrese dato a buscar: ");
                    int valor = sc.nextInt();
                    System.out.println(lista.buscar(valor) ? "Encontrado" : "No encontrado");
                    break;
                case 6:
                    lista.imprimir();
                    break;
            }
        } while(opcion != 7);

        sc.close();
    }
}

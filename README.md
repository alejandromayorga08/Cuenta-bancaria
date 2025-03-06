import java.util.Scanner;


public class Main {
    public static void main(String[] args) {

        Scanner teclado = new Scanner(System.in);

        int opc,con,ret,sal,ext,cons;
        String nom;
        String casa;
        String tel;


        do{
            System.out.println("""
                         CUENTA BANCARIA
                                      
                    """);
            System.out.println("Ingrese su nombre: ");
            nom= teclado.next();
            System.out.println("Ingrese su direccion: ");
            casa=teclado.next();
            System.out.println("Ingrese su telefono: ");
            tel=teclado.next();
            System.out.println("Ingrese su saldo: ");
            sal= teclado.nextInt();


        }while(sal<=0 );

        do {
            System.out.println("""
                         *MENU DE OPCIONES*
                    1-Consignar
                    2-Retirar
                    3-Extraccion rapida 
                    4-Consultar saldo
                    5-Salir    
                    
                    """);
            System.out.println("Ingrese la opcion: ");
            opc = teclado.nextInt();

            switch (opc) {
                case 1 -> {
                    System.out.println("Ingrese el valor que desea consignar: ");
                    con = teclado.nextInt();
                    System.out.println("*El valor a sido consignado con exito*");
                    if (con <= 0) {
                        System.out.println("Ingrese un valor valido para consignar");
                    }
                }
                case 2 -> {
                    System.out.println("Ingrese el valor que desea retirar: ");
                    ret = sal - teclado.nextInt();
                    System.out.println("Su retiro ha sido exitoso: " + ret);
                    if (ret > sal) {
                        System.out.println("*Su retiro no puede ser realizado debido a que su saldo es menor*");
                    }
                }
                case 3 -> {
                    System.out.println("*EXTACCION RAPIDA*");
                    ext = (int) (sal-(sal*0.2));
                    System.out.println("Usted acaba de realizar una extraccion rapida de: " + ext);
                    if (sal < 0) {
                        System.out.println(" *No tiene suficiente saldo* ");
                    }
                }
                case 4 -> {
                    System.out.println(" *Verificando saldo*");
                    cons = sal;
                    System.out.println("Su saldo es igual a: " + cons);
                }
            }

        }while(opc!=5);
        System.out.println("*--Factura--*");
        System.out.println("*Nombre:  "+nom);
        System.out.println("*Direccion:  "+casa);
        System.out.println("*Telefono:  "+tel);
        System.out.println("*Saldo:  "+sal);
        System.out.println("* ---------- *");
    }
}







        }while(opc<5);

    }
}

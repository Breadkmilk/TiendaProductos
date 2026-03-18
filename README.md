# TiendaProductos
En esta tienda se aplican codigos como, SWITCH, IF, ELSE,INT,DOUBLE


    
    public static void main(String[] args) {
       Scanner teclado = new Scanner(System.in); 
       

        System.out.println("Ingrese su nombre: ");
        String nombre = teclado.nextLine();
        
        
        System.out.println("Ingrese monto de compra: ");
        double monto = teclado.nextDouble();
       
        System.out.println("----PRODUCTOS----");
        System.out.println("1.-Monitor S/500 (Descuento 25%)");
        System.out.println("2.-Teclado S/200 (Descuento 15%)");
        System.out.println("3.-Mouse S/100   (Descuento 10%)");
        System.out.println("4.-MousePAD S/50 (no aplica descuento)");
        System.out.println("Elija un producto: ");
        int tienda = teclado.nextInt();
        
        double precio = 0;
        double descuento = 0;
        String producto = "";
        
        switch(tienda){
            case 1:
                producto = "Monitor";
                precio = 500;
                descuento = precio * 0.25;
                break;
            case 2:
                producto = "Teclado";
                precio = 200;
                descuento = precio * 0.15;
                break;
            case 3:
                producto = "Mouse";
                precio = 100;
                descuento = precio * 0.10;
                break;
            case 4:
                producto = "MousePAD";
                precio = 50;        
                descuento = precio * 0.00;
                break;
            default:
                System.out.println("Opcion no valida");
                return;

        }
        double total = precio - descuento;
        
        if (monto >= total){
            System.out.println("Nombre del cliente: " + nombre );
            System.out.println("Monto Original: " + monto);
            System.out.println("Descuento aplicado: " + descuento);
            System.out.println("Total a pagar: " + total);
            
        } else {
        
            System.out.println("Dinero Insuficiente");
            
        }
        
        teclado.close();
    }
    
}

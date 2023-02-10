# Practica-1-Laboratorio-IPC1C2023
Ramiro Solórzano Quintana
Carné: 202010237
Introducción a la programación y computación 1
Sección: C
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package com.mycompany.practica1;

import java.util.Scanner;

/**
 *
 * @author ramsq
 */
public class Practica1{

    /**
     * @param args the command line arguments
     */
        
    public static void main(String[] args) {
        // TODO code application logic here
                
        Scanner sn = new Scanner(System.in);
        boolean salir = false;
        boolean salirCredenciales = false;
        boolean c = false;
        int opcion;
        
        String nomcod ="";
        String nomproducto ="";
        int precproducto = 0;
        int numnit = 0;
        int fecha = 0;
        int cantcomprada = 0;
        String nomusuario ="";
        String contra ="";
        String nomcliente ="";
        int total = 0; 
        int descuento = 0;
        
        
        while(!salirCredenciales){
            System.out.println("Ingrese usuario");
            nomusuario = sn.next();
            System.out.println("Ingrese contraseña");
            contra = sn.next();
        if(nomusuario.equals("cajero_202010237") && contra.equals("ipc1_202010237")){
        salirCredenciales = true;
        }else{
            System.out.println("Credenciales incorrectas intente nuevamente");
        }        
        }
        
        while(!salir){
            System.out.println("1, Agregar nuevos productos");
            System.out.println("2, Agregar cupones de descuento");
            System.out.println("3, Realizar ventas");
            System.out.println("4, Realizar reporte");
            System.out.println("5, Emitir factura");
            System.out.println("6, Reporte articulos mas comprados");
            
            opcion = sn.nextInt();
            
            switch(opcion) {
            case 1:
                System.out.println("Ingrese nombre del usuario");
                nomusuario = sn.next();
                System.out.println("Ingrese contraseña");
            case 2:
                System.out.println("Agregar nuevos productos");
                System.out.println("Nombre del producto");
                nomproducto = sn.next();
                System.out.println("Precio del producto");
                precproducto = sn.nextInt();
                break;
            case 3:
                System.out.println("Agregar cupones de descuento");
                System.out.println("Agregar 5% de descuento");
                System.out.println("Agregar 10% de descuento");
                break;
            case 4:
                System.out.println("Realizar ventas");
                System.out.println("Ingrese nombre del producto");
                break;
            case 5:
                System.out.println("Nombre de la empresa: SUPER-25");
                System.out.println("Nombre del cajero: Ramiro Solórzano Quintana");
                System.out.println("Nombre del Cliente: ");
                nomcliente =sn.next();
                System.out.println("Número de Nit:");
                numnit = sn.nextInt();
                System.out.println("Fecha de emisión de la factura");
                fecha = sn.nextInt();
                System.out.println("Listado de productos");
                System.out.println("Nombre de producto:");
                nomproducto =sn.next();
                System.out.println("Precio de producto:");
                precproducto = sn.nextInt();
                System.out.println("Cantidad comprada:");
                cantcomprada =sn.nextInt();
                System.out.println("Total:");
                total =sn.nextInt();
                System.out.println("Subtotal:");
                System.out.println("Porcentaje de descuento:");
                descuento =sn.nextInt();
                System.out.println("Total con descuento");
                total=sn.nextInt();
                
                
                salir = true;
                break;
            case 6:
                System.out.println("Reporte de articulos más comprados");
                break;
            
            default:
                System.out.println("Error. Intente de nuevo");
                
            }
            
        }        
    }
    
}

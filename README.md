# presentacion6
esta incluye manejo de constructies y manejo de archivos de txt


package repaso_contenidos;

/**
 *
 * @author WILDER M
 */
public class manejo_de_excepciones extends Exception{
    
    public manejo_de_excepciones(String mensaje){
        super(mensaje);
    }

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
    }
    
}



programa 2

//en este ya utilizamos constructores


package repaso_contenidos;
import java.io.OptionalDataException;
import java.io.*;

/**
 *
 * @author WILDER M
 */
public class manejo_de_excepciones1 {

   private int numerador;
    private int denominador;
    
    
    public manejo_de_excepciones1(int numerador,int denominador) throws  manejo_de_excepciones{
        
        if (denominador==0){
           
            throw new  manejo_de_excepciones("denominador igual a cero");
        }
      this.numerador =numerador;
      this.denominador = denominador;
           
    }           
        
       
        
        
public void VisualizarOperacion(){
    System.out.println("el resultado de la division es: " + numerador/ denominador);
    
    
}


}




programa 3


package repaso_contenidos;

/**
 *
 * @author WILDER M
 */
public class manejo_de_excepciones2_resultados {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        
        
        try {
           manejo_de_excepciones1 division = new manejo_de_excepciones1 (10,0);
           division.VisualizarOperacion();
           
        } catch ( manejo_de_excepciones oe) {
            
            System.out.println("ha ocurrido un error  ");
            oe.printStackTrace();
        }
    }
    
}


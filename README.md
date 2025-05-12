# POO-II

import java.util.ArrayList;
import java.util.List;

public class GestionDeUsuarios {

    private List<String> usuarios;

    public GestionDeUsuarios() {
        this.usuarios = new ArrayList<>();
    }

    public void agregarUsuario(String usuario) {
        if (usuario.contains("@")) {
            usuarios.add(usuario);
            System.out.println("Usuario agregado: " + usuario);
            guardarEnArchivo(usuario);
        } else {
            System.out.println("Correo inválido");
        }
    }

    private void guardarEnArchivo(String usuario) {
        System.out.println("Guardando en archivo: " + usuario);
    }

    public void generarReporte(String tipo) {
        if (tipo.equals("PDF")) {
            System.out.println("Generando reporte en PDF");
        } else if (tipo.equals("EXCEL")) {
            System.out.println("Generando reporte en Excel");
        } else {
            System.out.println("Formato no soportado");
        }
    }

    public void enviarCorreoBienvenida(String correo) {
        if (correo.contains("@")) {
            System.out.println("Enviando correo de bienvenida a: " + correo);
        }
    }
}

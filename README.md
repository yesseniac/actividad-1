actividad
=========

yessenia.P2
package.yessenia;
Pakimport java.awt.Color;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.*;

public class FrameCurso extends JFrame  {
	
	private JPanel xpanel1, xpanel2, xpanel3;
	JTextField xcamponombre=new JTextField();
	JLabel xnombre=new JLabel("Nombre:");	
	JTextField disconombre= new JTextField();
	JLabel nombredeldisco= new JLabel("Ingrese Titulo de Pelicula:");
	
	JLabel nombreusuario= new JLabel("Ingrese Nombre del Usuario:");
	JLabel contraseña= new JLabel("Ingrese el contraseña");
	JTextField nombreu=new JTextField("Ingrese Nombre");
	JPasswordField claveusuario=new JPasswordField();
	
	String[] genero={"Accion", "Comedia", "Drama", "Terror", "Ficcion"};
	JComboBox listageneros= new JComboBox(genero);
	JLabel listan=new JLabel("Generos de Peliculas");
	
	JLabel precioalquiler=new JLabel("Precio Alquiler");
	JTextField precio=new JTextField("Ingrese Precio en Bolivares");
	
	JButton boton01, boton02, boton03;	
	public  FrameCurso(){		
		JTabbedPane paneldefichas= new JTabbedPane();
		createPanel();
		boton01=new JButton("Ingresar");
		 boton02=new JButton("Borrar");
		 boton03=new JButton("Cerrar Ventana");
		createPanel2();
		createPanel3();
		paneldefichas.addTab("Inicio", null, xpanel1, "Primer Panel");
		paneldefichas.addTab("Ingresos", null, xpanel2, "Ingresos de Discos");
		paneldefichas.addTab("Administracion de Usuarios", null, xpanel3, "Manejo de Usuarios");
		getContentPane().add(paneldefichas);
		getContentPane().setBackground(Color.MAGENTA);	 
		
	}
	public void createPanel(){
		xpanel1=new JPanel();
		xpanel1.setLayout(null);
		xcamponombre.setBounds(150, 100, 150, 25);
		xnombre.setBounds(20, 100, 150, 25);
		xpanel1.add(xcamponombre);
		xpanel1.add(xnombre);		
	}
	public  void createPanel2(){
		ManejadoradeEvento manejador1= new ManejadoradeEvento();
		xpanel2=new JPanel();
		xpanel2.setLayout(null);
		nombredeldisco.setBounds(20,60, 150, 25);
		disconombre.setBounds(180, 60, 150, 25);
		xpanel2.add(disconombre);
		xpanel2.add(nombredeldisco);
		listageneros.setBounds(180, 100, 200, 25);
		xpanel2.add(listageneros);
		listan.setBounds(30, 100, 150, 25);
		xpanel2.add(listan);
		precioalquiler.setBounds(20, 150, 150, 25);
		xpanel2.add(precioalquiler);
		precio.setBounds(150, 150, 150, 25);
		xpanel2.add(precio);
		boton01.setBounds(20, 200, 100, 25);
		boton01.addActionListener(manejador1);
		xpanel2.add(boton01);
		boton02.setBounds(170, 200, 100, 25);
		boton02.addActionListener(manejador1);
		xpanel2.add(boton02);
		boton03.setBounds(300, 200, 150, 25);
		boton03.addActionListener(manejador1);
		xpanel2.add(boton03);
		
	}

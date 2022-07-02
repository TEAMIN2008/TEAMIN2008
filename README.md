import java.awt.*;
import java.awt.event.*;
import javax.swing.*;

public class MouseListener extends JFrame{
MouseListener(){
setLayout(null);

JPanel p = new JPanel();
p.setBounds(15,10,100,100);
p.setBackground(Color.red);
add(p);

JPanel p1 = new JPanel();
p1.setBounds(15,150,100,100);
p1.setBackground(Color.yellow);
add(p1);

JPanel p2 = new JPanel();
p2.setBounds(15,300,100,100);
p2.setBackground(Color.blue);
add(p2);

JPanel p3 = new JPanel();
p3.setBounds(190,10,250,400);
p3.setBackground(Color.white);
add(p3);

JButton b = new JButton("Exit");
b.setBounds(370,420,100,30);
add(b);

b.addActionListener(new ActionListener(){
public void actionPerformed(ActionEvent e){
       System.exit(0);
}
});

p.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseEntered(MouseEvent e) {
   p.setCursor(Cursor.getPredefinedCursor(Cursor.HAND_CURSOR)); 
     p.setBackground(Color.red);
     
    }
});  
     
              
p.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseExited(MouseEvent e) {
   
      p.setBackground(Color.red);
     
    }
});

p.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseClicked(MouseEvent e) {       
    p3.setBackground (Color.red);

    }
}); 

p1.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseEntered(MouseEvent e) {
   p1.setCursor(Cursor.getPredefinedCursor(Cursor.HAND_CURSOR)); 
     p1.setBackground(Color.yellow);
     
    }
});  
     
              
p1.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseExited(MouseEvent e) {
   
      p1.setBackground(Color.yellow);
     
    }
});

p1.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseClicked(MouseEvent e) {       
    p3.setBackground (Color.yellow); 

    }
}); 

p2.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseEntered(MouseEvent e) {
   p2.setCursor(Cursor.getPredefinedCursor(Cursor.HAND_CURSOR)); 
     p2.setBackground(Color.blue);
     
    }
});  
     
              
p2.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseExited(MouseEvent e) {
   
      p2.setBackground(Color.blue);
     
    }
});

p2.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseClicked(MouseEvent e) {       
    p3.setBackground (Color.blue); 

    }
}); 

p3.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseEntered(MouseEvent e) {
   p3.setCursor(Cursor.getPredefinedCursor(Cursor.HAND_CURSOR)); 
     p3.setBackground(Color.black);
     
    }
});  
     
              
p3.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseExited(MouseEvent e) {
   
      p3.setBackground(Color.black);
     
    }
});

p3.addMouseListener(new MouseAdapter() {
   @Override
    public void mouseClicked(MouseEvent e) {  
    p.setBackground(Color.black);     
    p1.setBackground (Color.black);
    p2.setBackground(Color.black);
    p3.setBackground(Color.black);
     
    }
}); 

setSize(500,500);
setTitle("MouseListener");
setLocationRelativeTo(null);
setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
setVisible(true);
}

      public static void main(String[]args){
    MouseListener Farme = new MouseListener ();
}
}

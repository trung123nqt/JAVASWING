
package GUI1;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JTextField;
import javax.swing.JLabel;
public class JLabelExample {
	public static void main(String[]args) {
		JFrame frame=new JFrame("JLabel");
		
		JLabel lbl=new JLabel("username:");
		JLabel lbl2=new JLabel("passwork:");
		
		JTextField username=new JTextField("");
		JTextField passwork=new JTextField("");
		
		JButton login=new JButton("Login");
		
		username.setBounds(150, 30, 90, 25);
		passwork.setBounds(150, 90, 90, 25);
		
		lbl.setBounds(30, 30, 90, 40);
		lbl2.setBounds(30, 80, 90, 40);
		
		login.setBounds(100, 200, 200, 50);
		
		login.addActionListener((ActionListener) new ActionListener() {

			@Override
			public void actionPerformed(ActionEvent e) {
				System.out.println(username.getText());
				System.out.println(passwork.getText());
			}
			
		});
		
		frame.add(lbl);
		frame.add(lbl2);
		frame.add(username);
		frame.add(passwork);
		frame.add(login);
		frame.setSize(400,300);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setLocationRelativeTo(null);
		frame.setLayout(null);
		frame.setVisible(true);
	
	}

}


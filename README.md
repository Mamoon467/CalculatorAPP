# CalculatorAPP
 using java basics calculator 
 //Mamoon Ejaz 4545
package calculatorApp;

import java.awt.EventQueue;

import javax.swing.JFrame;
import java.awt.Color;
import javax.swing.JButton;
import java.awt.Font;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.JLabel;
import javax.swing.SwingConstants;
import javax.swing.border.LineBorder;
import javax.swing.UIManager;
public class Calculator {

	private JFrame frame;
	private JLabel Screen;
	private JLabel Ans;
	private double f_number;
	private String opr;
	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Calculator window = new Calculator();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public Calculator() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.getContentPane().setFont(new Font("Tahoma", Font.BOLD, 25));
		frame.getContentPane().setForeground(Color.LIGHT_GRAY);
		frame.getContentPane().setBackground(Color.LIGHT_GRAY);
		frame.setBounds(100, 100, 407, 469);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		JButton btnNewButton = new JButton("0");
		btnNewButton.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"0");
			}
		});
		btnNewButton.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton.setForeground(Color.BLACK);
		btnNewButton.setBounds(0, 386, 89, 33);
		frame.getContentPane().add(btnNewButton);
		
		JButton btnNewButton_1 = new JButton(".");
		btnNewButton_1.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+".");
			}
		});
		btnNewButton_1.setForeground(Color.BLACK);
		btnNewButton_1.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_1.setBounds(99, 386, 89, 33);
		frame.getContentPane().add(btnNewButton_1);
		
		JButton btnNewButton_2 = new JButton("=");
		btnNewButton_2.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				double s_number;
				s_number=Double.parseDouble(Screen.getText());
				Screen.setText (Screen.getText()+"=");
				
				if(opr.equals("+")) {
				Ans.setText(Double.toString(f_number+s_number));
			}
			else if(opr.equals("-")) {
				
			Ans.setText(Double.toString(f_number-s_number));
			}
			else if(opr.equals("*")) {
				Ans.setText(Double.toString(f_number*s_number));
			}
			else {
				Ans.setText(Double.toString(f_number/s_number));
				
			}
			}
		});
		btnNewButton_2.setForeground(Color.BLACK);
		btnNewButton_2.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_2.setBounds(198, 386, 89, 33);
		frame.getContentPane().add(btnNewButton_2);
		
		JButton btnNewButton_3 = new JButton("+");
		btnNewButton_3.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				opr="+";
				f_number=Double.parseDouble(Screen.getText());
				Screen.setText("");
				Screen.setText (Screen.getText()+"+");
			}
		});
		btnNewButton_3.setForeground(Color.BLACK);
		btnNewButton_3.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_3.setBounds(297, 386, 89, 33);
		frame.getContentPane().add(btnNewButton_3);
		
		JButton btnNewButton_4 = new JButton("1");
		btnNewButton_4.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"1");
			}
		});
		btnNewButton_4.setForeground(Color.BLACK);
		btnNewButton_4.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_4.setBounds(0, 326, 89, 33);
		frame.getContentPane().add(btnNewButton_4);
		
		JButton btnNewButton_5 = new JButton("2");
		btnNewButton_5.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"2");
			}
			
		});
		btnNewButton_5.setForeground(Color.BLACK);
		btnNewButton_5.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_5.setBounds(99, 326, 89, 33);
		frame.getContentPane().add(btnNewButton_5);
		
		JButton btnNewButton_6 = new JButton("3");
		btnNewButton_6.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"3");
			}
		});
		btnNewButton_6.setForeground(Color.BLACK);
		btnNewButton_6.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_6.setBounds(198, 326, 89, 33);
		frame.getContentPane().add(btnNewButton_6);
		
		JButton btnNewButton_7 = new JButton("-");
		btnNewButton_7.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				opr="-";
				f_number=Double.parseDouble(Screen.getText());
				Screen.setText("");
				//Screen.setText (Screen.getText()+"-");
			}
		});
		btnNewButton_7.setForeground(Color.BLACK);
		btnNewButton_7.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_7.setBounds(297, 326, 89, 33);
		frame.getContentPane().add(btnNewButton_7);
		
		JButton btnNewButton_8 = new JButton("4");
		btnNewButton_8.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"4");
			}
		});
		btnNewButton_8.setForeground(Color.BLACK);
		btnNewButton_8.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_8.setBounds(0, 274, 89, 33);
		frame.getContentPane().add(btnNewButton_8);
		
		JButton btnNewButton_9 = new JButton("5");
		btnNewButton_9.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"5");
			}
		});
		btnNewButton_9.setForeground(Color.BLACK);
		btnNewButton_9.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_9.setBounds(99, 274, 89, 33);
		frame.getContentPane().add(btnNewButton_9);
		
		JButton btnNewButton_10 = new JButton("6");
		btnNewButton_10.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"6");
			}
		});
		btnNewButton_10.setForeground(Color.BLACK);
		btnNewButton_10.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_10.setBounds(198, 274, 89, 33);
		frame.getContentPane().add(btnNewButton_10);
		
		JButton btnNewButton_11 = new JButton("*");
		btnNewButton_11.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				opr="*";
				f_number=Double.parseDouble(Screen.getText());
				Screen.setText("");
				//Screen.setText (Screen.getText()+"*");
			}
		});
		btnNewButton_11.setForeground(Color.BLACK);
		btnNewButton_11.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_11.setBounds(297, 274, 89, 33);
		frame.getContentPane().add(btnNewButton_11);
		
		JButton btnNewButton_12 = new JButton("7");
		btnNewButton_12.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"7");
			}
		});
		btnNewButton_12.setForeground(Color.BLACK);
		btnNewButton_12.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_12.setBounds(0, 218, 89, 33);
		frame.getContentPane().add(btnNewButton_12);
		
		JButton btnNewButton_13 = new JButton("8");
		btnNewButton_13.setBackground(UIManager.getColor("Button.background"));
		btnNewButton_13.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"8");
			}
		});
		btnNewButton_13.setForeground(Color.BLACK);
		btnNewButton_13.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_13.setBounds(99, 218, 89, 33);
		frame.getContentPane().add(btnNewButton_13);
		
		JButton btnNewButton_14 = new JButton("9");
		btnNewButton_14.setBackground(UIManager.getColor("Button.shadow"));
		btnNewButton_14.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText (Screen.getText()+"9");
			}
		});
		btnNewButton_14.setForeground(Color.BLACK);
		btnNewButton_14.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_14.setBounds(198, 218, 89, 33);
		frame.getContentPane().add(btnNewButton_14);
		
		JButton btnNewButton_15 = new JButton("/");
		btnNewButton_15.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				opr="/";
				f_number=Double.parseDouble(Screen.getText());
				Screen.setText("");
				//Screen.setText (Screen.getText()+"/");
			}
		});
		btnNewButton_15.setForeground(Color.BLACK);
		btnNewButton_15.setFont(new Font("Tw Cen MT", Font.BOLD, 20));
		btnNewButton_15.setBounds(297, 218, 89, 33);
		frame.getContentPane().add(btnNewButton_15);
		
		Screen = new JLabel("");
		Screen.setBorder(new LineBorder(Color.WHITE, 3));
		Screen.setFont(new Font("Tahoma", Font.BOLD, 20));
		Screen.setForeground(Color.BLACK);
		Screen.setBackground(Color.BLACK);
		Screen.setBounds(0, 35, 391, 53);
		frame.getContentPane().add(Screen);
		
		 Ans = new JLabel("");
		 Ans.setBorder(new LineBorder(Color.WHITE, 2));
		 Ans.setBackground(Color.LIGHT_GRAY);
		Ans.setHorizontalAlignment(SwingConstants.RIGHT);
		Ans.setFont(new Font("Tahoma", Font.BOLD, 20));
		Ans.setForeground(Color.WHITE);
		Ans.setBounds(0, 98, 391, 53);
		frame.getContentPane().add(Ans);
		
		JButton btnNewButton_16 = new JButton("ESC");
		btnNewButton_16.setFont(new Font("Tahoma", Font.BOLD, 14));
		btnNewButton_16.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				Screen.setText("");
			}
		});
		btnNewButton_16.setBounds(133, 162, 89, 35);
		frame.getContentPane().add(btnNewButton_16);
		
		JLabel lblNewLabel = new JLabel("Mamoon Ejaz 4545");
		lblNewLabel.setForeground(Color.BLACK);
		lblNewLabel.setBackground(Color.WHITE);
		lblNewLabel.setFont(new Font("Tahoma", Font.BOLD, 20));
		lblNewLabel.setBounds(10, 0, 256, 24);
		frame.getContentPane().add(lblNewLabel);
	}
}

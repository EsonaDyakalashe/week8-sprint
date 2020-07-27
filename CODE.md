# week8-sprint

//import statement
import java.awt.Color;
import java.awt.EventQueue;
import java.awt.Font;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JPanel;
import javax.swing.border.EmptyBorder;

//create class and extend with JFrame
public class OldWindow extends JFrame 
{
	//declare variable
	private JPanel contentPane;

public static void main(String[] args){
Jframe f = new Jframe(“Mzamomtsha Primary School”);
//login button
Jbutton b=new Jbutton(“Login”);
b.setbounds(200,200,95,30);
f.add(b);
f.setSize(500,500);
f.setLayout(null);
f.setVisible(true);

	//password 
JpasswordField  value=new JPasswordField();
Jlabel l1 = new Jlabel(“Password”);
L1.setbounds(30,100,90,40);
Value.setBounds (100,100,100,30);
f.add(l1);
F.add(value);
f.setSize(500,500);
f.setLayout(null);
f.setVisible(true);
//username 
Finally Jlabel label=new label();
Label.setBounds(20,180,200,50);
Jlabel l2 = new Jlabel(“Password”);
L2.setbounds(20,20,80,30);
f.add(l2);
f.setSize(500,500);
f.setLayout(null);
f.setVisible(true);


	EventQueue.invokeLater(new Runnable(){
			public void run(){
				try {
				//Create object of OldWindow
				OldWindow frame = new OldWindow();
					frame.setVisible(true);			
				} 
				catch (Exception e)
				{
				e.printStackTrace();
				}
			}
          });
	}

	/**
	 * Create the frame.
	 */
	public OldWindow()//constructor 
	{
		//set frame title
		setTitle("Old Frame");
		//set default close operation		setDefaultCloseOperation(JFrame.DISPOSE_ON_CLOSE);
		//set bounds of the frame
		setBounds(100, 100, 450, 300);
		//create object of JPanel
		contentPane = new JPanel();
		//set border
		contentPane.setBorder(new EmptyBorder(5, 5, 5, 5));
		//set ContentPane
		setContentPane(contentPane);
		//set null
		contentPane.setLayout(null);
		
		//create object of JButton and set label on it
		JButton btnNewFrame = new JButton("Parent Login");
		//add actionListener
		btnNewFrame.addActionListener(new ActionListener()
		{
			public void actionPerformed(ActionEvent arg0)
			{
		//call the object of NewWindow and set visible true
				NewWindow frame = new NewWindow();
				frame.setVisible(true);
				//set default close operation
				setDefaultCloseOperation(JFrame.DISPOSE_ON_CLOSE);
			}
		});
		//set font of the Button
		btnNewFrame.setFont(new Font("Microsoft YaHei UI", Font.BOLD, 12));
		//set bounds of the Button
		btnNewFrame.setBounds(180, 195, 78, 25);
		//add Button into contentPane
		contentPane.add(btnNewFrame);
		
		//set Label in the frame
JLabel lblThisIsOld = new JLabel("This is Old Frame");
		//set foreground color to the label
		lblThisIsOld.setForeground(Color.BLUE);
		//set font of that label
lblThisIsOld.setFont(new Font("Times New Roman", Font.BOLD | Font.ITALIC, 24));
		//set bound of the label
		lblThisIsOld.setBounds(127, 82, 239, 39);
		//add label to the contentPane
		contentPane.add(lblThisIsOld);
	}
}
	

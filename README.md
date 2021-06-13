import java.awt.Color;
import java.awt.Font;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.SwingConstants;

//implements ActionListener in the calculator//
public class Calculator implements ActionListener{
	
	Boolean operatorClicked=false;//main Operator//
	String oldValue;
	String newValue;
	int operatorNumber;
	float result;
	
	//jFrame and jLabel objects//
	
	JFrame jf;
	JLabel displayLabel;
	JButton sevenButton;
	JButton eightButton;
	JButton nineButton;
	JButton fourButton;
	JButton fiveButton;
	JButton sixButton;
	JButton oneButton;
	JButton twoButton;
	JButton threeButton;
	JButton dotButton;
	JButton zeroButton;
	JButton divisionButton;
	JButton multiButton;
	JButton subButton;
	JButton addButton;
	JButton equaltoButton,clearButton,percentageButton,squareButton;
	
	//Calculator constructor//
	
	public Calculator()
	{
		//Frame configuration//
		
	    jf=new JFrame("Calculator");  
		jf.setLayout(null);
		jf.setSize(350,520);
		jf.setLocation(400,100);
		
		displayLabel=new JLabel();
		displayLabel.setBounds(10,40,315,67);
		displayLabel.setBackground(Color.gray);
		displayLabel.setOpaque(true);
		displayLabel.setHorizontalAlignment(SwingConstants.RIGHT);
		displayLabel.setForeground(Color.black);
		displayLabel.setFont(new Font("Calibri",Font.BOLD,30));
		jf.add(displayLabel);
		
		
		//Numbers Button configuration//
		
		sevenButton=new JButton("7");
		sevenButton.setBounds(10,190,77,50);
		sevenButton.addActionListener(this);
		jf.add(sevenButton);
		
		eightButton=new JButton("8");
		eightButton.setBounds(89,190,77,50);
		eightButton.addActionListener(this);
		jf.add(eightButton);
		
		nineButton=new JButton("9");
		nineButton.setBounds(168,190,77,50);
		nineButton.addActionListener(this);
		jf.add(nineButton);
		
		fourButton=new JButton("4");
		fourButton.setBounds(10,263,77,50);
		fourButton.addActionListener(this);
		jf.add(fourButton);
		
		fiveButton=new JButton("5");
		fiveButton.setBounds(89,263,77,50);
		fiveButton.addActionListener(this);
		jf.add(fiveButton);
		
		sixButton=new JButton("6");
		sixButton.setBounds(168,263,77,50);
		sixButton.addActionListener(this);
		jf.add(sixButton);
		
		oneButton=new JButton("1");
		oneButton.setBounds(10,340,77,50);
		oneButton.addActionListener(this);
		jf.add(oneButton);
		
		twoButton=new JButton("2");
		twoButton.setBounds(89,340,77,50);
		twoButton.addActionListener(this);
		jf.add(twoButton);
		
		threeButton=new JButton("3");
		threeButton.setBounds(168,340,77,50);
		threeButton.addActionListener(this);
		jf.add(threeButton);
		
		dotButton=new JButton(".");
		dotButton.setBounds(10,420,77,50);
		dotButton.addActionListener(this);
		jf.add(dotButton);
		
		zeroButton=new JButton("0");
		zeroButton.setBounds(89,420,77,50);
		zeroButton.addActionListener(this);
		jf.add(zeroButton);
		
		
		//Operator Button configuration//

		clearButton=new JButton("clear");
		clearButton.setBounds(247,130,77,50);
		clearButton.addActionListener(this);
		jf.add(clearButton);
		
		percentageButton=new JButton("%");
		percentageButton.setBounds(168,130,77,50);
		percentageButton.addActionListener(this);
		jf.add(percentageButton);
		
		squareButton=new JButton("x2");
		squareButton.setBounds(89,130,77,50);
		squareButton.addActionListener(this);
		jf.add(squareButton);
		
		divisionButton=new JButton("/");
		divisionButton.setBounds(247,190,77,50);
		divisionButton.addActionListener(this);
		jf.add(divisionButton);
		
		multiButton=new JButton("*");
		multiButton.setBounds(247,263,77,50);
		multiButton.addActionListener(this);
		jf.add(multiButton);
		
		subButton=new JButton("-");
		subButton.setBounds(247,340,77,50);
		subButton.addActionListener(this);
		jf.add(subButton);
		
		addButton=new JButton("+");
		 addButton.setBounds(247,420,77,50);
		 addButton.addActionListener(this);
		jf.add( addButton);
		
		equaltoButton=new JButton("=");
		equaltoButton.setBounds(168,420,77,50);
		equaltoButton.addActionListener(this);
		jf.add(equaltoButton);
		
		
		
		jf.setVisible(true);
		jf.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);	
	}
	
	//Main Function//
	public static void main(String[] args) {
		
		new Calculator();
		
		
	}
	@Override    //actionPreformed function or class Where all the event being happening//
	public void actionPerformed(ActionEvent e) {
		
		if(e.getSource()==sevenButton)//Action of the seven button//
		{
			if(operatorClicked)  //checking that any Operator is clicked//
			{
				displayLabel.setText("7");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"7");
			}
			
			
	    }
		else if(e.getSource()==eightButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("8");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"8");
			}
		}
		else if(e.getSource()==nineButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("9");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"9");
			}
		}
		else if(e.getSource()==fourButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("4");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"4");
			}
		}
		else if(e.getSource()==fiveButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("5");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"5");
			}
		}
		else if(e.getSource()==sixButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("6");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"6");
			}
		}
		else if(e.getSource()==oneButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("1");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"1");
			}
		}
		else if(e.getSource()==twoButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("2");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"2");
			}
		}
		else if(e.getSource()==threeButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("3");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"3");
			}
		}
		else if(e.getSource()==dotButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText(".");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+".");
			}
		}
		else if(e.getSource()==zeroButton)
		{
			if(operatorClicked)
			{
				displayLabel.setText("0");
				operatorClicked=false;
			}
			else
			{
			displayLabel.setText(displayLabel.getText()+"0");
			}
			
			
			//Operations
			
			
		}
		else if(e.getSource()==divisionButton)
		{
			operatorClicked=true;
			oldValue=displayLabel.getText(); //Storing the old value that taken before the operator//
			operatorNumber=1;    //Storing that which operation is taken//
		}
		else if(e.getSource()==multiButton)
		{
			operatorClicked=true;
			oldValue=displayLabel.getText();
			operatorNumber=2;
		}
		else if(e.getSource()==subButton)
		{
			operatorClicked=true;
			oldValue=displayLabel.getText();
			operatorNumber=3;
		}
		else if(e.getSource()==percentageButton)
		{
			operatorClicked=true;
			oldValue=displayLabel.getText();
			operatorNumber=5;
		}
		else if(e.getSource()==addButton)
		{
			operatorClicked=true;
			oldValue=displayLabel.getText();
			operatorNumber=4;
			
			
			
		}
		else if(e.getSource()==clearButton)
		{
			displayLabel.setText("");
		}
		
		
		newValue=displayLabel.getText(); //Storing the New value that taken after the Operator//
		
		
		 if(e.getSource()==squareButton)
			{
				operatorClicked=true;
				oldValue=displayLabel.getText();
				float oldvalueF=Float.parseFloat(oldValue); //converting the string value into float value//
				result=oldvalueF*oldvalueF;      //performing the operation//
				displayLabel.setText(result+"");
			}
		
		if(e.getSource()==equaltoButton)
		{
			
			
		operatorClicked=true;
		
				if(operatorNumber==4)
				{
				float oldvalueF=Float.parseFloat(oldValue);//converting the old string value into float value//
				float newValueF=Float.parseFloat(newValue);//converting the new string value into float value//
				result=oldvalueF+newValueF;   //performing the operation//
			
				displayLabel.setText(result+"");
				}
				else if(operatorNumber==3)
				{
					float oldvalueF=Float.parseFloat(oldValue);
					float newValueF=Float.parseFloat(newValue);
					result=oldvalueF-newValueF;
				
					displayLabel.setText(result+"");
					}
				else if(operatorNumber==2)
				{
					float oldvalueF=Float.parseFloat(oldValue);
					float newValueF=Float.parseFloat(newValue);
					result=oldvalueF*newValueF;
				
					displayLabel.setText(result+"");
					}
				else if(operatorNumber==1)
				{
					float oldvalueF=Float.parseFloat(oldValue);
					float newValueF=Float.parseFloat(newValue);
					result=oldvalueF/newValueF;
				
					displayLabel.setText(result+"");
					}
				else if(operatorNumber==5)
				{
					float oldvalueF=Float.parseFloat(oldValue);
					float newValueF=Float.parseFloat(newValue);
					result=oldvalueF%newValueF;
				
					displayLabel.setText(result+"");
					}
		
			
			
			}
			
	}
}



import java.io.*;
import java.rmi.*;
import java.lang.String;
import java.net.*;
public class Rcli 
{
	public static void main(String args[])
	{
		int Port;
		try
		{		 
                BufferedReader buf=new BufferedReader(new InputStreamReader(System.in));
		System.out.println("Enter the port address");
		Port=Integer.parseInt(buf.readLine());
		Socket s=new Socket("localhost",Port);
		String cmd;
                DataOutputStream out=new DataOutputStream(s.getOutputStream());
		DataInputStream is=new DataInputStream(s.getInputStream());
		System.out.println("Enter the command");
		cmd=buf.readLine();
		out.writeUTF(cmd);
		   cmd=is.readUTF();
		System.out.println(cmd);
		}



		catch(Exception e)
		{
			System.out.println("Error"+e);
		}
	}
}

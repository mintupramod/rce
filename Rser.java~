import java.io.*;
import java.net.*;
import java.lang.Runtime;
import java.lang.Object;
public class Rser
{
	public static void main(String args[])
	{
		int Port;
                String cmd[]=new String[3];
		try
		{
		 BufferedReader buf=new BufferedReader(new InputStreamReader(System.in));
		System.out.println("Enter the port address");
		Port=Integer.parseInt(buf.readLine());
		ServerSocket ss=new ServerSocket(Port);
		Socket s=ss.accept();
	//	{
	//		System.out.println("connection successful");
	//	}
		DataInputStream is=new DataInputStream(s.getInputStream());
		OutputStream out=s.getOutputStream();
                BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
                cmd[0]="/bin/sh";
                cmd[1]="-c";
	        cmd[2]=is.readUTF();	
		Runtime r=Runtime.getRuntime();
		Process p=r.exec(cmd);
		BufferedReader br1=new BufferedReader(new InputStreamReader(p.getInputStream()));
		String str,str1="";
		
                DataOutputStream out1=new DataOutputStream(out);
		while((str=br1.readLine())!=null)){
		str1=str1+str+"\n"; 
		out1.writeUTF(str1);
		System.out.println("The command is" +cmd[2]);
		s.close();
		}
		
		
		catch(Exception e)
		{
			System.out.println("Error"+e);
		}
		
	}
}	


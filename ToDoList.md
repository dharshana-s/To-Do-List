LinkedIn : www.linkedin.com/in/dharshana-sivalingam-aa120125a
# To-Do-List
This code is used for creating a To-do-list app, in which you can add, delete and update the tasks. The coding is done using JAVA language.

	import java.util.*;
	import java.io.InputStreamReader;

	public class ToDoList {
	public static void main(String[] args) 
	{
		int iTasks=0;
		String sTask;
		// TODO Auto-generated method stub
		ArrayList<String> olist = new ArrayList<String>();
		Scanner oSc=new Scanner(System.in);
		System.out.println("Enter Number of Tasks: ");
		iTasks=oSc.nextInt();
		for(int i=0; i<iTasks;i++)
		{
			System.out.println("Enter Task "+ (i+1) +":");
			oSc=new Scanner(System.in);
			sTask=oSc.nextLine();
			olist.add(sTask);
			//i=i+1;
		}
		//Traversing list through Iterator  
		Iterator itr=olist.iterator();  
		while(itr.hasNext())
		{  
		System.out.println(itr.next());  	
		}
		System.out.println("1.Add task\n2.Update task\n3.Delete task");
		int ieditvalue = oSc.nextInt();
		switch(ieditvalue)
		{
		case 1:
			System.out.println("Enter the new task:");
			oSc=new Scanner(System.in);
			sTask=oSc.nextLine();
			olist.add(sTask);
			System.out.println("The task is added successfully");
			Iterator itr1=olist.iterator();  
			while(itr1.hasNext())
			{  
			System.out.println(itr1.next());  	
			}
			break;
		case 2:
			System.out.println("Enter the task number to be updated:");
			int etask = oSc.nextInt();
			System.out.println("Enter the task:");
			oSc=new Scanner(System.in);
			sTask=oSc.nextLine();
			olist.set((etask-1),sTask);
			System.out.println("The task is updated successfully");
			Iterator itr3=olist.iterator();  
			while(itr3.hasNext())
			{  
			System.out.println(itr3.next());  	
			}
			break;
		case 3:
			System.out.println("Enter the Task number to be deleted:");
			int dtask=oSc.nextInt();
			olist.remove(dtask-1); 
			System.out.println("The task has been removed successfully");
			Iterator itr2=olist.iterator();  
			while(itr2.hasNext())
			{  
			System.out.println(itr2.next());  	
			}
			break;
		default:
			System.out.println("No such operation");
			break;
		
		}
		
	}
	}

# datastructures
 a named location that can be used to store and organise data =data structure
 collction of steps to solve a problem=algorithm
 \why ????
  memory and time efficient 
  interview related
***stack in ds***
  package datastructuresandalgorithms;
import java.util.Stack;

public class stack {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//LIFo
		//VERTICAL TOWER
		//PUSH()
		//POP()
		Stack <String> stack =new Stack <String>();	
		//push ,pop,peek,search,empty
		
		stack.push("java");
		stack.push("python");
		stack.push("c");
		stack.push("data structures");
		stack.push("javascript");
		//System.out.println(stack.empty());
		System.out.println(stack);
		System.out.println(stack.pop());
		System.out.println(stack.pop());
		System.out.println(stack);
		System.out.println(stack.peek());
		System.out.println(stack.search("python")); 
     //applications of stack 
		//undo/redo  features in text editors
		//moving forward/backward through browser history 
		//backtracking algorithms (maze ,file directories)
		//calling functions (calling stack)
		
	}

}

***queue***
package datastructuresandalgorithms;
import java.util.Queue;
import java.util.LinkedList;

public class queue {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
       Queue<String>queue=new LinkedList<String>();	
       //fifo 
       //head,tail
       //enqueuing,dequeuing ,adding,removing
       //we are taking queue since because we are taking string elements

/*insert
add(e) offer(e) 

Remove
remove() poll() 

Examine
element() peek() */
  queue.offer("siva");
  queue.offer("rekha");
  queue.offer("siva1");
  System.out.println(queue.peek());
  System.out.println(queue.isEmpty());
  System.out.println(queue);
  System.out.println(queue.add("siva2"));
  System.out.println(queue.contains("vasu"));
  System.out.println(queue.size());
  System.out.println(queue.toString());
  //applications 
  //keyboardbuffer 
  //printerqueues
  //linkedlists,priority queues,bfs algorithm
	}
  
  
  

}

siva
false
[siva, rekha, siva1]
true
false
4
[siva, rekha, siva1, siva2]
***priorityqueue***

package datastructuresandalgorithms;
import java.util.*;


public class priorityqueue {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		// a priority queue is a fifo data structure that serves elements with highest priorities
		//first then remaining elements
		Queue<Double> queue=new PriorityQueue<>(Collections.reverseOrder());
		queue.offer(9.0);
		queue.offer(3.9);
		queue.offer(3.2);
		queue.offer(3.6);
		queue.offer(3.1);
		while(!queue.isEmpty())
		{
			System.out.print(queue.poll()+" ");
			 
		}
		System.out.println(" ");
		Queue<Double> queue1=new PriorityQueue<>();
		queue1.offer(9.0);
		queue1.offer(3.9);
		queue1.offer(3.2);
		queue1.offer(3.6);
		queue1.offer(3.1);
		while(!queue1.isEmpty())
		{
			System.out.print(queue1.poll() +" ");
		}
		System.out.println(" ");
		Queue<String> queue2=new PriorityQueue<>();
		queue2.offer("siz");
		queue2.offer("sivbf");
		queue2.offer("sivbz");
		queue2.offer("sivcq");
		queue2.offer("sivda");
		while(!queue2.isEmpty())
		{
			System.out.print(queue2.poll()+ " ");
		}
		System.out.println(" ");
		Queue<Integer> queue3=new PriorityQueue<>();
		queue3.offer(678);
		queue3.offer(786);
		queue3.offer(986);
		queue3.offer(231);
		queue3.offer(986);
		while(!queue3.isEmpty())
		{
			System.out.print(queue3.poll()+ " ");
		}
		System.out.println(" ");
	}
	}
 9.0 3.9 3.6 3.2 3.1  
3.1 3.2 3.6 3.9 9.0  
sivbf sivbz sivcq sivda siz  
231 678 786 986 986  

package datastructuresandalgorithms;
import java.util.LinkedList;

public class linkedlists {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		LinkedList<String> linkedlist =new LinkedList<String>();
		linkedlist.push("a");
		linkedlist.push("b");
		linkedlist.push("d");
		linkedlist.push("e");
		System.out.println(linkedlist);
		System.out.println(linkedlist.pop());
		System.out.println(linkedlist);
		System.out.println(linkedlist);
		linkedlist.offer("a");
		linkedlist.offer("b");
		linkedlist.offer("d");
		linkedlist.offer("e");
		System.out.println(linkedlist);
		System.out.println(linkedlist.poll());
		System.out.println(linkedlist.pop());
		linkedlist.remove(2);
		System.out.println(linkedlist);
		linkedlist.add(3, "c");
		System.out.println(linkedlist);
		System.out.println(linkedlist.);
		
		
	}

}
[e, d, b, a]
e
[d, b, a]
[d, b, a]
[d, b, a, a, b, d, e]
d
b
[a, a, d, e]
[a, a, d, c, e]
//singlelinkedlist =data and address
//double linked list =data previous and next
advantages==dynamic,insertion and deletion is easy 
// low memory usage
disadvantages ==greater memory usage
no random access of elements
accessing and searching takes more time

applications 
1.gps
2.music playlists
3.stack and queue

 ***static array***
 1 capacity is fixed
 2 size can be varied upto the the capacity 
 3.insertion and deletion takes more time for large array
 4.size cannot be changed even if requires
 ***dynamic array***
 1 capacity can be cahanged based upon requirement 
 2.but uses too much memory
 3.memory wastage
 4.insertion and deletion is easy compared to static 
package datastructuresandalgorithms;
//import java.util.DynamicArray;

public class Main{
	
      
 public static void main(String[] args) {
	DynamicArray dynamicarray =new DynamicArray(15);
	dynamicarray.add("a");
	dynamicarray.add("b");
	dynamicarray.add("c");
	System.out.println(dynamicarray);
	System.out.println("empty "+ dynamicarray.isEmpty());
	System.out.println( " size " +dynamicarray.size);
	System.out.println(" capacity "+dynamicarray.capacity);
	
	System.out.println(dynamicarray.get(0));
	dynamicarray.insert(0, " x");
	System.out.println(dynamicarray);
	dynamicarray.delete("a");
	System.out.println(dynamicarray.search("b"));
	System.out.println(dynamicarray);
	dynamicarray.delete("c");
}
}
package datastructuresandalgorithms;

public class DynamicArray {
	int size;
	int capacity =10;
	Object[] array;
	public DynamicArray()
	{
		this.array=new Object[capacity];	
	}
	public DynamicArray(int capacity )
	{
		this.capacity=capacity;
		this.array=new Object[capacity];
	}
	public void add(Object data)
	{
		if(size>=capacity)
		{
			grow();
		}
		array[size]=data;
		size++;
	}
	public void insert(int index,Object data)
	{
		if(size>=capacity)
		{
			grow();
			}
		for(int i=size;i>index;i--)
		{
			array[i]=array[i-1];
		}
		array[index]=data;
		size++;
	}
	public void delete(Object data)
	{
		for (int i=0;i<size;i++)
		{
			if(array[i]== data)
			{
				for(int j=0;j<(size-i-1);j++)
				{
					array[i+j] =array[i+j+1];			
				}
			array[size-1]=null;
			size--;
			if(size<=(int)(capacity/3))
			{
				shrink();
			}
			break;
		}
	}
}
	public int search(Object data)
	{
		for(int i=0;i<size;i++)
		{
			if (array[i]==data)
			{
				return i;
			}
		}
		return -1;
	}
	private void grow()
	{
		int newcapacity =(int)(capacity*2);
		Object[] newarray=new Object[newcapacity];
		for(int i=0;i<size;i++)
		{
			newarray[i]=array[i];
		}
		capacity=newcapacity;
		array=newarray;
				}
	private void shrink()
	{
		int newcapacity =(int)(capacity/2);
		Object[] newarray=new Object[newcapacity];
		for(int i=0;i<size;i++)
		{
			newarray[i]=array[i];
		}
		capacity=newcapacity;
		array=newarray;	
	}
	public boolean isEmpty()
	{
		return size==0;
	}
	public String toString()
	{
		String string="";
		for(int i=0;i<capacity;i++)
		{
			string+=array[i]+" ,";
		}
		if(string!=" ")
		{
			string="["+ string.substring(0,string.length()-2)+" ]";
	}
		else
		{
			string="[]";		}
		return string;
}
	public Object get(int index) {
		// TODO Auto-generated method stub
		return array[index];
	}
}
****linkedlistsversusarraylists***
package datastructuresandalgorithms;
import java.util.ArrayList;
import java.util.LinkedList;
public class linkedlistarraylist {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		LinkedList <Integer>linkedlist =new LinkedList<Integer>();
		ArrayList <Integer>arraylist =new ArrayList<Integer>();
		long starttime;
		long endtime;
		long elapsedtime;
		for(int i=0;i<1000000;i++)
		{
			linkedlist.add(i);
			arraylist.add(i);
		}
		starttime=System.nanoTime();
		//linkedlist.get(0);
		//linkedlist.get(500000);
		//linkedlist.get(999999);
		//linkedlist.remove(0);
		//linkedlist.remove(500000);
		linkedlist.remove(999999);
		endtime =System.nanoTime();
		elapsedtime=endtime-starttime;
		System.out.println(" linkedlist " +elapsedtime);
		starttime=System.nanoTime();
		//arraylist.get(0);
		//arraylist.get(500000);
		//arraylist.get(999999);
		//arraylist.remove(0);
		//arraylist.remove(500000);
		arraylist.remove(999999);
		endtime =System.nanoTime();
		elapsedtime=endtime-starttime;
		System.out.println( " Arraylist "+ elapsedtime);

	}

} 
1.linkedlists takes less time for getting and removing elements at the end than arraylists
2.arraylists took longer time for getting last or first element as it has to move severl elements
***big O notation***
1.describes the performance of an algorithm as the amount of data increases
2.machine independent
3.ignore small operatios
some examples are 
0(1),O(N),O(LOG N).O(N^2)
N=AMOUNT OF DATA
LOOP =MILLIONS RUNS 
NO LOOP LEASS THAN MILLION STEPS
***linearsearch***
package datastructuresandalgorithms;

public class linearsearch {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
    /*linear search =iterates through a collection one element after another 
    run time complexity =O(n)
    dis: slow for large datasets
    adv: 
    	1.fast for searches of small to medium data sets
    	2.no need for sorting
    	3.very useful for data structures that does not have random access*/
      int[] array= {2,6,7,4,3,6,8};
      int index=linearsearch(array,2);
      if(index!=-1)
      {
    	  System.out.println("element found at index" + index);
      }
      else
      {
    	  System.out.println("element does not found");
      }
	}

	private static int linearsearch(int[] array, int value) {
		// TODO Auto-generated method stub
		for(int i=0;i<array.length;i++)
		{
			if(array[i]==value)
			{
				return i;
			}
		
	}return -1;
	}
}
***binarysearchusingarrays (inbuiltfunction)***
package datastructuresandalgorithms;
import java.util.Arrays;

public class binarysearchusingarrays {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//binary search =finds possition of a targeted value with a sorted prder
		int[] array =new int [100];
		int target=42;
		for(int i=0;i<array.length;i++)
		{
			array[i]=i;
		}
		int index=Arrays.binarySearch(array, target);
		if(index==-1)
		{
			System.out.println("target not found");
		}
		else
		{
			System.out.println("element found at index"+ index);
		}

	}

}

package datastructuresandalgorithms;

public class interpolationsearch {

	public static void main(String[] args) {
		// it is animprovement over binary search 
		//it is effiecient for a=search of uniformly distributedelements
		// just like mid is calculated here probe is calculated 
		//based on the probe array is searched
		// average case=O(log(log(n))
		//worst case : O(n)
		int [] array= { 1,4,9,16,25,36,49,64,81,100,121,144,169,196,225};
		int index=interpolationsearch(array,196);
		if(index!=1)
		{
			System.out.println("element found at index" + index);
		}
		
		

	}
	
***interpolationsearch***
	private static int interpolationsearch(int[] array, int value) {
		int low=0;
		int high=array.length-1;
		while((value>=array[low])&& (value <=array[high ])&& low<=high)
		{ 
		int probe=low+(high-low)*(value-array[low])/(array[high]-array[low]);
		System.out.println("probe value"+ probe);
		if(array[probe]==value)
		{
			return probe;
		}
		else if (array[probe]>value)
		{
			high=probe-1;
		}
		else
		{
			low=probe+1;
		}
		
		
	}
		return -1;
	}

}



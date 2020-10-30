# array-implementation-of-stack-and-queue-adt
lab expt 1
class Stack{
static final int max=1000;
int top;
int a[]=new int[max];
boolean isEmpty();
{
  return(top<0);
}
Stack()
{
  top=-1;
}
boolean push(int x)
{ 
  if(top>=(max-1)){
  System.out.println("stack overflow");
  return false;
}
else{
a[++top]=x;
System.out.println(x+"pushed into the stack");
return true;
}
}
int pop()
{ 
  if(top<0){
      System.out.println("stack underflow");
      return 0;
      }
  else{
    int x=a[top--];
    return x;
    }
    }
    int peek()
    {
     if(top<0){
     System.out.println("stack underflow");
     return 0;
     }
     else{
     int x=a[top];
     return x;
     }
     }
     }
     class Queue{
     private static int front,rear,capacity;
     private static int queue();
     Queue(int c)
     {
      front=rear=0;
      capacity=c;
      queue=new int(capacity);
      }
      static void queueEnqueue(int data)
      {
       if(capacity==rear){
       System.out.println("\n queue is full");
       return;
       }
       else{
        queue[rear]=data;
        rear++;
        }
        return;
        }
        static void queueDequeue()
        {
         if(front==rear){
          System.out.println("\n queue is empty");
          return;
          }
          else{
           for(int i=0;i<rear-1;i++)
           {
           queue[i]=queue[i+1];
           }
           if(rear<capacity)
            queue[rear]=0;
            rear--;
            }
            return;
            }
            static void queueDisplay()
            {
            int i;
            if(front==rear){
             System.out.println("\n queue is empty");
             return;
             }
             for(i=front;i<rear;i++){
             System.out.println(queue[i]);
             }
             return;
             }
             static void queueFront()
             {
              if(front==rear){
               System.out.println("queue is empty");
               return;
               }
               System.out.println("\n front element is",queue[front]);
               return;
               }
            public class stackqueuearray{
             public static void main(string args[])
             { 
              Stack s=new Stack();
              s.push(10);
              s.push(20);
              s.push(30);
              System.out.println(s.pop()+"popped from stack");
              Queue q=new Queue();
              q.queueDisplay();
              q.queueEnqueue(20);
              q.queueEnqueue(30);
              q.queueEnqueue(40);
              q.queueEnqueue(50);
              q.queueDisplay();
              q.queueDequeue();
              q.queueDequeue();
              System.out.println("\n After two node deletion");
              q.queueDisplay();
              q.queueFront();
              }
              }
              

//LINKED LISTS
/* Traversal of a linked list
   Searching an element 
   insertiopn of an element 
   deletion of an element
   creation of a linked list 
   reversal of a linked list    */
   
#include<stdio.h>
#include<stdlib.h>

struct node {
	int data;
	struct node *link;
};

struct node *create_list(struct node *start);
void display(struct node *start);
void count(struct node *start);
void search(struct node *start,int data);
struct node *addbeg(struct node *start,int data);
struct node *addend(struct node *start,int data);
struct node *addafter(struct node *start,int data,int item);
struct node *addbefore(struct node *start,int data,int item);
struct node *addatpos(struct node *start,int data,int pos);
struct node *del(struct node *start,int data);
struct node *reverse(struct node *start);

main()
{
	struct node *start=NULL;
	int choice,data,item,pos;
	
	while(1)
	{
		printf("1.create list\n");
		printf("2.display\n");
		printf("3.count\n");
		printf("4.search\n");
		printf("5.add to empty list\n");
		printf("6.add at end\n");
		printf("7.add after node\n");
		printf("8.add befor node\n");
		printf("9.add at the position\n");
		printf("10.delete\n");
		printf("11.reverse\n");
		printf("12.quit\n");
		printf("enter your choice: \n");
		scanf("%d",&choice);
		
	switch(choice)
	{
		case 1:start=create_list(start);
			   break;
		
		case 2:display(start);
			   break;
		
		case 3:count(start);
			   break;
		
		case 4:printf("enter the element to be searched :\n");
				scanf("%d",&data);
				search(start,data);
			   break;
		
		case 5:printf("enter the element to be inserted :\n");
			   scanf("%d",&data);
			   start=addbeg(start,data);
			   break;
		
		case 6:printf("enter the the element to be inserted :\n");
			   scanf("%d",&data);
			   start=addend(start,data);
			   break;
		
		case 7:printf("enter the element to be inserted :\n");
			   scanf("%d",&data);
			   printf("enter the element after which to inserted :\n");
			   scanf("%d",&item);
			   start=addafter(start,data,item);
			   break;	   	   	   	   
		
		case 8:printf("enter the element to be inserted :\n");
			   scanf("%d",&data);
			   printf("enter the element before which to inserted :\n");
			   scanf("%d",&item);
			   start=addbefore(start,data,item);
			   break;
		
		case 9:printf("enter the element to be inserted :\n");
			   scanf("%d",&data);
			   printf("enter the position where the element to be inserted :\n");
			   scanf("%d",&pos);
			   start=addatpos(start,data,pos);
				break;
		
		case 10:printf("enter the element to be deleted :\n");
				scanf("%d",&data);
			    start=del(start,data);
				break;
		
		case 11:start=reverse(start);
			   break;
			   
		case 12:exit(1);
			   break;
			   
		default:printf("wrong choice input given\n");
				break;	   
			   	   	   	   	   	   	   
	}
		
	}
}

struct node *create_list(struct node *start)
{
}

void display(struct node *start)
{
	struct node *p;
	if(start=NULL)
	{ printf("list is empty\n");}
	return;
	p=start;
	printf("list is :");
	while(p!=NULL)
	{
		printf("%d and the address of the pointer is %d>",p->data,&p);
		p=p->link;
	}
	printf("\n\n");
	
}

void count(struct node *start)
{   int count=0;
	struct node *p;
	if(start=NULL)
	{printf("list is empty\n");}
	return;
	p=start;
	printf("total no of elements in the list are:");
	while(p!=NULL)
	{
		p=p->link;
		count++;
	}
	printf("%d ",count);
	printf("\n\n");
}

void search(struct node *start,int item) //keep in mind that sturct node data and this item varible naming are not same
{  int pos=1;
	struct node *p;
	if(start=NULL)
	{
		printf("list is empty no element present\n");
	}
	return;
	p=start;
	while(p!=NULL)
	{
		if(p->data==item)
		{printf("element %d found in the list \n",item);return;}
		p=p->link;
		pos++;
	}
	printf("%d not found in the list",item);return;
}

struct node *addbeg(struct node *start,int item)
{   
	struct node *p;
	p=(struct node*)malloc(sizeof(struct node));
	p->data=item;
	if(start==NULL)
	{
		p->link=NULL;
		start=p;
	}
	p=start;
	p->link=start;
	start=p;
	return start;
}
	
struct node *addend(struct node *start,int item)
{
	struct node *p,*temp;
	p=(struct node*)malloc(sizeof(struct node));
	p->data=item;
	if(start==NULL)
	{
		p->link=NULL;
		start=p;
	}
	p=start;
	while(p!=NULL)
	{   
		p->link=temp;
		temp->link=NULL;
	}	
	return start;
}

struct node *addafter(struct node *start,int data,int item)
{
	struct node *p,*temp;
	p=(struct node*)malloc(sizeof(struct node));
	p->data=data;
	while(p!=NULL)
	{
		if(p->data=item)
		{
		temp->link=p->link;
		p->link=temp;
		return start;
		}
		p=p->link;
	}
	printf("%d not present in the given list",item);
	return start;
}

struct node *addbefore(struct node *start,int data,int item)
{
	struct node *p,*temp;
	p=(struct node*)malloc(sizeof(struct node));
	p->data=data;
	if(item==start->data)
	{
		p->link=start;
		start=p;
		return start;
	}
	p=start;
	while(p!=NULL)
	{
		if(p->link->data==item)
		{
			p->link=temp->link;
			p->link=temp;
			return start;
		}
		p=p->link;
	}
	printf("%d not present in the given list",item);
	return start;
}

struct node *addatpos(struct node *start,int data,int pos)
{	int i=0;
	struct node *p,*temp;
	p=(struct node*)malloc(sizeof(struct node));
	p->data=data;
	if(pos==1)
	{
		p->link=start;
		start=p;
		return start;
	}
	p=start;
	for(i=0;i<(pos-1)&&p!=NULL;i++)
		p=p->link;
	if(p==NULL)
	{
		printf("there are less no of elements than %d in the list.",pos);
	}
	else
	{
		p->link=temp->link;
		p->link=temp;
		
	}
	return start;
}

struct node *del(struct node *start,int data)
{   //there are 4 cases possible when deletion occures it may occur at first node
	//if there is only one node condition.
	//deletion in between the list.
	//deletion at the end.
	struct node *p,*temp;
	if(p->data!=data)
	{
		printf("item is not on the list\n");
	}
	if(start==NULL)
	{
		printf("list is empty\n");
		return start;
	}
	if(start->data=data)
	{
		p=start;
		start=start->link;
		free(p);
		return start;
	}
	p=start;
	while(p!=NULL)
	{
		if(p->link->data==data)
		{
			temp=p->link;
			p->link=temp->link;
			free(temp);
			return start;
		}
		p=p->link;
	printf("element %d is not found in the list bro!!\n",data);
	return start;
	}
}

struct node *reverse(struct node *start)
{
	struct node *prev,*next,*ptr;
	prev=NULL;
	ptr=start;
	while(ptr!=NULL)
	{
		next=ptr->link;
		prev=ptr;
		ptr=next;
	}
	start=prev;
	return start;
}

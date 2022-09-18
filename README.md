# Linkedlist-21108015

#include<iostream>
using namespace std;

struct Node{
    string data;
    Node *prev;
    Node *next;
    Node(string a){
        data=a;
        prev=NULL;
        next=NULL;
    }
};

void print_list(struct Node*node){
    struct Node* last;

    while (node != NULL) {
        cout << node->data << " ";
        last = node;
        node = node->next;
    }
    if (node == NULL){
        cout << "NULL\n";
    }
}



int main(){
    Node *name1= new Node("Rani");
    Node *name2= new Node("Atul");
    Node *name3= new Node("Kavita");
    Node *name4= new Node("Mayank");
    Node *age1= new Node("73");
    Node *age2= new Node("50");
    Node *age3= new Node("42");
    Node *age4= new Node("20");
    name1 -> next= age1;
    age1 -> prev= name1;
    age1 -> next= name2;
    name2 -> next= age2;
    name2 -> prev= age1;
    age2 -> prev= name2;
    age2 -> next= name3;
    name3 -> next= age3;
    name3 -> prev= age2;
    age3 -> prev= name3;
    age3 -> next= name4;
    name4 -> next= age4;
    name4 -> prev= age3;
    age4 -> prev= name4;
    print_list(name1); 
}

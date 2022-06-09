# Struktur-data
Kumpulan pembelajaran matkul struktur data
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package tugastree;

/**
 *
 * @author CBT-GDGI
 */
class Node{
    int data;
    Node kiri, kanan;
    public Node(int d){
    data=d;
    kiri=kanan=null;

}
public static class Tugastree {

   Node root ;
   Tugastree(){
   root=null;
   }
   
   void preorder (Node node){
        if (node==null){
        return;
        }
        System.out.println(node.data);
        preorder(node.kiri);
        preorder (node.kanan); 
   }
           void inorder (Node node){
               if (node==null);{
               return;
               }
            inorder(node.kiri);
            System.out.println(node.data);
            inorder(node.kanan);
           }
                   void postorder(Node node){
                       if (node==null){
                           return;
                       }
                       postorder(node.kiri);
                       postorder(node.kanan);
                       System.out.println(node.data);
                   }
                   public static void main (String[]args){
                       Tugastree tr = new Tugastree();
                       
                       tr.root = new Node(30);
                       tr.root.kiri = new Node(3);
                       tr.root.kanan = new Node (10);
                       tr.root.kanan.kiri = new Node (5);
                       tr.root.kanan.kanan = new Node (2);
                       
                       System.out.println("\n PreOrder");
                       tr.preorder(tr.root);
                       
                       System.out.println("\n InOrder");
                       tr.inorder(tr.root);
                       
                       System.out.println("\n PostOrder");
                       tr.postorder(tr.root);
                   }
}
    
}

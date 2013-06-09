Maximum-Depth-of-Binary-Tree
============================


public class Solution {
    public int maxDepth(TreeNode root) {
        // Start typing your Java solution below
        // DO NOT write main() function
        
       
        
        return depth(root);
    }
    
    public int depth(TreeNode root){
        int left = 0;
        int right = 0;
        
        if(root == null) {return 0;}
      
        
        else{
          left = depth(root.left)+1;
          right = depth(root.right)+1;
        }
        
        return left > right? left:right;
    }
}

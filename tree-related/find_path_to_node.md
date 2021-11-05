```
def getPathToNode(self, root, arr, p):
        x = p.val

        # if root is None there is no path
        if (not root):
            return False

        # push the node's value in 'arr'
        arr.append(root)    

        # if it is the required node
        # return true
        if (root.val == x):    
            return True

        # else check whether the required node
        # lies in the left subtree or right
        # subtree of the current node
        if (self.getPathToNode(root.left, arr, p) or
            self.getPathToNode(root.right, arr, p)):
            return True

        # required node does not lie either in
        # the left or right subtree of the current
        # node. Thus, remove current node's value
        # from 'arr'and then return false    
        arr.pop()
        return False
```


## Binary Search Using Recursive Function
✅ **Programming Language** 

```markdown
   C#
   Data structure 
   Algorithm
   Call stack mechanism.

```

✅ **Binary Search Method** 

```markdown
 //Binary tree search method

static int binarySearch(int[] binaryTree, int left, int right, int itemToSearch)
        {
            if (right >= left)
            {
                //Find the middle of tree
                int mid = left + (right - left) / 2;

                // If the element is present at the
                // middle  then will return middle 
                if (binaryTree[mid] == itemToSearch)
                    return mid;

                // If element is smaller than mid, then
                // it will  only be present in left side of tree
                if (binaryTree[mid] > itemToSearch)
                    return binarySearch(binaryTree, left, mid - 1, itemToSearch);

                // On other cases element will be  present
                // in right side of given tree
                return binarySearch(binaryTree, mid + 1, right, itemToSearch);
            }

            // We will return negative value when searchItem will not be found at tree
            return -1;
        }


```

✅ **Implementation** 


```markdown

int[] binaryTree = { 2, 3, 4, 10, 50, 70 };
//Calculating the lenth of tree
int treeLength = binaryTree.Length;
int left = 0;
int right = treeLength - 1;
int itemToSearch = 10;

int result = binarySearch(binaryTree, left, right, itemToSearch);

if (result == -1)
    Console.WriteLine("Search item not present");
else
    Console.WriteLine("Search item  found at index of " + result);
    Console.ReadLine();
```
## Output


<img src="https://i.stack.imgur.com/tPZXF.gif" alt="user avatar" width="650" height="450" class="bar-sm bar-md d-block">  


public class New {
	static int pinakas[] = new int[]{222, 79, 34, 56, 89};
    
    /* Method to return largest pair sum. */
    static int MaxSum()
    {
        
        int first, second;
        if (pinakas[0] > pinakas[1])
        {
            first = pinakas[0];
            second = pinakas[1];
        }
        else
        {
            first = pinakas[1];
            second = pinakas[0];
        }
      
        
        for (int i = 2; i<pinakas.length; i ++)
        {
            
            if (pinakas[i] > first)
            {
                second = first;
                first = pinakas[i];
            }
      
            
            else if (pinakas[i] > second && pinakas[i] != first)
                second = pinakas[i];
        }
        return (first + second);
    }
    
    public static void main(String[] args) 
    {
         
        System.out.println("Max Sum of two nums is " + MaxSum());
         
    }
}

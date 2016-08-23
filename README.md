# Algorithm

将一个字符串转换成一个整数，要求不能使用字符串转换整数的库函数。
public class Solution {
    public int StrToInt(String str) {
        String symbol ="";
        if(str.startsWith("+") || str.startsWith("-")){
            fuhao = str.substring(0,1);
			str = str.substring(1);
			if(!str.matches("\\d+")){
                System.out.println("0");
                return 0;
            }
		}
        else{
			if(!str.matches("\\d+")){
                System.out.println("0");
                return 0;
			}
		}
	    char[] c =str.toCharArray();
	    int in = 0;
	    for(int i =0;i<str.length();i++){
	        in = in  + (c[str.length() - 1 - i] - '0') * (int) Math.pow(10, i);//10的立方	           
	    }
        if(symbol.equals("-")){
            in = -in;
        }
		return in;
        
    }
}

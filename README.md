# test
my first repository
import java.util.Scanner;

class ThrowAndThrows {
    public static double sqrt(String  nStr) throws Exception {  // throws出现在方法声明中
        if (nStr == null) {
            // throw出现在方法体中，用于抛出一个具体的异常对象
            throw new Exception("输入的字符不能为空！");
        }
        double n = 0;
        try {
            n = Double.parseDouble(nStr);
        }
        catch(NumberFormatException e) {
            throw new Exception("输入的字符串必须能够转化成数字！");
        }
        if (n < 0 ){
            throw new Exception("输入的字符串转化成的数字必须大于0！");
        }
        return Math.sqrt(n);
    }
}

    public static void main(String[] args) {
        boolean f=true;
        while(f) {
            try{
                System.out.print("请输入值：");
                String s=new Scanner(System.in).nextLine();
                System.out.println(new ThrowAndThrows().sqrt(s));
                f=false;
            }catch(Exception e){
                //处理异常
                System.out.println(e.getMessage());
                f=true;
            }
        }
    }

import java.util.concurrent.Callable;

class ComplexNumber {
    int real, image;

    public ComplexNumber(int r, int i) {
        this.real = r;
        this.image = i;
    }

    public void showC() {
        System.out.print(this.real + " +i" + this.image);
    }

    public static ComplexNumber add(ComplexNumber n1, ComplexNumber n2) {
        ComplexNumber res = new ComplexNumber(0, 0);
        res.real = n1.real + n2.real;
        res.image = n1.image + n2.image;
        return res;
    }

    public static void main(String args[]) {
        ComplexNumber c1 = new ComplexNumber(2, 3);
        ComplexNumber c2 = new ComplexNumber(4, 3);
        System.out.println("first Complex number : ");
        c1.showC();
        System.out.println("\nSecond Complex number : ");
        c2.showC();
        ComplexNumber res = add(c1, c2);
        System.out.println("\nAddition is : ");
        res.showC();
    }
}

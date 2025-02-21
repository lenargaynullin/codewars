import java.util.List;

public class BinaryArrayToNumber {

    public static int ConvertBinaryArrayToInt(List<Integer> binary) {
        // Your Code
        String binaryNumber = "";
        for (int num : binary) {
            binaryNumber += num; 
        }
        int decimalNumber = 0;
        for (int i = 0; i < binaryNumber.length(); i++) {
            int index = binaryNumber.length() - 1 - i;
            int value = Character.getNumericValue(binaryNumber.charAt(index));
            decimalNumber += value * Math.pow(2, i);
        }
	  return decimalNumber;
    }
}
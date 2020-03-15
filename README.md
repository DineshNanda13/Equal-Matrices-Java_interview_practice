# Equal-Matrices-Java_interview_practice
Java program to check whether the given two matrices are equal or not
package equal_matrices;

/**
 *
 * @author Dinesh Nanda
 */

/* Both the matrices should have the same number of rows and columns.
   Both the matrices should have the same corresponding elements.
 */
 
public class EqualMatrices {
     
    public static void main(String[] args) {

        int a[][] = {{1, 2, 3}, {8, 4, 6}, {4, 5, 7}};
        int b[][] = {{1, 2, 3}, {8, 4, 6}, {4, 5, 7}};

        int rows_of_a = a.length;
        int cols_of_a = a[0].length;

        int rows_of_b = b.length;
        int cols_of_b = b[0].length;

        if (rows_of_a != rows_of_b || cols_of_a != cols_of_b) {
            System.out.println("Given two matrices are not equal");
        } else {

            boolean flag = true;

            for (int i = 0; i < rows_of_a; i++) {
                for (int j = 0; j < cols_of_a; j++) {

                    if (a[i][j] != b[i][j]) {
                        flag = false;
                    }
                }
            }
            if (flag) {
                System.out.println("Given two matrices are equal");
            } else {
                System.out.println("Given two matrices are not equal");
            }
        }
    }

}

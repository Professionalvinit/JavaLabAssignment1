import java.util.ArrayList;
import java.util.List;

public class  ProgammingAssignment1 {

    public static int getValidRegistrationsCount(List<String> registrationNumbers) {
        int validCount = 0;
        List<String> validDepartments = List.of("CSE", "INFT", "CHEN", "MECH");

        for (String regNumber : registrationNumbers) {
            String year = regNumber.substring(0, 4);
            String department = regNumber.substring(4, 7);
            String sequence = regNumber.substring(7);

            if (validDepartments.contains(department)) {
                validCount++;
            }
        }

        return validCount;
    }

    public static void main(String[] args) {
        List<String> registrationNumbers = new ArrayList<>();
        registrationNumbers.add("2023CSE001");
        registrationNumbers.add("2022INFT002");
         registrationNumbers.add("223MECH005");
        registrationNumbers.add("2025CHEN003");
        registrationNumbers.add("2023ELEC004");
        registrationNumbers.add("2023MECH005");

        int result = getValidRegistrationsCount(registrationNumbers);
        System.out.println("Number of valid registration numbers: " + result);
        }
}

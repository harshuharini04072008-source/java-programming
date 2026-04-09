import java.util.*;

class Policy {
    int policyId;
    String holderName;
    double premiumAmount;
    String dueDate;

    Policy(int policyId, String holderName, double premiumAmount, String dueDate) {
        this.policyId = policyId;
        this.holderName = holderName;
        this.premiumAmount = premiumAmount;
        this.dueDate = dueDate;
    }

    void display() {
        System.out.println("Policy ID: " + policyId);
        System.out.println("Holder Name: " + holderName);
        System.out.println("Premium Amount: " + premiumAmount);
        System.out.println("Due Date: " + dueDate);
        System.out.println("--------------------------");
    }
}

public class InsuranceSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Policy> policies = new ArrayList<>();

        int choice;

        do {
            System.out.println("\n--- Insurance Policy System ---");
            System.out.println("1. Add Policy");
            System.out.println("2. View Policies");
            System.out.println("3. Premium Reminder");
            System.out.println("4. Exit");
            System.out.print("Enter choice: ");
            choice = sc.nextInt();

            switch (choice) {

                case 1:
                    System.out.print("Enter Policy ID: ");
                    int id = sc.nextInt();
                    sc.nextLine();

                    System.out.print("Enter Holder Name: ");
                    String name = sc.nextLine();

                    System.out.print("Enter Premium Amount: ");
                    double amount = sc.nextDouble();
                    sc.nextLine();

                    System.out.print("Enter Due Date (dd-mm-yyyy): ");
                    String date = sc.nextLine();

                    policies.add(new Policy(id, name, amount, date));
                    System.out.println("Policy Added Successfully!");
                    break;

                case 2:
                    if (policies.isEmpty()) {
                        System.out.println("No policies found.");
                    } else {
                        for (Policy p : policies) {
                            p.display();
                        }
                    }
                    break;

                case 3:
                    System.out.print("Enter today's date (dd-mm-yyyy): ");
                    String today = sc.next();

                    System.out.println("\n--- Premium Reminders ---");
                    for (Policy p : policies) {
                        if (p.dueDate.equals(today)) {
                            System.out.println("Reminder: Premium due for " + p.holderName);
                        }
                    }
                    break;

                case 4:
                    System.out.println("Exiting...");
                    break;

                default:
                    System.out.println("Invalid choice!");
            }

        } while (choice != 4);

        sc.close();
    }
}

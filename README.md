# Java-second-year-mini-project
javaFx introduction used 
import javax.swing.*;
import java.util.LinkedHashSet;
import java.util.Scanner;

public class Password {
    public static void main(String[] args) {
        int attempt = 0;

        String username = "bazenga";
        String password = "wearehere";
        String usernameEntered;
        String passwordEntered;
        usernameEntered = (JOptionPane.showInputDialog("Please enter the username"));
        passwordEntered = (JOptionPane.showInputDialog("Please enter the password"));

        if (usernameEntered.equals(username) && passwordEntered.equals(password)) {

            JOptionPane.showMessageDialog(null, "Credentials Match. Welcome Bazenga!");
            LinkedHashSet<String> wood = new LinkedHashSet<String>();
            wood.add("mahogany");
            wood.add("spruce");
            wood.add("teak");
            wood.add("Alder");
            wood.add("Aspen");
            wood.add("Balsa");
            wood.add("Bamboo");
            wood.add("Basswood");
            wood.add("Beechwood");
            wood.add("Birchwood");
            wood.add("California Redwood");
            wood.add("Cedar");
            wood.add("Cherry");
            wood.add("Douglas Fir");
            wood.add("Ebony");
            wood.add("Hard wood");
            wood.add("Hardie board");
            wood.add("Larch");
            wood.add("Luan");
            wood.add("Maple");
            wood.add("MDF");
            wood.add("Oak");
            wood.add("Pine");
            wood.add("Plywood");
            wood.add("Poplar");
            wood.add("Rosewood");
            wood.add("Spruce");
            wood.add("Walnut");
            wood.add("Whitewood");
            wood.add("Zebra");

            System.out.println("We have " + wood.size() + " wood types");
            System.out.println("Our wood types are:" + wood);
            Scanner scan = new Scanner(System.in);
            System.out.println("Enter your wood type");
            String name = scan.nextLine();
            if (wood.contains(name) == true) {
                System.out.println(" Yes, " + name + " is in our wood types ");
                if (wood.contains(name) == true) {
                    Rectangle r1 = new Rectangle();
                    if (wood.contains(name) == wood.add("mahogany")) {
                        Rectangle r2 = new Rectangle();
                        r2.areaOfRectangle();}
                        Scanner scan2 = new Scanner(System.in);
                        System.out.println("Enter number of drawers  ");
                        int drawers = scan.nextInt();
                        if (drawers < 7) {
                            System.out.println("Enter length  ");
                            int length = scan2.nextInt();
                            System.out.println("Enter width  ");
                            int width = scan2.nextInt();
                            r1.insert(length, width, drawers);
                            r1.areaOfRectangle();
                        } else {
                            System.out.println("The number of drawers exceeds our limit ");
                        }
                    }
                } else if (wood.contains(name) == false) {
                    System.out.println("That wood type does not exist");

                }
            } else if (usernameEntered.equals(username)) {

                JOptionPane.showMessageDialog(null, "Password Invalid.");
                attempt++;
                passwordEntered = (JOptionPane.showInputDialog("Please enter the password AGAIN"));

            } else if (passwordEntered.equals(password)) {

                JOptionPane.showMessageDialog(null, "Username Invalid.");
                attempt++;
                usernameEntered = (JOptionPane.showInputDialog("Please enter username AGAIN"));
            } else {

                JOptionPane.showMessageDialog(null, "Both username and password are inncorrect. Who are you");
                attempt++;
                usernameEntered = (JOptionPane.showInputDialog("Please enter username AGAIN"));
                passwordEntered = (JOptionPane.showInputDialog("Please enter password AGAIN"));
            }
            if (attempt == 5) {

                JOptionPane.showMessageDialog(null, "You've reached maximum attempts. Program will now close");


            }

        }
    }


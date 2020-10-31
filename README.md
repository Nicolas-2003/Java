package fr.minikurbaga.user;
import java.util.ArrayList;
import java.util.Scanner;

public class User {


    public static void main(String[] args){

        Userservice user1 = new Userservice("Bob", "Eponge", 45, "waylandjace84@gmail.com", "Instagram,Twitter,Snapchat");
        Userservice user2 = new Userservice("Bernard", "Turta", 63, "fdg", "Instagram,Twitter");
        Userservice user3 = new Userservice("Boyfthb", "Mirut", 32, "waylagfd4@gmail.com", "Instagram,Twitter,Snapchat");


        ArrayList userList = new ArrayList();

        User user = new User();
        userList.add(user1);
        userList.add(user2);
        userList.add(3);









        try(Scanner scanner = new Scanner(System.in)){

            System.out.print( "Veuillez saisir votre prénom : " );
            String name = scanner.nextLine();

            System.out.print( "Veuillez saisir votre nom : " );
            String surname = scanner.nextLine();

            System.out.print( "Veuillez saisir votre E-mail : " );
            String Email = scanner.nextLine();




            if ( name.equals(user1.getName() ) && surname.equals( user1.getSurname()) && Email.equals( user1.getEmail() ) ) {
                System.out.println("user1");
            }
            if ( name.equals(user2.getName() ) && surname.equals( user2.getSurname()) && Email.equals( user2.getEmail() ) ) {
                System.out.println("user2");
            }
            if ( name.equals(user3.getName() ) && surname.equals( user3.getSurname()) && Email.equals( user3.getEmail() ) ) {
                System.out.println("user3");
            }
            if ( !name.equals(user3.getName() )  || !name.equals(user2.getName() )  ||  !name.equals(user1.getName() )  ) {
                System.out.println("Vous n'êtes pas enregistré");

                System.out.print( "Veuillez saisir votre liste des réseaux sociaux que vous aimez : " );
                String list = scanner.nextLine();

                System.out.print( "Veuillez saisir votre age : " );
                int age = scanner.nextInt();

                System.out.println( name + surname+  Email +  list +  age);

                Userservice users = new Userservice(name, surname,  age,  Email,  list);
                userList.add(users);
                System.out.println( user);

            }

            System.out.println("Veulliez remplir le petit questionnaire svp");

            System.out.print( "Veuillez saisir votre liste des réseaux sociaux que vous aimez : " );
            String list = scanner.nextLine();

            System.out.println( "Veuillez saisir votre age : " );
            int age = scanner.nextInt();

            if ( list.equals(user1.getList() ) && age == user1.getAge() ){
                System.out.println("user1");
            }
            if ( list.equals(user2.getList() ) && age == user2.getAge() ){
                System.out.println("user2");
            }
            if ( list.equals(user3.getList() ) && age == user3.getAge() ){
                System.out.println("user3");
            }
            if ( age !=user3.getAge()   || age !=user2.getAge()  ||  age !=user1.getAge()  ) {
                System.out.println("Vous n'êtes pas enregistré");
            }

        }

    }



}

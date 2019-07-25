package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        boolean m=false;
        System.out.println("Здравствуйте, вас привествует банкомат. Вставьте карту.");
            Scanner l = new Scanner(System.in);

            int schet=1000;
            int n=0;
            while(m==false){
                boolean q=false;
                System.out.println("Введите пожалуйста пинкод");
            while(q==false){
            String b=l.next();
            if(b.length()<16||b.length()>16)
            {
                System.out.println("Попробуйте еще раз");
            }
            else{q=true;}}

            System.out.println("Введите , пожалуйста тип операции с вашим балансом:");
            System.out.println("---> Проверить");
            System.out.println("---> Снять");
            System.out.println("---> Пополнить");

            String a=l.next(),f="Проверить",g="Снять",h="Пополнить";
            if(a.equals(h)) {
                System.out.println("Введите сумму, которую вы хотите добавить.");
                int plus = l.nextInt();
                System.out.println("Опперация проведена успешно!");
                schet=schet+plus;
                System.out.println("Ваша баланс на данный момент составляет: " + schet);
            }
            if(a.equals(f)) {
                System.out.println("Ваша баланс на данный момент составляет: " + schet);
            }
            if(a.equals(g)) {
                    System.out.println("Введите сумму, которую вы хотите снять.");
                    int minus=l.nextInt();
                    System.out.println("Опперация проведена успешно!");
                    schet=schet-minus;
                    System.out.println("Ваша баланс на данный момент составляет: " + schet);
            }

            System.out.println("Вы хотите произвести другие операции : да или нет ?");
            String s=l.next();
            if(s.equals("да")) {
                m=false;
            }
                if(s.equals("нет")) {
                    System.out.println("Спасибо, что воспользовались услугами нашего банкомата.");
                m=true;

                }
            }
        }}





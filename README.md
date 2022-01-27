package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        System.out.println("Давай ссумировать числа.\nЧтобы закончить введи end.");
        Scanner console = new Scanner(System.in); //Вызываем класс Scanner
        boolean end = false;
        boolean end2 = false;
        int i1 = 0;
        String str1 = "end";
        System.out.println("начало цикла");

        while (!end) {
                System.out.println("Проверяю ввел ли ты число");
            if (console.hasNextInt())
            {
                System.out.println("Ты ввел число, суммирую");
                int i2 = console.nextInt();
                i1 = i1 + i2;
                System.out.println("Последнее введенное число: " + i2);
                System.out.println("Сумма: " + i1);
            }
            System.out.println("Ты ввел не число, проверяю ввел ли ты end");
            if (console.nextLine().equalsIgnoreCase(str1))
            {
                System.out.println("Ты ввел end, заканичиваю программу!");
                end = true;
            }
            System.out.println("Ты ввел не число и не end, вводи только эти 2 значения");
        }

        System.out.println("Конец программы."); //Конец программы
    }
}

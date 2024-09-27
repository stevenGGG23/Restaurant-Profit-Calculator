* Filename: festival.cpp
* Description: This program takes a input of how much of each item at this shop is sold and calqulates a recipt 
at the end in a specific fonted way 
*/ 

#include <iostream> 
#include <iomanip> 

int main() {

    // This is the price of each item on the menue 
    const float price_mushrooms = 0.80f;
    const float price_lembas = 3.00f;
    const float price_cram_bread = 2.00f;
    const float price_salted_pork = 2.25f;
    const float price_rabbit_stew = 3.25f;
    const float price_honey_cake = 2.00f;
    const float price_well_water = 1.25f;
   
    // the cut percentage calc that we will use later on in the recipt 
    const float cut_percentage = 0.0675f;

    //making sure we make all these into integer format so that the user can input a number 
    int mushrooms, lembas, cram_bread, salted_pork, rabbit_stew, honey_cake, well_water;

    //prompting user to input quantity 
    std::cout << "How many Mushrooms were sold?: ";
    std::cin >> mushrooms;
    std::cout << "How many Lembas were sold?: ";
    std::cin >> lembas;
    std::cout << "How many Cram Bread were sold?: ";
    std::cin >> cram_bread;
    std::cout << "How many Salted Pork were sold?: ";
    std::cin >> salted_pork;
    std::cout << "How many Rabbit Stew were sold?: ";
    std::cin >> rabbit_stew;
    std::cout << "How many Honey Cake were sold?: ";
    std::cin >> honey_cake;
    std::cout << "How many Well Water were sold?: ";
    std::cin >> well_water;

    // calc for the total price 
    float total_mushrooms = mushrooms * price_mushrooms;
    float total_lembas = lembas * price_lembas;
    float total_cram_bread = cram_bread * price_cram_bread;
    float total_salted_pork = salted_pork * price_salted_pork;
    float total_rabbit_stew = rabbit_stew * price_rabbit_stew;
    float total_honey_cake = honey_cake * price_honey_cake;
    float total_well_water = well_water * price_well_water;

    //calc for total revenue, the cut ammount, and pre cut profit 
    float total_revenue = total_mushrooms + total_lembas + total_cram_bread + total_salted_pork + total_rabbit_stew + total_honey_cake + total_well_water;

    float cut_amount = total_revenue * cut_percentage;
    float total_after_cut = total_revenue - cut_amount;
    
    float pre_cut_profit = total_revenue / 2;

    //print of the final result 
    std::cout << "------------------------------------------" << std::endl;
    std::cout << "----Tomburan Longriver's Savory Dishes----" << std::endl;
    std::cout << "------------------------------------------" << std::endl;
    std::cout << " QTY   DISH NAME UNIT PRICE TOTAL RECEIVED" << std::endl;
    std::cout << "---- ----------- ---------- --------------" << std::endl;
    std::cout << std::setw(4) << mushrooms << " Mushrooms      $" << std::setw(5) << std::fixed << std::setprecision(2) << price_mushrooms << "       $  " << std::setw(6) << total_mushrooms << std::endl;
    std::cout << std::setw(4) << lembas << " Lembas         $" << std::setw(5) << std::fixed << std::setprecision(2) << price_lembas << "       $  " << std::setw(6) << total_lembas << std::endl;
    std::cout << std::setw(4) << cram_bread << " Cram Bread     $" << std::setw(5) << std::fixed << std::setprecision(2) << price_cram_bread << "       $  " << std::setw(6) << total_cram_bread << std::endl;
    std::cout << std::setw(4) << salted_pork << " Salted Pork    $" << std::setw(5) << std::fixed << std::setprecision(2) << price_salted_pork << "       $  " << std::setw(6) << total_salted_pork << std::endl;
    std::cout << std::setw(4) << rabbit_stew << " Rabbit Stew    $" << std::setw(5) << std::fixed << std::setprecision(2) << price_rabbit_stew << "       $  " << std::setw(6) << total_rabbit_stew << std::endl;
    std::cout << std::setw(4) << honey_cake << " Honey Cake     $" << std::setw(5) << std::fixed << std::setprecision(2) << price_honey_cake << "       $  " << std::setw(6) << total_honey_cake << std::endl;
    std::cout << std::setw(4) << well_water << " Well Water     $" << std::setw(5) << std::fixed << std::setprecision(2) << price_well_water << "       $  " << std::setw(6) << total_well_water << std::endl;
    std::cout << "                            --------------\n" << std::endl;
    std::cout << "              TOTAL RECEIVED     $ " << std::setw(6) << total_revenue << std::endl;
    std::cout << "                   CUT TAKEN     $ " << std::setw(6) << cut_amount << std::endl;
    std::cout << "             TOTAL MINUS CUT     $ " << std::setw(6) << total_after_cut << std::endl; \

    std::cout << "\n"<<  std::endl;
    
    std::cout << "Total Profit pre-cut: $" << std::fixed << std::setprecision(2) << pre_cut_profit << std::endl;

    return 0;

}



# Project-C-
#include <iostream>
#include<conio.h>
using namespace std;
main()
{
    int purchase_pizza=0,purchase_burger=0,purchase_samosha=0,purchase_momos=0,
    purchase_icecream=0;

    int sell_pizza=0,sell_burger=0,sell_samosha=0,sell_momos=0,sell_icecream=0;

    int pizza=0,burger=0,samosha=0,momos=0,icecream=0;

    int choice,quantity;

    cout << "Stock add In Shop  : "<<endl;
    cout << "Number Of Pizza   : ";
    cin >> purchase_pizza;
    cout << "Number Of Burger  : ";
    cin >> purchase_burger;
    cout << "Number Of Samosha : ";
    cin >> purchase_samosha;
    cout << "Number Of Momos   : ";
    cin >> purchase_momos;
    cout << "Number Of IceCream: ";
    cin >> purchase_icecream;
    purchase:
    system("cls");
    cout << "This is all iteam Available in My Shop: "<<endl;
    cout<<"\nPress 1 to order Pizza"<<endl;
    cout<<"\nPress 2 to order Burger"<<endl;
    cout<<"\nPress 3 to order Samosha"<<endl;
    cout<<"\nPress 4 to order Momos"<<endl;
    cout<<"\nPress 5 to order IceCream"<<endl;
    cout<<"\nPress 6 to Chek Details "<<endl;
    cout << "\nPress 7 to Exit"<<endl;
    cout << "\nEnter Your Choice: ";
    cin >> choice;
    switch (choice)
    {
    case 1:
    cout << "Enter Quantity For Pizza Purchasing : ";
    cin >> quantity;
    if (purchase_pizza - sell_pizza >= quantity)
    {
        sell_pizza += quantity;
        pizza += quantity * 199;
        cout<<"Your Order is Processing...."<<endl;
        cout<<"\t"<<quantity <<" Pizza Order Succesful... Thank You !!! ";
    }
    else
    cout << "Sorry" << purchase_pizza - sell_pizza << "Pizza Remaining in Resturent";
        break;
    case 2:
    cout << "Enter Burger Quantity : ";
    cin >> quantity;
    if (purchase_burger - sell_burger >= quantity)
    {
        sell_burger += quantity;
        burger += quantity * 149;
        cout<<"Your Order is Processing...."<<endl;
        cout<<"\t"<<quantity <<" Burger Order Succesful.. Thank You!!";
    }
    else
    cout << "Sorry" << purchase_burger - sell_burger << "burger Remaining in Resturent";
        break;
    case 3:
         cout << "Enter Samosha Quantity : ";
    cin >> quantity;
    if (purchase_samosha - sell_samosha >= quantity)
    {
        sell_samosha += quantity;
        samosha += quantity * 10;
        cout<<"Your Order is Processing...."<<endl;
        cout<<"\t"<<quantity <<" Samosha Order Succesful... Thank You !!! ";
    }
    else
    cout << "Sorry" << purchase_samosha - sell_samosha << "Samosha Remaining in Resturent";
        break;
    case 4:
        cout << "Enter momos Quantity : ";
    cin >> quantity;
    if (purchase_momos - sell_momos >= quantity)
    {
        sell_momos += quantity;
        momos += quantity * 30;
        cout<<"Your Order is Processing...."<<endl;
        cout<<"\t"<<quantity <<" Momos Order Succesful... Thank You !!! ";
    }
    else
    cout << "Sorry" << purchase_momos - sell_momos << "Momos Remaining in Resturent";
        break;
    case 5:
        cout << "Enter icecream Quantity : ";
    cin >> quantity;
    if (purchase_icecream - sell_icecream >= quantity)
    {
        sell_icecream += quantity;
        icecream += quantity * 49;
        cout<<"Your Order is Processing...."<<endl;
        cout<<"\t"<<quantity <<" IceCream Order Succesful... Thank You !!! ";
    }
    else
    cout << "Sorry" << purchase_icecream - sell_icecream << "IceCream Remaining in Resturent";
        break;
    case 6:
        system("cls");
        cout << "\tPizza Details"<<endl;
        cout<< "\nPurchase Pizza Quantity : " << purchase_pizza<<endl;
        cout<< "\nsales Pizza Quantity : " << sell_pizza<<endl;
        cout<< "\nRemaining Pizza Quantity : " << purchase_pizza - sell_pizza<<endl;
        cout<< "\nTotal Pizza Price in a Day : " << pizza<<endl;

        cout << "\tBurger Details"<<endl;
        cout<< "\nPurchase Burger Quantity : " << purchase_burger<<endl;
        cout<< "\nsales Burger Quantity : " << sell_burger<<endl;
        cout<< "\nRemaining Burger Quantity : " << purchase_burger - sell_burger<<endl;
        cout<< "\nTotal Burger Price in a Day : " << burger<<endl;

        cout << "\tSamosha Details"<<endl;
        cout<< "\nPurchase Samosha Quantity : " << purchase_samosha<<endl;
        cout<< "\nSales Samosha Quantity : " << sell_samosha<<endl;
        cout<< "\nRemaining Samosha Quantity : " << purchase_samosha - sell_samosha<<endl;
        cout<< "\nTotal Samosha Price in a Day : " << samosha<<endl;

        cout << "\tMomos Details"<<endl;
        cout<< "\nPurchase Momos Quantity : " << purchase_momos<<endl;
        cout<< "\nSales Momos Quantity : " << sell_momos<<endl;
        cout<< "vRemaining Momos Quantity : " << purchase_momos - sell_momos<<endl;
        cout<< "\nTotal Momos Price in a Day : " << momos<<endl;

        cout << "\tIceCream Details"<<endl;
        cout<< "\nPurchase IceCream Quantity : " << purchase_icecream<<endl;
        cout<< "\nSales IceCream Quantity : " << sell_icecream<<endl;
        cout<< "\nRemaining IceCream Quantity : " << purchase_icecream - sell_icecream<<endl;
        cout<< "\nTotal IceCream Price in a Day : " << icecream<<endl;
        cout <<"\nTotal Day Price : " <<pizza+burger+samosha+momos+icecream<<endl;
        break;
    case 7:
        exit(0);
        break;
    default:
        cout << "Invalid value .. Please Try Again : ";
        break;
    }
    getch();
    goto purchase;
}

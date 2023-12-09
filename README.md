# Hotel-Managmet
#include <iostream>
using namespace std;
int main()
{
    int quant;
    int choice;
    // quanties
    int qrooms = 0, qpasta = 0, qburger = 0, qnoodle = 0, qshake = 0, qchicken = 0;
    // sold
    int srooms = 0, spasta = 0, sburger = 0, snoodle = 0, sshake = 0, schicken = 0;
    // total price
    int Total_rooms = 0, Total_pasta = 0, Total_burger = 0, Total_noodle = 0, Total_shake = 0, Total_chicken = 0;

    cout << "\n\t Quantities of items we have in hotel";
    cout << "\n\t Number of Rooms we have in hotel:";
    cin >> qrooms;
    cout << "\n Quantities of Pasta:";
     cin >> qpasta;
    cout << "\n Quantities of Burger:"; 
    cin >> qburger;
    cout << "\n Quantities of Noodle:" ;
    cin >> qnoodle;
    cout << "\n Quantities of Shake:" ;
    cin >> qshake;
    cout << "\n Quantities of Chicken-roll:";
     cin >> qchicken;

    // menu

    m:
    cout << "\n\t\t\t Please select from the menu item";
    cout << "\n\n 1) Rooms";
    cout << "\n 2) Pasta";
    cout << "\n 3) Burger";
    cout << "\n 4) Noodle";
    cout << "\n 5) shake";
    cout << "\n 6) Chicken-roll";
    cout << "\n 7) Inoformation regarding sales and collection";
    cout << "\n 8) Exit";

    cout << "\n\n Please enter your choice:";
    cin >> choice;

    switch (choice)
    {
    case 1:
        cout << "\n\n Enter the numbers of rooms you want:";
        cin >> quant;
        if (qrooms - srooms >= quant)
        {
            srooms += quant;
            Total_rooms += quant * 1200;
            cout << "\n\n\t\t" << quant << "\t room/rooms have been alloated to you";
        }
        else
        {
            cout << "\n\t Only" << qrooms - srooms << "\t Rooms remaining in hotel";
        }
        break;

    case 2:
        cout << "\n\n Enter the Patsa Quantiy:";
        cin >> quant;
        if (qpasta - spasta >= quant)
        {
            spasta += quant;
            Total_pasta += quant * 250;
            cout << "\n\n\t\t" << quant << "\t Pasta is the order";
        }
        else
        {
            cout << "\n\t Only" << qpasta - spasta << "\t Stock of pasta remaining in hotel";
        }
        break;

    case 3:
        cout << "\n\n Enter Burger Quantity:";
        cin >> quant;
        if (qburger - sburger >= quant)
        {
            sburger += quant;
            Total_burger += quant * 120;
            cout << "\n\n\t\t" << quant << "\t Burger is order";
        }
        else
        {
            cout << "\n\t Only" << qburger - sburger << "\t Quantity of Burger remaining in hotel";
        }
        break;

    case 4:
        cout << "\n\n Enter Noodle Quantity:";
        cin >> quant;
        if (qnoodle - snoodle >= quant)
        {
            snoodle += quant;
            Total_noodle += quant * 140;
            cout << "\n\n\t\t" << quant << "\t Noodle is order";
        }
        else
        {
            cout << "\n\t Only" << qnoodle - snoodle << "\t Quantity of Noodle remaining in hotel";
        }
        break;

    case 5:
        cout << "\n\n Enter shake Quantity:";
        cin >> quant;
        if (qshake - sshake >= quant)
        {
            sshake += quant;
            Total_shake += quant * 120;
            cout << "\n\n\t\t" << quant << "\t shake is order";
        }
        else
        {
            cout << "\n\t Only" << qshake - sshake << "\t Quantity of Shake remaining in hotel";
        }
        break;

    case 6:
        cout << "\n\n Enter Chicken-Roll Quantity:";
        cin >> quant;
        if (qchicken - schicken >= quant)
        {
            schicken += quant;
            Total_chicken += quant * 150;
            cout << "\n\n\t\t" << quant << "\t Chicken-Roll is order";
        }
        else
        {
            cout << "\n\t Only" << qchicken - schicken << "\t Quantity of Chicken-Roll remaining in hotel";
        }
        break;

    case 7:
        cout << "\n\t\tDetails of sales and collection";
        cout << "\n\n Number of rooms we had:" << qrooms;
        cout << "\n\n Number of rooms we gave for rent:" << srooms;
        cout << "\n\n Remaining Rooms:" << qrooms - srooms;
        cout << "\n\n Total rooms collection for the day:" << Total_rooms;

        cout << "\n\n Quantity of pasta we had:" << qpasta;
        cout << "\n\n Quanntity of pasta we sold:" << spasta;
        cout << "\n\n Remaining Pasta:" << qpasta - spasta;
        cout << "\n\n Total sold Pasta for the day:" << Total_pasta;

        cout << "\n\n Quantity of Burger we had:" << qburger;
        cout << "\n\n Quanntity of Burger we sold:" << sburger;
        cout << "\n\n Remaining Burger:" << qburger - sburger;
        cout << "\n\n Total sold Burger for the day:" << Total_burger;

        cout << "\n\n Quantity of Noodle we had:" << qnoodle;
        cout << "\n\n Quanntity of Noodle we sold:" << snoodle;
        cout << "\n\n Remaining Noodle:" << qnoodle - snoodle;
        cout << "\n\n Total sold Noodle for the day:" << Total_noodle;

        cout << "\n\n Quantity of Shake we had:" << qshake;
        cout << "\n\n Quanntity of Shake we spld:" << sshake;
        cout << "\n\n Remaining Shake:" << qshake - sshake;
        cout << "\n\n Total sold Shake for the day:" << Total_shake;

        cout << "\n\n Quantity of Chicken-roll we had:" << qchicken;
        cout << "\n\n Quanntity of Chicken-roll  we sold:" << schicken;
        cout << "\n\n Remaining Chicken-roll :" << qchicken - schicken;
        cout << "\n\n Total sold Chicken-roll  for the day:" << Total_chicken;

        cout<<"\n\n\n Total collection for the day:"<<Total_rooms+Total_burger+Total_chicken+Total_noodle+Total_pasta+Total_shake;
        break;

        case 8:
        exit(0);
         
         default:
         cout<<"\n Please select the number maintain above!";
    }
 goto m;
 return 0;
}

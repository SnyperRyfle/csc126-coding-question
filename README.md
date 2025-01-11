# csc126-coding-question
#include <iostream>
using namespace std;

int main() {
    int destinationCode, numAdults, numChild;
    double totalAmount = 0.0, taxAmount, totalPayment;
    const double taxUser = 0.06;
    const double adulttoBali = 105.00;
    const double childtoBali = 50.00;
    const double adulttoPerth = 250.00;
    const double childtoPerth = 78.00;
    const double adulttoSingapore = 59.00;
    const double childtoSingapore = 29.00;
        const double adulttoBeijing = 199.00;
    const double childtoBeijing = 109.00;

    cout << "DESTINATION ======= DESTINATION CODE===== ADULT=====CHILD(<9 YEARS)" << endl;
    cout << "=KL TO BALI==========1===================RM105.00======50.00" << endl;
    cout << "KL TO PERTH==========2===================RM250.00======78.00" << endl;
    cout << "=KUCHING TO SINGAPORE==========3===================RM59.00======29.00" << endl;
    cout << "KUCHING TO BEIJING==========4===================RM199.00======109.00" << endl;

    cout << "Please enter the destination code: ";
    cin >> destinationCode;

    cout << "Enter the number of passengers below." << endl;
    cout << "Number of adults: ";
    cin >> numAdults;
    cout << "Number of children (under 9 years old): ";
    cin >> numChild;

    if (destinationCode == 1) {
        totalAmount = (numAdults * adulttoBali) + (numChild * childtoBali);
    } else if (destinationCode == 2) {
        totalAmount = (numAdults * adulttoPerth) + (numChild * childtoPerth);
    } else if (destinationCode == 3) {
        totalAmount = (numAdults * adulttoSingapore) + (numChild * childtoSingapore);
    } else if (destinationCode == 4) {
        totalAmount = (numAdults * adulttoBeijing) + (numChild * childtoBeijing);
    } else {
        cout << "Invalid destination code." << endl;
        
    }

    if (totalAmount > 0) {
        taxAmount = totalAmount * taxUser;
        totalPayment = totalAmount + taxAmount;

        cout << "Your total before the tax is: RM" << totalAmount << endl;
        cout << "Your real payment is: RM" << totalPayment << endl;
    }

    return 0;
}

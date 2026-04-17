#include<iostream>
using namespace std;

string seats[10]; // empty = free, otherwise stores name

void showMenu() {
    cout<<"\n===== Seat Reservation System =====\n";
    cout<<"1. Reserve Seat\n";
    cout<<"2. View All Seats\n";
    cout<<"3. Cancel Reservation\n";
    cout<<"4. Seat Summary\n";
    cout<<"5. View Seat Details\n";
    cout<<"6. Exit\n";
    cout<<"Enter choice: ";
}

int main() {
    int choice, seat;

    while(true) {
        showMenu();
        cin>>choice;

        switch(choice) {

            case 1: {
                cout<<"Enter seat number (1-10): ";
                cin>>seat;

                if(seat < 1 || seat > 10) {
                    cout<<"Invalid seat number\n";
                    break;
                }

                if(seats[seat-1] == "") {
                    cout<<"Enter your name: ";
                    cin>>seats[seat-1];
                    cout<<"Seat Reserved Successfully\n";
                } else {
                    cout<<"Seat already booked by "<<seats[seat-1]<<endl;
                }
                break;
            }

            case 2: {
                cout<<"\n--- Seat Status ---\n";
                for(int i=0;i<10;i++) {
                    cout<<"Seat "<<i+1<<": ";
                    if(seats[i] == "")
                        cout<<"Free\n";
                    else
                        cout<<"Booked ("<<seats[i]<<")\n";
                }
                break;
            }

            case 3: {
                cout<<"Enter seat number to cancel: ";
                cin>>seat;

                if(seat < 1 || seat > 10) {
                    cout<<"Invalid seat number\n";
                    break;
                }

                if(seats[seat-1] == "") {
                    cout<<"Seat is already free\n";
                } else {
                    seats[seat-1] = "";
                    cout<<"Reservation Cancelled\n";
                }
                break;
            }

            case 4: {
                int booked = 0;
                for(int i=0;i<10;i++) {
                    if(seats[i] != "") booked++;
                }
                cout<<"Booked Seats: "<<booked<<endl;
                cout<<"Free Seats: "<<10 - booked<<endl;
                break;
            }

            case 5: {
                cout<<"Enter seat number: ";
                cin>>seat;

                if(seat < 1 || seat > 10) {
                    cout<<"Invalid seat number\n";
                    break;
                }

                if(seats[seat-1] == "")
                    cout<<"Seat is Free\n";
                else
                    cout<<"Booked by: "<<seats[seat-1]<<endl;

                break;
            }

            case 6:
                cout<<"Exiting program...\n";
                return 0;

            default:
                cout<<"Invalid choice\n";
        }
    }

    return 0;
}

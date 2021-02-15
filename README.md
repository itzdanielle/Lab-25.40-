# Lab-25.40-
#include <iostream>
#include <string>
using namespace std;

int main() {
 double averageRain, highestRain, lowestRain;
 double monthlyRainfall[12];
 double totalRains = 0;
 int highMonth, lowMonth;

 string Months [12] = { "Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"};
 
 cout << "Enter the rainfall for the Months" << endl;
 for (int i = 0; i < 12; i ++) {
   cout << Months[i] << ": ";
   cin >> monthlyRainfall[i];
   totalRains = totalRains + monthlyRainfall[i];
 }
 averageRain = totalRains/12;

 highestRain = monthlyRainfall[0];
 for (int i = 1; i < 12; i ++) {
   if (monthlyRainfall[i] > highestRain) {
     highestRain = monthlyRainfall[i];
      highMonth = i;
   }
   else {
     highMonth = 0;
   }
 }
 lowestRain = monthlyRainfall[0];
 for (int i = 1; i < 12; i++) {
   if (monthlyRainfall[i] < lowestRain) {
     lowestRain = monthlyRainfall[i];
     lowMonth = i;
   }
   else {
     lowMonth = 0;
   }
 }

 cout << "The total rain for the year was " << totalRains << endl;
 cout << "The average rainfall for the year was " << averageRain << endl;
 cout << "The month with the most rain was " << Months[highMonth] << endl;
 cout << "The month with the least rain was " << Months [lowMonth] << endl;
}

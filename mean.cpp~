// Names: Nicole Hipolito, Carlos Huizar, Mavey Ma, Mario Martinez.
// Created: Friday, Oct. 30, 2015
// Steel / Graphite
/* Answer to the question: Since the force is too great for the bridge, the bridge will break if we have a safety factor of 3 standard devition. 
*/ 
#include <iostream>
#include <fstream>
#include <string>
#include <cstdlib>
#include <iomanip>
#include <cmath>
using namespace std;

void printAry(int ary[], int n);
double mean(int ary[], int n);
int maxValue(int ary[], int n);
int min(int a[], int n);
double variance(int ary[], int numberElement);
double standardDeviation(int ary[], int numberElement);

int main()
{
    ifstream fin;
    ifstream finB;
    ofstream fout;
    int count = 0;
    int count2 = 0;
    int nums, num2;
    int ary[20];
    int ary2[20];
    fin.open("data1.txt");
    finB.open("data2.txt");
    fout.open("results.txt");
    if(fin.fail() || finB.fail() || fout.fail())
    {
        cout << "Error in file\n";
    }
    while(fin >> nums)
    {
        ary[count] = nums; 
        count++;
    }
    while(finB >> num2)
    {
        ary2[count2] = num2;
        count2++;
    }
    
    fout.setf(ios::fixed);
    fout.setf(ios::showpoint);
    fout.precision(2);
    
    fout << "Nicole Hipolito, Carlos Huizar, Mavey Ma, Mario Martinez." << endl;
    fout << "Mean for data1: " << mean(ary, count) << endl;
    fout << "Mean for data2: " << mean(ary2, count2) << endl;
    fout << "Max value for data1: " << maxValue(ary, count) << endl;
    fout << "Max value for data2: " << maxValue(ary2, count2) << endl;
    fout << "Min value for data1: " << min(ary, count) << endl;
    fout << "Min value for data2: " << min(ary2, count2) << endl;
    fout << "Variance for data1: " << variance(ary, count) << endl;
    fout << "Variance for data2: " << variance(ary2, count2) << endl;
    fout << "Standard Deviation for data1: " << standardDeviation(ary, count) << endl;
    fout << "Standard Deviation for data2: " << standardDeviation(ary2, count2) << endl;
    
    fin.close();
    finB.close();
    fout.close();
    return 0;
}
//*************************************************
void printAry(int ary[], int n)
{
    for(int i = 0; i < n; i++)
    {
        cout << setw(7) << ary[i];
    }
    cout << endl;
}
//*************************************************
double mean(int ary[], int n)
{
    double total = 0;
    double average;
    for (int ix = 0; ix < n; ix++)
    {
        total += ary[ix];
    }//END FOR LOOP
    average = total / n;
    return average;
}//END MEAN 
//*************************************************
int maxValue(int ary[], int n)
{
    int max = ary[0];
    for(int i = 0; i < n; i++)
    {
        if(ary[i] > max)
        {
            max = ary[i];
        }
    }
    return max;
}
//*************************************************
double variance(int ary[], int numberElement)
{
    double mean1 = mean(ary, numberElement);
    double top = 0, total, x;
    for(int ix = 0; ix < numberElement; ix++)
    {
        x = pow((ary[ix] - mean1), 2);
        top += x;

    }
    total = top / numberElement;
    
    return total;
}
//*************************************************
double standardDeviation(int ary[], int numberElement)
{
    double variance1 = variance(ary , numberElement);
    double mean1 = mean(ary , numberElement);
    double deviation = mean1 - sqrt(variance1)*3;
    return deviation;
}
//*************************************************
int min(int a[], int n)
{
    int min = a[0];
    for(int i = 0; i < n; i++)
    {
        if(min > a[i])
        {
            min = a[i];
        }
    
    }   
    return min;
}
//*************************************************

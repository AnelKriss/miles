# miles
#include <fstream>
#include <string>
#include<iostream>
using namespace std;
class FileCreator
{
private:
ofstream MyFile;
public:
FileCreator(string);
void WriteFile(string, double, double, int, double);
void WriteHeader();
void CloseFile();
};

# 2ndpg)
#include <iostream> 
#include <string> 
using namespace std;
FileCreator::FileCreator(string file)
{
this->MyFile.open(file);
}
void FileCreator::WriteHeader()
{
MyFile << "City Name, MilesToDrive, GasPrice, MPG, TravelExpense\n";
}
void FileCreator::WriteFile(string cityName, double milesToDrive, double gasPrice, int mpg, double te)
{
MyFile << cityName << ", " << milesToDrive << ", " << gasPrice << ", " << mpg << ", " << te << endl;
}
void FileCreator::CloseFile()
{
MyFile.close();
}

# Pg3)
***
#include "FileCreator.h";
#include <string>
#include <iostream>
using namespace std;
//number of para is how many var youll use
int main()
{
string fileName;
string cityName;
double miles;
double gasPrice;
int milesPerGallon;
double travelExpense;
cout << "Enter the name of this file: ";
cin >> fileName;
FileCreator luis(fileName);
luis.WriteHeader(); ////the num > 5 representes 5 diffewrent cities 
for (int x = 0; x < 2; x++)
{
cout << "Enter the city name: ";
cin >> cityName;
cout << "Enter the miles to drive: ";
cin >> miles;
cout << "Enter the gas price: ";
cin >> gasPrice;
cout << "Enter the mpg: ";
cin >> milesPerGallon;
travelExpense = ((miles / milesPerGallon) * gasPrice);
luis.WriteFile(cityName, miles, gasPrice, milesPerGallon, travelExpense);
}
luis.CloseFile();
}


# oppp
#pragma once
#include <fstream> 
#include <string> 
#include<iostream> 
using namespace std;
class Card
{
class FileCreator
{
private:
ofstream MyFile;
public:
FileCreator(string);
void WriteFile(string, double, double, int, double);
void WriteHeader();
void CloseFile();
}

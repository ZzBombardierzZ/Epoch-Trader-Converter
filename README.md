# Epoch Trader Converter -- Version 1.0
A simple program built for DayZ Epoch to easily convert trader files into a CSV file for easier editing. You can also import a CSV file to rebuild trader files. If you want to switch your economy from gold/gem to coins or vice versa, you can simple build a CSV file with your current files and then rebuild the trader files with your desired economy system.

## Features
* Convert trader files to CSV files
* Import CSV files to rebuild trader files
* Switch between gold/gem and coins
* Super Fast!

Youtube Example Video:
https://www.youtube.com/watch?v=q9t-Ug1_ZIE

## Notes
* This DOES NOT deal the with the trader menu handling. If you add Category numbers to the CSV file, you will need to manually assign them to your desired traders. The default location for this is @DayZ_Epoch\addons\dayz_code\system\mission\server_traders\chernarus11.sqf or replace chernarus11.sqf with whichever map you are using. These are not instructions for how to customize this file.
* It is suggested to backup your trader files before using this program in case of some sort of error. Although, it doesn't change your files directly unless you tell it to.
* Running Trader to CSV will not take any comments from the trader files, they are stripped as it reads them.
* Trader to CSV only works with "worth" aka coins and silver/gold item classnames for the buy/sell prices.
* Be sure to select the entire CfgServerTrader (or CfgServerTraderZSC) folder when using Trader to CSV.
* Once you have the CSV file, consider the following:
    * You can use the CSV file to rebuild trader files with your desired economy system.
    * Do not add any more columns to the CSV file.
    * Do not change the order of the columns.
    * Do not change the column names.
    * You CAN and are encouraged to add/remove/change the rows in the CSV file, but not the first row (the header row).
* Notes for when converting back into trader files:
    * You can use the CSV file to rebuild trader files with your desired economy system as previously stated.
    * The returned trader files will be named CfgServerTraderZSC if you are using coins or CfgServerTrader if you are using gold/gem.
    * If you select classic economy, the program will use a lowest common denominator of silver and gold for the buy/sell prices.
        * This means 12000 in the CSV file would be converted to 12x ItemGoldBar10oz
        * Another example: 1050 would be converted to 105x ItemSilverBar10oz
        * Consider the above carefully when choosing prices if you plan to use classic silver/gold economy.
* As stated before, do not use something like "ItemRuby" for the buy price, it will not work. Epoch should automatically convert 10, "Itembriefcase100oz" to 1 ruby in the traders if you have a ruby set to being worth to 10 briefcases.
* When viewing/editing the CSV file and if you plan to use classic economy, take a look at this [Currency Value File](https://github.com/ZzBombardierzZ/Epoch-Trader-Converter/blob/main/DayZ_Epoch_Silver_and_Gold_Values.txt)

## Legal
* I built this software myself and I am not affiliated with Epoch.
* I am not responsible for any damage or loss of data that may occur from using this software.
* Though this software is free to all to use, I have decided to not share the source code this time around.
* It is not techincally licensed but I do ask that you give me credit if you use this software.

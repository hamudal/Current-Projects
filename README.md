# Current-Projects

Data Analyses, Data Engineering , Data science

All For One Scraper

Hall of Pole Web Scraping Project
My sister is a passionate pole dancer who teaches and performs as her passion. She wanted to provide a platform (https://www.hallofpole.com) for all pole studios in Germany to be easily found and connected to. To help her with this, I used data scraping on the website https://www.eversports.de/ to gather information about pole studios.

Project Overview
The project consists of three versions: V1, V2, and V3. V1 was my first attempt to implement a solution using BeautifulSoup4 and consists of five Jupyter files, one for each category: pole studio overview site, the corresponding workshop list, the overview of the workshop itself, the prices of different kinds of memberships of the pole studios, and finally, an exploration py file that loads all CSVs generated by the scripts before.

V2 is the most stable version, building on V1. I focused on readability and reusability of the code itself. We have six scripts here, including the main function that imports all function scripts such as the PoleStudio_Overview_Func, Workshops_List_Func, Workshop_Overview_Func, and a function that calls all three scripts, putting them into a function that combines them all into one function, which is called CallPy.

The main functions will import everything from call by the 1_main_Func:

# Example URLs: https://www.eversports.de/sw/poda-studio, https://www.eversports.de/sw/poda-studio

# Get user input for a list of URLs

user_input = input("Enter URLs separated by commas: ")

# Split the input string into a list of URLs

url_list = [url.strip() for url in user_input.split(',')]

# Call the super_function with the list of URLs

workshops_df, workshops_overview_df, polestudios_overview_df = super_function(url_list)

# Display the DataFrames

print(workshops_df)
print(workshops_overview_df)
print(polestudios_overview_df)

V3 combines all scripts into one to see which case is more useful or easier to debug. However, V2 is the most reliable and readable script, and I would advise you to try V1 and V2 first.

Usage
Clone the repository to your local machine.
Install the required dependencies using the requirements.txt file.
Run the 1_MainFunc script.
Input the URL of the pole studio in the format "https://www.eversports.de/sw/poda-studio".
The script will scrape all available workshops of the pole studio and will run through the workshop overview and pole studio overview.
The script will output three CSV files with the corresponding dataframes.
Dependencies
All required dependencies are included in the requirements.txt file.

Conclusion
This project aims to provide a platform for all pole studios in Germany to be easily found and connected to. Through web scraping, we were able to gather valuable information that could help pole dancers find the right studio for their needs. The project has three versions, with V2 being the most reliable and readable script.

The Pole Studio Scraper script is intended for educational and research purposes only. The script should not be used for commercial purposes without the consent of the studio owners.

PS: This was my first self managed project and was much fun. I would lie, if I said, it was easy, but it was worth it. Learning by doing and trial & error taught me much more, than just "watching" or learning.

To create the One For All Scraper script took around 130h of learning, coding and debugging.

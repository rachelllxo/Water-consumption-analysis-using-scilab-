# Water-consumption-analysis-using-scilab-
A simple water consumption analysis and comparison of weekly data in liters.  
WATER TANK CONSUMPTION ANALYSIS USING SCILAB 

INTRODUCTION: 
Water consumption is a key aspect of daily life, and tracking it can help in better managing water resources. This project focuses on creating a Water Consumption Analysis that allows users to monitor and compare water usage over multiple weeks. The tracker enables users to view the water consumption for a specific week or compare the water consumption data between two weeks, helping them to make informed decisions about their water usage habits.
This project was implemented using Scilab, an open-source software for numerical computations, to visualize the consumption data in an easy-to-understand manner. The main features of this project include viewing weekly data and comparing water usage over two weeks using simple line graphs.
OBJECTIVES: 
The primary objectives of this project are:
To create a user-friendly water consumption tracker.
To visualize daily water consumption data over multiple weeks.
To provide options for comparing the water consumption between two different weeks.
To assist users in tracking and analyzing their water usage patterns.



 FEATURES:
The Water Consumption Tracker offers the following features:
View Specific Week Data: Users can choose a specific week (from week 1 to week 4) and view the daily water consumption for that week.


Compare Water Consumption Between Two Weeks: Users can compare the water consumption between any two weeks by displaying their respective consumption data on a line graph.


Visual Representation: The consumption data is displayed on a line graph, making it easy to identify trends in water usage.                                                   

MAIN COMPONENTS: 
           The system is designed with two main components:
Data Storage: Hardcoded data representing the water consumption for 4 weeks.
User Interaction: A menu-driven interface that allows users to select options for viewing data or comparing two weeks.

PROGRAM :
week1 = [500, 470, 520, 450, 480, 510, 495];
week2 = [460, 475, 490, 505, 520, 495, 510];
week3 = [480, 450, 470, 460, 495, 500, 485];
week4 = [490, 460, 505, 480, 510, 475, 500];
consumption_data = [week1; week2; week3; week4];
function show_week_data(week_num)
    if week_num == 1 then
        disp("Week 1 Data: " + string(consumption_data(1, :)));
    elseif week_num == 2 then
        disp("Week 2 Data: " + string(consumption_data(2, :)));
    elseif week_num == 3 then
        disp("Week 3 Data: " + string(consumption_data(3, :)));
    elseif week_num == 4 then
        disp("Week 4 Data: " + string(consumption_data(4, :)));
    else
        disp("Invalid week number. Please enter a number between 1 and 4.");
    end
endfunction
function compare_weeks(week1_num, week2_num)
    if week1_num == 1 then
        data1 = consumption_data(1, :);
    elseif week1_num == 2 then
        data1 = consumption_data(2, :);
    elseif week1_num == 3 then
        data1 = consumption_data(3, :);
    elseif week1_num == 4 then
        data1 = consumption_data(4, :);
    else
        disp("Invalid first week number.");
        return;
    end

    if week2_num == 1 then
        data2 = consumption_data(1, :);
    elseif week2_num == 2 then
        data2 = consumption_data(2, :);
    elseif week2_num == 3 then
        data2 = consumption_data(3, :);
    elseif week2_num == 4 then
        data2 = consumption_data(4, :);
    else
        disp("Invalid second week number.");
        return;
    end
    clf;
    plot(data1, '-r', 'LineWidth', 2); 
    hold on; 
    plot(data2, '-b', 'LineWidth', 2);
    hold off;

    legend("Week " + string(week1_num), "Week " + string(week2_num));
    title("Water Consumption Comparison (Week " + string(week1_num) + " vs Week " + string(week2_num) + ")");
    xlabel("Days (1-7)");
    ylabel("Liters Consumed");
endfunction

disp("Welcome to the Water Consumption Tracker!");
disp("=========================================");
disp("1. View Data of a Specific Week");
disp("2. Compare Two Weeks'' Consumption");
choice = input("Enter your choice (1 or 2): ");

if choice == 1 then
    week_choice = input("Enter the week number (1-4) you want to view: ");
    show_week_data(week_choice);

elseif choice == 2 then
    week1 = input("Enter the first week number for comparison (1-4): ");
    week2 = input("Enter the second week number for comparison (1-4): ");
    compare_weeks(week1, week2);

else
    disp("Invalid choice. Please enter either 1 or 2.");
End

DATA REPRESENTATION
The water consumption data for each week is stored in a matrix:
week1, week2, week3, and week4 represent the daily water consumption for each week (7 days).


consumption_data stores all weekly data in a single matrix where each row corresponds to one week's data.


FUNCTIONS USED IN THE PROGRAM: 
show_week_data(week_num): Displays the data of a specific week based on the user's choice.


compare_weeks(week1_num, week2_num): Compares the water consumption between two weeks by plotting them on a graph.


METHODOLOGY
The project was developed in Scilab by following the steps below:
Hardcoded Data: The data for 4 weeks was manually entered into the program as arrays. Each array corresponds to a week and contains 7 values representing the daily water consumption.


Menu Interface: A simple text-based menu was created, which prompts the user to input their choice. Based on the user’s input, the program either displays data for a specific week or compares two weeks.


Graphical Representation: For the comparison feature, Scilab's plotting functions were used to create line graphs. The plot() function was used to display the consumption data, and a legend, title, and labels were added for better readability.


Error Handling: The program ensures that the user can only select valid options (week numbers between 1 and 4). If the user enters invalid data, an error message is displayed.


RESULT 
The Water Consumption Tracker successfully displays and compares water consumption data over a four-week period. The user is able to input a week number and view the daily consumption data for that week. Additionally, the comparison feature allows users to visualize the differences in water consumption between two weeks.
CONCLUSIONS
This project demonstrates a simple and effective way to track and compare water consumption over time. It is hard coded with weekly data and provides more sophisticated analysis and recommendations.
The Water Consumption Tracker can be a useful tool for individuals or organizations looking to monitor and reduce water usage, ultimately promoting better water conservation practices.


REFERENCES
Scilab Documentation: https://www.scilab.org/
Wikipedia : https://www.wikipedia.org/


*****




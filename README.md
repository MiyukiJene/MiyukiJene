  # Chinese-English Dictionary of Academic Terms in Psychology
    #### Video Demo:  <URL HERE>
    #### Description:
    about my project:
    In the psychology.py, 
    1. Import the pandas as pd and import the display from IPython.display. 
    2. Add the file of Chinese-English Comparison Table of Psychological Academic Terms in CSV from "https://data.gov.tw/dataset/15167"
    3. I define a keyword search function so that I can find the corresponding English name even I don't know the full name of the academic title.
    4. Because there are some punctuation marks in wodrs, so I replace those punctuation marks in nothing, then I split the input keyword into sub-keywords by spaces.
    5. the program analy sub-keywords by using a for loop, searching for the keys in the keywords list. 
       If the "英文名稱"  field contains the sub-keyword "key," return True; otherwise, return False.
       Similarly, if the "中文名稱" field contains the sub-keyword "key," return True; otherwise, return False. 
       Finally, matching_records is updated with the records that meet the above conditions.
    6. Next, use the condition matching_records > 0 to determine whether any records that meet the search criteria have been found. If matching_records=0, print"Not Exist" and hint user to input again.
    7. create an empaty list"result" to store the result that match the follow requirement.
    8. Use a for loop along with iterrows() to iterate through all the information in matching_records.
       And then using `english_name = record['英文名稱']` and `chinese_name = record['中文名稱']`, find and record the values in the "英文名稱" (English name) and "中文名稱" (Chinese name) fields, 
       respectively, and store them in the variables `english_name` and `chinese_name`.
    9. The line results.append([english_name, chinese_name]) creates a list containing the values of "英文名稱" (English name) and "中文名稱" (Chinese name)
       , and then adds this list to the previously created results list, forming a two-dimensional list.Each element in the results list is itself a list containing the English name and the Chinese name.
    10. After the for loop finishes running, the records are returned to results, serving as the output result.
    11. Define a function `show_func` that takes `results` as a parameter.
    12. The line df = pd.DataFrame(results, columns=["英文名稱", "中文名稱"]) converts the results list into a Pandas DataFrame, with two columns named "英文名稱" and "中文名稱" respectively.
    13.Finally, the display function is used to present the DataFrame df in a tabular format, making it more convenient to view the results.
    14. Using if '__main__' == __name__: to check if the program is being executed as the main program.
    15. Using while True, the user can perform consecutive searches repeatedly until they input "*" to stop the search.
        The line choice = input('Please input a keyword or * (to stop searching): ') prompts the user to enter a keyword or "*", and stores the user's input in a variable named choice.
        And use choice = choice.strip() to remove leading and trailing spaces from choice to prevent any interference with the keyword search operation. 
        Next, if "" is detected, it stops the search and breaks out of the while loop. If "" is not detected, the else block is executed, and it stores the value of choice in the variable keyword.
    16. Using show_func(search_keyword(keyword)) to invoke the function for keyword search. The show_func() function is designed to take the results from search_keyword() as its parameter and display them in a tabular format in the IPython environment.

    

This project's main goal is to predict which Hogwart’s house a student will be assigned to, based on their characteristics, such as: species, hair and eye colour, wand properties, blood status, last name or special skills.

Prediction model was trained and tested with data from [Harry Potter Dataset](https://www.kaggle.com/datasets/gulsahdemiryurek/harry-potter-dataset).

Dataset ['Characters.csv'](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/Characters.csv) contains 140 rows of data described by 15 columns:
- Id
- Name
- Gender
- Job
- House
- Wand
- Patronus
- Species
- Blood status
- Hair colour
- Eye colour
- Loyalty
- Skills
- Birth
- Death

Data cleaning can be found in the file [**'hogwart_houses_data_cleaning.ipynb'**](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/hogwart_houses_data_cleaning.ipynb). The result of the source code is a new CSV file. Clean data was extracted from the raw data as follows:
- name splitted into first_name and last_name
- gender converted to boolean values (0 or 1)
- characters selection: is student, is teacher
- complete information about wand splitted into length, wood, core source and core element and converted to numeric values ([wood legend](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/wand_wood_dictionary.csv), [core source legend](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/wand_core_src_dictionary.csv), [core element legend](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/wand_core_part_dictionary.csv))
- patronus column extraction (only animal species) and convertion to numeric values ([legend](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/patronus_dictionary.csv))
- characters selection: human, giant, werewolf, goblin, ghost
- blood status selection: pure, half and muggle-born
- hair and eye colours extraction (only colour without tone) and convertion to numeric values
- characters loyalty selection: Dumbledore's Army, Order of the Phoenix and Lord Voldemort/Death eaters
- characters special skills selection: is highly skilled, is a student, is a prefect, have something in common with quidditch, have something in common with unforgivable curses
- Hogwart's houses names convertion ([legend](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/house_dictionary.csv)) to numeric values (prediction column)

Clean data can be found in the file [**'hogwart_houses.csv'**](https://github.com/musimartini/Projects/blob/main/own-projects/Hogwart%20Houses%20Classification/hogwart_houses.csv).

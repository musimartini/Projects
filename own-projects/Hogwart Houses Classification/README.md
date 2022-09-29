This project's main goal is to predict which Hogwart’s house a student will be assigned to, based on their characteristics, such as: species, hair and eye colour, wand properties, blood status, last name or special skills.

Prediction model was trained and tested with data from [Harry Potter Dataset](https://www.kaggle.com/datasets/gulsahdemiryurek/harry-potter-dataset).

Dataset 'Characters.csv' contains 140 rows of data described by 15 columns:
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

Data cleaning can be found in the file **'hogwart_houses_data_cleaning.ipynb'**. The result of the source code is a new CSV file. Clean data was extracted from the raw data as follows:
- name splitted into first_name and last_name
- gender converted to boolean values (0 or 1)
- characters selection: is student, is teacher
- complete information about wand splitted into length, wood, core source and core element and converted to numeric values*
- patronus column extraction (only animal species) and convertion to numeric values*
- characters selection: human, giant, werewolf, goblin, ghost
- blood status selection: pure, half and muggle-born
- hair and eye colours extraction (only colour without tone) and convertion to numeric values
- characters loyalty selection: Dumbledore's Army, Order of the Phoenix and Lord Voldemort/Death eaters
- characters special skills selection: is highly skilled, is a student, is a prefect, have something in common with quidditch, have something in common with unforgivable curses
- Hogwart's houses names convertion* to numeric values (prediction column)

\*Convertion to numeric values legend:
- wand_wood column: {'holly': 0, 'ash': 1, 'vine': 2, 'elder': 3, 'oak': 4, 'cherry': 5, 'willow': 7, 'mahogany': 8, 'cypress': 9, 'chestnut': 10, 'fir': 11, 'alder': 12, 'hazel': 13, 'hornbeam': 14, 'hawthorn': 15, 'walnut': 16, 'birch': 17, 'cedar': 18, 'elm': 19, 'yew': 20, 'snakewood': 21}
- 'wand_core_src': {'phoenix': 0, 'unicorn': 1, 'dragon': 2, 'thestral': 3, 'basilisk': 5}
- 'wand_core_part': {'feather': 0, 'hair': 1, 'heartstring': 2, 'horn': 4}
- 'patronus': {'stag': 0, 'terrier': 1, 'otter': 2, 'phoenix': 3, 'none': 4, 'non-corporeal': 5, 'unknown': 6, 'horse': 7, 'fox': 8, 'doe': 9, 'wolf': 10, 'cat': 11, 'weasel': 12, 'swan': 13, 'hare': 14, 'squirrel': 15, 'boar': 17}
- 'house': {'Gryffindor': 0, 'Ravenclaw': 1, 'Slytherin': 2, 'Hufflepuff': 3}

Clean data can be found in the file **'hogwart_houses.csv'**.

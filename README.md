## This package can give predictions on stability of new perovskite compoounds using machine learning approach.

## How to use:
1. New compounds info should be put in the ```newCompound.xlsx``` file, with the specified format as described in the excel file
2. The training data should be put in the ```perovskite_DFT_EaH_FormE.xlsx```. This file already contains over 1900 compounds. Users can add more compounds to this training set.
3. Run python script ```energy_prediction.py``` using command: ```python energy_prediction.py```. Requirements: 

** python version >= 3.5

** sklearn, pandas, numpy.

4. During the running of the python script, ```temporary files *.csv``` will be generated, which contain the generated features of the compounds in the training set and the new compounds to be predicted. The temporary files are generated by ```feature_vector.py```, called by the ```energy_prediction.py```. 
5. Results are put in the ```prediction_result.xlsx``` file. In the stability column, 1 stands for stable, 0 stands for unstable.

Information:
The energy_prediction embeds the selected best classification model (extra trees) and the best regression model (kernel ridge regression).
The elemental property database is provided as continousproperty.xlsx, discrictproperty.xlsx and shannon_perovskite.xlsx.
Feature inportance list is stored by *.txt files


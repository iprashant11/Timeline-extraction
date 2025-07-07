# Timeline-extraction

The topic extraction based on the keyBERT model

Application to convert .py using following command

    First we need to convert the .ipynb file to the .py using below command in cmd C:\Users\prashanti> jupyter nbconvert --to script UpdatedTimeExtractionAPI.ipyn
    now open the anaconda prompt and run the following commands activate the conda environment conda activate rag-env streamlit run UpdatedTimeExtractionAPI.py

Application hots on the port using following command in the anaconda prompt C:\Users\prashanti> python -m uvicorn UpdatedTimeExtractionAPI:app --host 0.0.0.0 --port 8004 --reload

Application to create the .bat file to run the all hosted python APIS

    Open the text file Copy the below content @echo off

:: Set path to your conda base installation CALL "C:\ProgramData\anaconda3\Scripts\activate.bat" C:\Users\prashanti.conda\envs\rag-env

:: Change directory to your project folder cd /d C:\Users\prashanti

:: Start TopicExtractionAPI in a new window start cmd /k "CALL C:\ProgramData\anaconda3\Scripts\activate.bat myenv && cd /d C:\Users\prashanti && python -m uvicorn UpdatedTimeExtractionAPI:app --host 0.0.0.0 --port 8004 --reload"

    Save as a .bat file
    Run the .bat file

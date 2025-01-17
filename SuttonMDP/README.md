Requirements
------------

This project is coded in Python 3.6 on Windows. Required packages include Numpy, Pandas and Matplotlib. Executes

>pip3 install numpy matplotlib pandas

or

>pip3 install -r requirements.txt

On Ubuntu 16.04, if getting error message "no module named _tkinter", then execute the following

>sudo apt-get install python3-tk


Generate Figures Using Random Training Sets
------------

Execute the following line to generate all three figures using new randomly generated training sets. Numerical results will also be displayed in the terminal.

>python3 all_figures.py

Then generated figures will be in the folder `figures` folder. The file name of the reproduced figures will look like `fig3_1550443283.png` where `1550443283` is a time stamp, so that new generated figures will not overwrite old ones.

To generate each figure separately, run the following commands. **Reproducing figure 3 may take half an hour to finish** because it is trying different alphas.

>python3 figure3.py

>python3 figure4.py

>python3 figure5.py

For reproducing `Figure 4`, the error TD(0) at α=0.6 could be between TD(0.3) and TD(0.8). Run the command `python3 figure4.py` three times or more to see a plot where the error TD(0) is above the error of TD(0.8), as shown in my report.

Generate The Same Figures in The Report
------------

Execute the following lines to generate exactly the same figures in my report, using files in the `data` folder. (However, this might fail due to compatibility problem of different Numpy and Pickle versions.)

>python3 all_figures.py -f

>python3 figure3.py -f

>python3 figure4.py -f

>python3 figure5.py -f

Folders
------------

`figures`: store geneated figure. Four figures used in the report are provided here. New figures generated by running the scripts are also stored here.

`data`: pickle files containing the experiment results that can generate the same figures in the report
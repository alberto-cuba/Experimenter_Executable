========================
BUILD OUTPUT DESCRIPTION
========================
To run the project it is necessary to have installed Java SE Development Kit 8, 
http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

When you build an Java application project that has a main class, the IDE
automatically copies all of the JAR
files on the projects classpath to your projects dist/lib folder. The IDE
also adds each of the JAR files to the Class-Path element in the application
JAR files manifest file (MANIFEST.MF).

To run the project from the command line, go to the dist folder and
type the following:

java -jar "moa.2016.04.jar" 

To distribute this project, zip up the dist folder (including the lib folder)
and distribute the ZIP file.
========================
RUN DESCRIPTION
========================
The Experiment tab allows to run several online learning algorithms over multiple datasets
and save the corresponding experiment results. The experiments can also be performed via
the command line.

Basically, the configuration of an experimental setting is performed in the Experiment tab.
For example, considering the following commands:
• ls: names of the algorithms separated by commas.
• lss: id of the algorithms separated by commas.
• ds: names of the streams separated by commas.
• dss: id of the streams separated by commas.
• rf: results folder.
• th: number of threads.
• ts: task
========================
RUNNING AN EXAMPLE
========================
1. Download the folder moa-experimenter-jar. This folder contains the libraries, the executable file moa.2016.04.jar, the datasets, and the scripts needed to run experiments both on Windows (script-w.bat) and Linux (script-l.sh).
2. Unzip the file datasets.7z containing the datasets in the folder moa-experimenter-jar. 
3. Run the script to perform the proposed experiment. For Linux, open a terminal at moa-experimenter-jar and run the command "bash script-l.sh"
 For Windows, double-click on script-w.bat. The experiment results will be saved to a folder named "Results",  which is created at moa-experimenter-jar.
4. To visualize and summarize the experiment results, it is necessary to run the MOA software via its GUI by typing the following command line: java -jar "moa.2016.04.jar".
5.  In the MOA GUI, click on the Experimenter tab. The Experimenter tab has four sub-tabs (Experiment, Summary, Plot, and Analyze):
-The "Experiment" tab allows to run several online learning algorithms over multiple datasets and save the corresponding experiment results (not needed for this example: we used the command line).
 -The "Summary" tab summarizes various performance measurements for different learning algorithms by means of tables in LaTeX and HTML formats. The summaries can be obtained when the experiments finish or by means of the "Results" folder. To open the results folder click on the "Browse" button and select the folder with the results that is in the same folder as the file moa.2016.04.jar.
To summarize the algorithms' performance measurements, first select the measure in the combobox "Measures". For example, select "classifications correct (percent)" and click on the "Add Measure" button. Then click on the "Show Summary" button and a window will appear with a summary of the algorithms' performance. That summary can be exported to any folder, by default it will be saved to the "Results" folder.
-The "Plot" tab generates figures representing the performance measures of various learning algorithms over time (in accordance with the experiment results previosly stored in the "Results" folder). Open the folder containing the experiment results and then click on the "Generate Images" button. A window listing all the generated images will be displayed. The images can be exported to the following formats: PNG, JPG, EPS, and SVG.
-The "Analyze" tab allows to verify significant differences between different algorithms by means of four different statistical tests: Friedman, Holm, Shaffer and Nemenyi.First open the folder with the results. Then in the combobox "Test", it  can be selected the statistical test to be executed, by default the Holm test is selected. It can also be set the p-value, the measure and the form in which the measurement is summarized, which can be by the average or by the last value. Next, click in the "Run Test" button.  To present the results in a simple way, the proposed software extension generates a figure representing significant differences by clicking on the Image button. The generated figure is applicable to any corrected p-value procedures for the post-hoc analysis. The image can be saved as PNG, JPG and EPS formats.
   

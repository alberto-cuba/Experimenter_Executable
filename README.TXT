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
1. Download the moa-experimenter-jar at https://github.com/alberto-cuba/moa-experimenter-jar. The moa-experimenter-jar folder contains the libraries to run the application, the executable file moa.2016.04.jar, the datasets, and the replicatios scripts, a .bat for windows and a .sh for linux. Please do not change the name of any of these files.
2. Unzip the folder datasets.7z with the data sets at the same level of the file moa.2016.04.jar. 
3. Run the replication script. For Unix system excute the command line at the same directory of the moa.2016.04.jar an type
bash script-l.sh. 
For Windows system double click on the script-w.bat file. This process may take several minutes. When the algorithms are finished, the results will be in the Results folder that is created at the same level of the file moa.2016.04.jar.
4. To visualize and summarize the results it is necessary to run the software via the GUI: type the following in command line, java -jar "moa.2016.04.jar"  
5. Click on the Experimenter tab. This tab has four tabs (Experiment, Summary,Plot,and Analyze):
-The Experiment tab allows to run several online learning algorithms over multiple datasets
and save the corresponding experiment results (not needed for the example since we execute the experiment via the command line).
-The Summary tab summarizes various performance measurements for different learning algorithms by means of tables in LaTeX and HTML formats. The summaries can be obtained when the experiments finish or by means of the Results folder. To open the results folder click on the Browse button and select the folder with the results that is in the same address as the file moa.2016.04.jar
To make the summary of the measurements, first you have to select the measure in the Combobox Measures, for example select "classifications correct (percent)" and click on the Add Measure button. Then click on the Show Summary button and the window appears with the results of the algorithms that can be exported to any folder, by default they are saved in the Results folder.
-The Plot tab generates figures representing the performance measurements of various learning
algorithms over time by means of the result folder. First open the folder with the results and then click on the Generate Images button. A window with all the generated images is displayed. The images can be exported in different formats, PNG, JPG, EPS and SVG; by default they are saved in the results folder.
-The Analyze tab allows to verify significant differences between algorithms with the Friedman test and the Holm, Shaffer and Nemenyi. First open the folder with the results. Then in the Combobox Test  can be selected the statistical test to execute, by default the Holm test is selected. You can also specify the pValue, the measure and the form in which the measurement is summarized, which can be by the average or by the last value. Next, click in the Run Test button.  To present the
results in a simple way, the proposed software extension generates a figure representing significant differences by clicking on the Image button. The generated figure is applicable to any corrected p-value procedures for the post-hoc analysis. The image can be saved as PNG, JPG and EPS formats.
   

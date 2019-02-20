# matsim-example-project

A small example of how to use MATSim as a library.

By default, this project uses the latest (pre-)release. In order to use a different version, edit `pom.xml`.

A recommended directory structure is as follows:
* `src` for sources
* `original-input-data` for original input data (typically not in MATSim format)
* `scenarios` for MATSim scenarios, i.e. MATSim input and output data.  A good way is the following:
  * One subdirectory for each scenario, e.g. `scenarios/mySpecialScenario01`.
  * This minimally contains a config file, a network file, and a population file.
  * Output goes one level down, e.g. `scenarios/mySpecialScenario01/output-from-a-good-run/...`.
  
  
### Import into eclipse

1. download a modern version of eclipse. This should have maven and git included by default.
1. `file->import->git->projects from git->clone URI` and clone as specified above.  _It will go through a 
sequence of windows; it is important that you import as 'general project'._
1. right-click on the project directory to `configure->convert to maven project`.  

To run the model: 

1. right-click on MATSimGUI.java in the folder src/main/java, org.matsim.gui and 
select Run As > Java Application.
1. Next to configuration file, select Choose and double-click the scenarios folder, RunCarshringIT, 
and config.xml. The output directory should be automatically set. Click Start MATSim to start the model.
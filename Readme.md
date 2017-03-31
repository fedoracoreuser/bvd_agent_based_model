# Preamble
This program is a simulation code written in C++ which is used to simulate the bovine viral diarrhea (BVD) and it's spread among farms. It has been developed at ITP (Institute of Theoretical Physics) at TU Berlin.

# Use of the code
## Compilation
Like most open source projects, this projects has not been build for users who do not already posses some knowledge in building C++ code on a Unix platform (I am not an expert at all). As you can see in the roadmap, making the code more accessible is a goal, but to be honest, it has to priority to me (Pascal Blunk) at the moment. If you are running windows, I have to tell you right now, that even I would not have any idea how to get this running on Windows. For Linux and mac OS (till Sierra), small text files which should make it easier to get this thing running have been provided (their names begin with 'install'). All other Unix flavors should be easily made up starting with those files. I am happy for any contribution to the code that increases the user friendliness of the code (GUI anyone?).

## Running the code
After successful compilation an executable called 'bvd_agent_simulation' can be found in the directory. So far it only has to options which can be added on the command line `--help` and `--ini`. The later one has to be used in order to provide an ini file which then specifies the behavior of the simulated system. Some ini files can be found in `/iniFiles/` so that the program can be run by executing `./bvd_agent_simulation --ini iniFiles/pascalTest.ini` (if your current working directory is indeed the main directory of the the repository).

# Development
A roadmap following the needs of FLI and TU Berlin has been proposed. 
## Roadmap
Several tasks have already been defined for the development of the code.

* Simulation Capability
** At the moment (Beginning of April 2017) the behavior of the market is determined by some very simple rules, leading to some kind of worst case scenario. In order to come up with more realistic results, a better market model based on loyalties between premises will be implemented.
** The biggest amount of time is used by the market for the process of choosing cattle to put them into the offer and demands driven market and doing the matchmaking. Making this part of the simulation thread safe and doing it in N threads should increase the performance of the code significantly.
* Output
** Fixing of the SQLite output 
** Including support for CSV file output
** Supporting turning on and off different output data (to minimize data size)
* Tests
** Since the code's size has grown in the course of writing multiple theses, the code needs to be tested properly
* usability 
** The code was not build with users in mind who are not as experienced with C++ or unix administration. One of the goals would be to include autogen in order to generate proper make files to ease up the building process. 

## Contribute
You can easily contribute to this project by forking it and starting pull requests. If you are interested in the corresponding research, feel to reach out to one of the main developers of this package.

## History
This project has been developed during a collaboration of Philipp Hövel and his working group at TU Berlin and Friedrich Loeffler Institut (FLI), which belongs to the German federal ministry of agriculture. The idea was to implement an agent based simulation with the cattle being the agents to simulate the disease of interest, since BVD is a very complex disease, which can not easily be described analytically. 

The code was started in November 2015 by Thomas Isele, PhD and then continued by Inia Steinbach, M.Sc. and Pascal Blunk, M.Sc.. The data for the simulation as well as all information on the disease as well as German legislation was provided by Jörn Gethmann, PhD (FLI) and Hartmut Lentz, PhD (FLI).

Jason Bassett is going to be the guy mainly responsible for the code on the site of TU Berlin, while Pascal Blunk is still going to contribute to this project. 

## Includes from other projects
The directory `projectImports` includes those libraries provided by other sources. By now it only contains a project called `inih` [https://github.com/benhoyt/inih](https://github.com/benhoyt/inih). It's license is the BSD License and can be found in the corresponding folder.

# Research 

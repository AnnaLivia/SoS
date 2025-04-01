# SoS - Solution Simulator

<p align="center">
  <img src="https://github.com/AnnaLivia/SoS/blob/main/figures/icon.png" width="100" />
</p>

**SoS** is an offline application for the case presented in

> Anna Livia Croella, Martina Gregori (2025) Case Article—Optimizing Food Donation Delivery for the Nonprofit Company Logica&Co. INFORMS Transactions on Education 0(0).
https://doi.org/10.1287/ited.2023.0042ca
<be>

and

> Anna Livia Croella, Martina Gregori (2025) Case—Optimizing Food Donation Delivery for Nonprofit Company Logica&Co. INFORMS Transactions on Education 0(0).
https://doi.org/10.1287/ited.2023.0042cs

**SoS** has been created using [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter), a Python UI library.
<br>
The application is compatible with Windows and macOS platforms.

> [!IMPORTANT]
> On macOS put the app in quarantine platforms by running the following command in a terminal:<br>
> <em>xattr -d com.apple.quarantine your/path/to/SoS/SoS_mac.app</em>

<br>
<br>

<p align="center">
  <img src="https://github.com/AnnaLivia/SoS/blob/main/figures/Figure1.png" width="531"/>
</p>

<p align="center"><b>Figure1:</b> SoS Home Frame.</p>

**SoS** needs three folders to be run: <em>data</em>, <em>input</em> and <em>output</em>.

#### Data
The <em>data</em> folder contains an Excel file named <em>Data.xlsx</em> with all the data required to model the Logica&Co problem. It includes:
<ul>
    <li> a list of all soup kitchens' parameters (sheet <em>Soup Kitchens</em>);</li>
    <li> a list of all local businesses' daily supply (sheet <em>Donations</em>);</li>
    <li> a list of all warehouses' parameters (sheet <em>Warehouses</em>);</li>
    <li> a list of all sponsors' parameters (sheet <em>Investments</em>);</li>
    <li> an origin-destination matrix of the distances from every warehouse to every local business (sheet <em>Distances W-LB</em>);</li>
    <li> an origin-destination matrix of the distances from every local business to every soup kitchen (sheet <em>Distances LB-S</em>);</li>
    <li> an origin-destination matrix of the distances from every soup kitchen to every warehouse (sheet <em>Distances S-W</em>);</li>
    <li> a list of supplementary parameters and coefficients (sheet <em>Additional Parameters</em>).</li>
</ul>

A file named <em>Data.txt</em>, summarizing all data reported in <em>Data.xlsx</em> in a text file, can also be generated using a **SoS** command <code>Print</code>.


#### Input
The <em>input</em> folder contains solution-alike </em>.txt</em> files.  To evaluate the quality of a proposed solution, users must populate this folder with the solution data.

#### Output
The <em>output</em> folder is the target folder for the simulation reports. After a simulation, the <em>\output</em> folder is automatically populated with a variable summary file and a report.

## How to use SoS

The **SoS** allows users to gain insights into a solution and inspect the framework data. A Map frame provides a navigable map of all soup kitchens, local businesses, and warehouses, and an Info frame summarizes the step-by-step procedure for running a simulation.

Within the Home frame, there are three command buttons:

<ul>
<li> <code>Print</code>: Print the model parameters in a file named <em>Data.txt</em> in the data folder. This file summarizes all model dimensions and parameters.
</li>
<li> <code>Upload</code>: Upload, check, and print the solution files inserted by the user in the input folder. If no errors are detected, a summary file <em>Variables.txt</em> is created and saved in the output folder; otherwise, a popup window with an error report appears.
</li>
<li> <code>Run simulation</code>: Run a simulation using the uploaded input values. If the inputs produce a feasible solution, all revenues and costs are calculated in detail by day, month, and semester (total) and stored in a file named <em>Report.txt</em> in the output folder. If the inputs lead to an infeasible solution, a popup window with an error report appears; details on the violated constraints can be found in the <em>Report.txt</em> file.
</li>
</ul>

# crystal_interpenetration_web
A web application for processing crystal structures, supporting CIF file uploads. It provides functionalities such as supercell generation, interpenetration expansion, and unit cell reduction. Built with Flask and pymatgen, the app features bilingual support (English/Chinese) for easy use in materials science research.

# User Manual
## 1.1 Software Download
(1) Download and install Anaconda (recommended version ≥ 3.8, compatible with Python environment management requirements);
(2) Visit the GitHub website, download the code compression package `crystal_interpenetration_web.zip`, and extract it to a specified local path (e.g., D:\ResearchTools\).

## 1.2 Usage Instructions
(1) Open Anaconda Navigator, click "Environments" on the left, and create a virtual environment via "Create" (recommended name: crystal_env, Python version ≥ 3.8);
(2) After activating the virtual environment, click "Open Terminal" to launch the terminal, and use the command `cd D:\ResearchTools\crystal_interpenetration_web` to navigate to the unzipped software directory;
(3) Enter `pip install -r requirements.txt` in the terminal to install dependent packages such as Flask, pymatgen, and numpy (ensure a stable internet connection and no errors during dependency installation);
(4) Enter `python app.py` to start the Web service. If the terminal displays "* Running on http://127.0.0.1:5000/", the service has started successfully;
(5) Open a browser and enter the address http://127.0.0.1:5000 to access the software's Web interface (supports Chinese-English bilingual switching; click the language icon in the upper right corner to switch);
(6) Click the "Upload File" button on the interface and select a local standard CIF format file (supports carbon-containing organic compounds, porous crystalline materials such as MOF/COF/HOF, etc.; file size ≤ 16MB);
(7) Set core parameters in the parameter configuration area:
- Number of Interpenetrating Layers: Enter the target number of layers (the system will automatically verify if it exceeds the maximum feasible number of layers; a prompt will be given if exceeded);
- Translation Vector Mode: Select "Auto Calculation" (evenly divided along the maximum cell expansion direction by default) or "Custom" (manually enter fractional coordinate vectors);
- Retain Chemical Bond Information: Check to generate result files containing chemical bond types and bond length information, compatible with visualization software such as VESTA;
(8) Click the "Generate Interpenetrating Structure" button. The system will automatically complete CIF parsing, layer count calculation, structure construction, and validity verification;
(9) Result Viewing and Download:
- View structure verification results (minimum atomic spacing, presence of invalid atomic pairs);
- Select the output format: Single CIF File (single-layer interpenetrating structure) or ZIP Package (batch packaging of multi-layer structures), and click "Download Results" to obtain the file;
(10) After the download is complete, the system will automatically clean up temporary files; no manual operation is required.

The parameter configuration interface of the Crystal Processor crystal structure interpenetration processing tool is as follows:

<img width="945" height="566" alt="image" src="https://github.com/user-attachments/assets/ec6e8266-cb6e-4493-ab26-b628c63dd908" />


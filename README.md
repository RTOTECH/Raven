
# Raven Setup Instructions

**Version 1.0.0 Beta**

## Prerequisites

Please read the full documentation [here](https://www.fosa-tech.com/sdr-resource-pages/using-raven)

Before proceeding, ensure you have the following installed on your system.
- Python 3
- `pip` + `virtualenv`
- `rtl-sdr` package, including `rtl_tcp` and `rtl_power`
- `hackrf_sweep` for the [HackRF](https://github.com/greatscottgadgets/hackrf)

## Installation and Setup

Before starting Rave, make sure that you have the backend tools like rtl_tcp, rtl_power, or hackrf_sweep installed and updated to the most current version. If you're on Windoze, make sure that you have these in your system PATH. Instuctions for all of this can be found with some quick Googleing. 

1. **Clone the Source Code**
   ```bash
   git clone https://github.com/RTOTECH/Raven.git
   ```

2. **Navigate to the Project Directory**
   ```bash
   cd Raven/
   ```

3. **Create a Python Virtual Environment:**
   ```bash
   python3 -m venv venv
   ```

4. **Activate the Virtual Environment:**
   ```bash
   source venv/bin/activate
   ```

5. **Install Dependencies:**
   ```bash
   python -m pip install -r requirements.txt
   ```

6. **Run the Flask Application:**
   ```bash
   python raven.py
   ```
   Note: this currently starts the Flask development server. Proper WSGI server support is coming soon.

## Usage

After completing the setup, the Flask application will be running on your local server. You can access it via `localhost:5000/rtl_data`.

1. Open the settings window, enter the desired wideband scan range and bin size, and start the scan.

2. Start the `rtl_tcp` server with the desired port and IP, and connect to it with your SDR software.

3. Select your desired rtl-tcp server instance by clicking on the current frequency, then `ctrl + left click` on the wideband window and Raven will automatically tune your SDR to it.

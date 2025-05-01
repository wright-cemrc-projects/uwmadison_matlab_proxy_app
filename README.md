# Batch Connect - OSC MATLAB Server

An OnDemand application to launch MATLAB as an HTTP server.

Install this repo within /var/www/ood/apps/sys.

This requires installing and separately setting up several items:

1. MATLAB on the worker node
2. Setup the Python wrapper 'matlab-proxy' from https://github.com/mathworks/matlab-proxy using a virtual environment.
3.   Worker node will need Python 3.8 or newer
4.   Setup with `python3.11 -m venv venv` to create the virtual environment in an accessible location like a network drive.
5.   Then `python -m pip install matlab-proxy`

The script in this OOD application will source the virtual environment and then will call the `matlab-proxy-app` to launch on the worker node
This will launch a web server and use a port that must be reachable from the OOD machine.

## Follow-ups
Is there a way to restrict the port range the matlab-proxy app can be launched on?

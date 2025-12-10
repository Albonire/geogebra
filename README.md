# GeoGebra Temperature Visualization

This project displays a GeoGebra applet that visualizes the temperature curves of a CPU and a GPU over time.

## Description

The `geogebra.html` file contains a self-contained web page that:

1.  Embeds a full-screen GeoGebra Classic applet.
2.  Sets up a coordinate system with time in seconds (`t (s)`) on the x-axis and temperature in Celsius (`T (°C)`) on the y-axis.
3.  Plots two temperature curves using analytical solutions:
    *   **CPU Temperature:** `T_cpu(t) = 140 * e^(-2t) - 70 * e^(-4t)`
    *   **GPU Temperature:** `T_gpu(t) = e^(-t) * (40 * cos(2t) + 25 * sin(2t))`
4.  Adds labels to the curves ("CPU" and "GPU").
5.  Calculates and displays the intersection point of the two temperature curves, labeled "Cruce" (Intersection).

The visualization is configured to load automatically when the page is opened.

## How to Use

Simply open the `geogebra.html` file in any modern web browser.

## Implementation Details

*   **GeoGebra Applet:** The project uses the official GeoGebra JavaScript library (`deployggb.js`) to embed the applet.
*   **Styling:** CSS is used to make the GeoGebra applet occupy the entire browser window (fullscreen).
*   **Automation:** A JavaScript script automates the process of:
    *   Injecting the applet into the page.
    *   Waiting for the GeoGebra engine to be ready.
    *   Executing a series of `evalCommand` calls to set up the graph, define the functions, and find the intersection point.
*   **Language:** The user interface of the GeoGebra applet is set to Spanish (`es`).

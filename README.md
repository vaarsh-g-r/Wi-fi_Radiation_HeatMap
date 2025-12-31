# Wi-Fi Radiation Pattern Analysis Using Smartphones

This project analyzes Wi-Fi radiation patterns using smartphones and visualizes the results with graphical heatmaps. By leveraging built-in smartphone sensors, we provide a cost-effective alternative to traditional Wi-Fi measurement tools.

## Features

* Smartphone-Based Measurement: Uses smartphones instead of expensive spectrum analyzers.
* Real-Time Mapping: Collects Wi-Fi signal data dynamically across different environments.
* Graphical Visualization: Generates heatmaps for signal strength, upload speed, and internet performance.
* Environmental Analysis: Evaluates the impact of population density and obstacles on Wi-Fi coverage.

## Methodology

1. Collect Wi-Fi signal data using smartphones (RSSI, upload speed, internet speed).
2. Map data points to specific coordinates on the floor plan.
3. Generate heatmaps using Python libraries (`pandas`, `matplotlib`, `seaborn`, `SciPy`).
4. Compare Wi-Fi performance in empty vs. populated environments.

## Tech Stack

* Python
* Pandas, Seaborn, Matplotlib, SciPy
* OpenCV (for overlaying heatmaps on floor maps)

## How to Use

1. Prepare a CSV file with Wi-Fi measurements (`xcoordinate`, `ycoordinate`, and parameters).
2. Provide a floor plan image.
3. Run the `create_heatmap` function to generate heatmaps and overlay them on the floor plan.

```python
# Example
csv_file = "PhysicsProjectData.csv"
floor_map = "map.jpeg"
output_directory = "heatmaps"
columns_to_visualize = ['InternetSpeedClean', 'InternetSpeedNoise', 'UploadSpeed']
for column in columns_to_visualize:
    create_heatmap(csv_file, floor_map, output_directory, column, "xcoordinate", "ycoordinate")
```

## Future Work

* Incorporate machine learning for better signal prediction.
* Extend analysis to 5G and IoT environments.
* 3D visualizations and health/safety studies of Wi-Fi radiation.

## Authors

* K. Sai Jyothirmayi
* Jenita Rachel C
* Lakshana Baskaran
* Vaarshini R
* Vandana Padman

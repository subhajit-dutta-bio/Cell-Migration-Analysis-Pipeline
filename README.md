# Cell-Migration-Analysis-Pipeline
This pipeline processes Trackmate spot CSV files to extract important biophysical and migratory parameters, visualize behavior over time, and statistically compare experimental conditions.


📖 Introduction
This notebook provides a comprehensive, interactive, and reproducible pipeline for analyzing cell migration datasets generated by TrackMate (an open-source tracking tool in Fiji/ImageJ).

TrackMate detects and tracks individual cells or particles across time-lapse microscopy images. It outputs CSV files containing positional coordinates (POSITION_X, POSITION_Y, POSITION_Z) and time/frame information (FRAME).
Our pipeline processes these CSV files to extract important biophysical and migratory parameters, visualize behavior over time, and statistically compare experimental conditions.

This tool is particularly useful for comparing different treatments, genetic modifications, or environmental conditions affecting cell motility.

🛠️ Measurements and Features Calculated
For each track (individual cell trajectory), the following features are extracted:

Mean Speed (μm/min): Average movement speed over time.

Total Displacement (μm): Straight-line distance from start to end.

Total Distance Travelled (μm): Cumulative path length.

Directionality (ratio): Straightness of the path (displacement / total distance).

Track Duration (frames): Time from first to last detection.

Asphericity: Shape irregularity of the trajectory (based on covariance of x and y).

Mean Square Displacement (MSD): Time-lagged spatial exploration behavior.

Mean Turning Angle (radians): Angular deviation between steps.

Velocity Vectors: Instantaneous movement vectors between frames.

Displacement Angle: Final angle between start and end points.

Additionally:

Instantaneous Speed Plot (per condition)

Directionality Polar Plot and Animated Rose Plots

Statistical comparisons between groups (auto-selected tests based on normality/homogeneity).

🧪 Usage Guidelines
Requirements
Input data: TrackMate exported .csv files (one or multiple files per condition).

The notebook will automatically guide you interactively:

Upload your CSV files to Colab.

Specify the number of experimental conditions.

Assign files to each condition.

Run the full pipeline to compute features, create plots, movies, and perform statistical analysis.

Outputs will be packaged into a downloadable .zip file containing:

CSV summary of extracted features

CSV of statistical test results

Box plots, strip plots, and rose plots (both raw and statistically annotated)

Animated MP4 movies of speed and directionality evolution

📜 Usage Policy
Free for academic use.

If you use this notebook or its output in your research:

Acknowledge its usage in your Methods section.

Cite the corresponding publication if a paper based on this pipeline appears (forthcoming).

Disclaimer:

The author is not responsible for any errors, misinterpretations, or modifications made to this pipeline after download.

Users are encouraged to validate outputs against their experimental expectations.

# MPPI for RoboRacer (F1/10 Autonomous Racing)
This repository contains an implementation of **Model Predictive Path Integral (MPPI) control**
for F1/10 platform, developed for the **final race** of
**ESE 6150 – F1/10 Autonomous Racing**.

**Note:** To enable JAX to run on a GPU, you may need to uncomment line 23 in [mppi_node.py](mppi/scripts/mppi_node.py).

## Run MPPI on your own waypoints
- First, you need to have a CSV file that records Cartesian coordinates (I assume it has two columns: `x_position` and `y_position`). This can be obtained using a `waypoint_logger` or the drawing tool (available in the [Pure Pursuit lab](https://github.com/f1tenth-class/slam-and-pure-pursuit-team9)).
- Next, run `process_waypoint.py` in [mppi/scripts/waypoints](mppi/scripts/waypoints). This program converts the raw waypoint file into a CSV file formatted for use with MPPI.
- Update the `wpt_path` in [mppi/scripts/config.yaml](mppi/scripts/config.yaml) and [mppi/scripts/waypoints/map_info.txt](mppi/scripts/waypoints/map_info.txt) to point to the waypoint file you just generated.


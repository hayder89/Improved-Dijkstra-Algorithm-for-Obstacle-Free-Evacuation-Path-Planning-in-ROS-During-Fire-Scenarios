# Robot
# Dynamic Capacity and Obstacle-Aware Evacuation Path Planning in Fire Scenarios Using an Enhanced Dijkstra Algorithm

This ROS package implements a basic obstacle-free path planner using the **Dijkstra algorithm**, assuming a clean, known environment with no sensors involved. The planning logic is influenced by the **ratio of the length to width**, which determines path cost heuristics and movement preferences.

---

## ✅ Features

- Obstacle-awareness path planning
- Purely geometric map-based navigation
- Adjustable planning area (length & width)
- Path optimization based on L/W ratio
- Lightweight and sensor-free
- Designed for simulation or controlled environments

---

## 🧾 Assumptions

- The environment has **some obstacles**.
- The robot operates on a known 3D .
- No sensor data is used.
- Start and goal positions are manually provided.
- The improved Dijkstra algorithm is used for shortest path generation.

---

## 📥 Inputs (10 Parameters)

1. `start_x`: Start position X (int)
2. `start_y`: Start position Y (int)
3. `goal_x`: Goal position X (int)
4. `goal_y`: Goal position Y (int)
5. `map_length`: Length of the map/grid (int)
6. `map_width`: Width of the map/grid (int)
7. `resolution`: Grid resolution 
8. `length_width_ratio_weight`: A tuning weight for cost scaling based on map proportions
9. `diagonal_movement`: Allow diagonal movement (`true/false`)

---
Project Structure

```bash
dijkstra_path_planner/
├── launch/
│   └── planner.launch
├── src/
│   └── dijkstra_planner_node.py
├── config/
│   └── planner_params.yaml
├── scripts/
│   └── grid_utils.py
├── CMakeLists.txt
├── package.xml
└── README.md

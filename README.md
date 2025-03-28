# MinTopGraph

MinTopGraph is a Python implementation for computing and visualizing minTopGraphs in multi-dimensional data spaces. This tool helps in analyzing and understanding the structure of data points in both 2D and high-dimensional spaces, with a focus on skyline computation and group max-rank analysis.

## Features

- Support for both 2D and high-dimensional data analysis
- Skyline computation and visualization
- Group max-rank calculation
- Minimum top-k graph estimation
- Query space analysis

## Prerequisites

- Python 3.x
- Required Python packages:
  - pandas
  - numpy
  - matplotlib (for visualization)

## Installation

1. Clone this repository:
```bash
cd minTopGraph
```

2. Install the required dependencies:
```bash
pip install pandas numpy matplotlib
```

## Usage

The main script can be run using the following command:

```bash
python main.py path/to/datafile increment_of_k compute_group_max_rank
```

Parameters:
- `datafile`: A CSV file containing normalized data points with associated IDs
- `increment_of_k`: The increment value for estimating q(s) in the MinTopGraph algorithm
- `compute_group_max_rank`: Boolean value indicating whether to compute GroupMaxRank (default: True)

### Required Input Files

For the program to work, the following files must be present in the same directory as your data file:
- `skyline.csv`: Contains the skyline of the dataset
- `maxrank.csv`: Contains the maxrank of each skyline point
- `cellsout.csv`: Contains the mincells for 2D datasets
- `cells.csv`: Contains the mincells for high-dimensional datasets

## Examples

The project includes various example datasets in the `examples/` directory:
- 2D datasets (uniform, normal, exponential, correlated)
- 3D datasets
- Real-world datasets (laptops, housing, Spotify, Airbnb)

## Output

The program generates one or two graphs depending on the dataset dimensions:
- MinTopGraph is always displayed
- Query space and skyline are displayed for 2D datasets

## Project Structure

- `main.py`: Main entry point of the program
- `gGraph.py`: Core graph estimation functionality
- `maxrank.py`: Maxrank computation implementation
- `qtree.py`: Query tree implementation
- `geom.py`: Geometric utilities
- `queryutils.py`: Query-related utility functions
- `GroupMaxRank.py`: Group max-rank computation

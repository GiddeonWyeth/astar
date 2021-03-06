astar
=====

A small package that implements the A\* (A star) pathfinding algorithm.

Example
-------

	import (
		"fmt"
		"github.com/sperre/astar"
	)

	func main() {
		// If your map is something more than 2D matrix then you might want to modify adjacentNodes
		map_data := astar.GetMapFromImage(test.png)

		// Returns a list of nodes from start to stop avoiding all, obstacles if possible
		startx, starty :=  0,  0
		stopx, stopy   := 99, 99
		dir8 := false // Use 4 directions, not 8
		shortest_path := astar.Astar(map_data, startx, starty, stopx, stopy, dir8)
	}

Origin
------

This library was developed for Eurobot-NTNU 2012,
based on code from: https://github.com/humanfromearth/gopathfinding

Compared to the original library, our version was benchmarked to run
approximately 27x faster.

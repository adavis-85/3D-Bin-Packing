# 3D Bin Packing

1. Partition the items into clusters by non-increasing height and then construct optimal bins using a 1D bin packing problem.
2. The items are then re-sorted by non-increasing base area (width by depth) and a second solution is obtained using a 1D bin packing problem.

Each layer is formed using a 2DBP:

1. Sort the items by non-increasing height.
2. Place the items with the first at the bottom left corner of the container.
3. Add items sharing an edge as close as possible to the right edge of the container
4. Place the next item on the minimum height item with the right edge touching the right edge of the container.
5. Place items sharing edges consecutively until none can fit or the left edge of the last item touches the left edge of the container with it's left edge.
6. Alternate placing items left to right and right to left until none can be placed in either direction.
    
These layers are then used to construct bins with the objective being to use the fewest bins possible.




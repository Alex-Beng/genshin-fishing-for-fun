# genshin-fishing-for-fun(G-triple-F)

Focus on the **throwing the rod**, rather than the whole fishing process, 
cause it is done with so many other tools. Also, just focus on the **Algorithm** itself, so never mind the how ugly the UI/code/etc. is.

It's only in planning, trying to use more 3d vision algorithms to make it more robust in different-scenes' rod-throwing.

## Development Plan

- [x] 1. For language: mainly Python, maybe cpp or rust for deployment.
- [ ] 2. Algorithm structure: Detection + 3d vision + Control.
- [ ] 3. Detection: 
    - [ ] 1. common object that unchanged in different scenes like UI objs: just easily use contour + color/Hu moments/area/width_height_ratio/etc. , keep it easy and simple, which is robust enough.
    - [ ] 2. slilghtly changed objs like the target: use hough transform to detect the circle, then use the circle's center to calculate the distance between the rod and the target. 
    - [ ] 3. move-dynamic objs like the fish: use gaussian blur + filter to detect and predict the fish's movement, then use the center of the fish to calculate the distance between the rod and the fish.
- [ ] 4. 3d vision:
    - [ ] 1. Estimate the H matrix to transform the 2d fishing surface to known 2d surface. Maybe estimate the 3d position as well ? 
    - [ ] 2. target + fish velocity and position estimation in the 2d surface.
- [ ] 5. Control:
    - [ ] 1. control the target moving with the known fishs position and velocity.
    - [ ] 2. high-level control: FSM ?


# detach-instances
A Figma plugin to detach all component instances contained in your selection, or on the current page.

# Update
Turns out this is a pretty hard problem to solve. On detaching an instance, the instance is replaced with all the layers in the instance. This drastically increases the memory consumption in the file. Do this for all the layers in an entire page and you will likely crash Figma.

I'd started working on this plugin to find a reliable way to 'freeze' design (for documentation) and not have to evolve as I updated my components. Since discovering the memory implications of detaching instances, I have abandoned the approach.

My current solution is to use Figma's newly added branching feature. One can create new branches to preserve the state of a design. Branches do not receive updates from the master file, and hence the design is preserved as it was when the branch was created.

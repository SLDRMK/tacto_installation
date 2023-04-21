# tacto_installation
Here are some issues occured in the configuration of tacto envioronment.
1. torch, gym, pybulletX are not available in conda, but can be installed from pip
2. some importing problems
	- from collections import Mapping $\rightarrow$ from collections.abc import Mapping
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/networkx/classes/graph.py
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/networkx/classes/coreviews.py
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/networkx/classes/reportviews.py
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/networkx/algorithms/lowest_common_ancestors.py
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/attrdict/mapping.py
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/attrdict/mixins.py
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/attrdict/merge.py
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/attrdict/default.py
	- from fractions inmport gcd $\rightarrow$ from math import gcd
		- ome/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/networkx/algorithms/dag.py
	- from collections import Set $\rightarrow$ from collections.abc import Set
		- /home/sldrmk/anaconda3/envs/pytorch/lib/python3.10/site-packages/networkx/algorithms/lowest_common_ancestors.py
3. example errors:
	- errors:
		- pyglet.gl.ContextException: Could not create GL context
		- Set the environment variable HYDRA_FULL_ERROR=1 for a complete stack trace.
	- solution1:
		- nvidia-settings
		- PRIME Profiles
		- NVIDIA (Performance Mode)
	- solution2-with-no-core-graphics-card:
		- install some dependencies
			- sudo apt-get install build-essential libgl1-mesa-dev
			- sudo apt-get install libglew-dev libsdl2-dev libsdl2-image-dev libglm-dev libfreetype6-dev
			- sudo apt-get install libglfw3-dev libglfw3

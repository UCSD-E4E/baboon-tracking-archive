# baboon-tracking-archive
This is where all the old stuff from baboon team lives. Due to multiple failed approaches and refactors, a lot of deprecated code was moved to this repo to be archived.

## Included Projects
### scraper
Webscraper to download streamed videos from the San Diego Zoo's [Baboon Live Cams](https://zoo.sandiegozoo.org/cams/baboon-cam). These videos habe been determined to not be useful at the current time in the project, as drone footage has very different properties.
### kcf_tracking
Attempt to track baboons using Kernelized Correlation Filters. (TODO: Insert blurb here to explain how well this worked)
### background_subtraction
Attempt to detect baboons using simple background subtraction methods. Works well with stationary cameras, but translational and rotational background movement causes issues with this approach.
### opencv_builtin_tracking
Interactive test of various common builtin [opencv tracking methods](https://www.learnopencv.com/object-tracking-using-opencv-cpp-python/). Allows user to draw bounding box around baboon, and attempts to track it for duration of the video. Only able to track, not detect baboons.
### variable_background_tracking
Attempt to isolate moving foreground from a variable background by implementing the algorithm described in [this paper](https://arxiv.org/abs/1706.02672). At the moment, algorithm works well but is incredibly slow, as it has not been optimized for performance.
### registration_bg_subtraction
Use registration (stabilization) functions from variable_background_tracking, and apply regular background subtraction on the results

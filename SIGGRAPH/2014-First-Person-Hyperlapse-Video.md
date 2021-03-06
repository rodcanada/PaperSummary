##First-person Hyperlapse Videos

Johannes Kopf, Michael F. Cohen and Richard Szeliski

[website](http://research.microsoft.com/en-us/um/redmond/projects/hyperlapse/) / [pdf](http://research.microsoft.com/en-us/um/redmond/projects/hyperlapse/paper/hyperlapse.pdf)

###Abstract
We present a method for converting first-person videos, for example, captured with a helmet camera during activities such as rock climbing or bicycling, into hyper-lapse videos, i.e., time-lapse videos with a smoothly moving camera. 

At high speed-up rates, simple frame sub-sampling coupled with existing video stabilization methods does not work, because the erratic camera shake present in first-person videos is amplified by the speed-up. 

Our algorithm first reconstructs the 3D input camera path as well as dense, per-frame proxy geometries. We then optimize a novel camera path for the output video (shown in red) that is smooth and passes near the input cameras while ensuring that the virtual camera looks in directions that can be rendered well from the input.
Next, we compute geometric proxies for each input frame. These allow us to render the frames from the novel viewpoints on the optimized path.	

Finally, we generate the novel smoothed, time-lapse video by rendering, stitching, and blending appropriately selected source frames for each output frame. We present a number of results for challenging videos that cannot be processed using traditional techniques.

###Bibtex
```
@article{kopf2014first,
  title={First-person hyper-lapse videos},
  author={Kopf, Johannes and Cohen, Michael F and Szeliski, Richard},
  journal={ACM Transactions on Graphics (TOG)},
  volume={33},
  number={4},
  pages={78},
  year={2014},
  publisher={ACM}
}
```

### Pipelines
 - Scene reconstruction
 - Path planning
 - Image-based rendering

### Used techiques
 - SfM (Struct from motion) [2006 Photo Tourism](2006-Photo-Tourism.md)
 - MRF (Markov Random Field)

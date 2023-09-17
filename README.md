Background  
====
Autonomous navigation in unknown indoor environments using an RGB-D camera is a challenging task, especially when utilizing the feature-based visual simultaneous localization and mapping (SLAM) methods. The existence of low-texture scenes, such as narrow corridors and white walls, may lead to frequent tracking failure of indoor features. Recent works show that incorporating some form of map-like spatial memory can aid the performance of visual navigation. Therefore, we propose to add saliency information to map-like spatial memory to enable the learning-based agent to be better aware of the obstacle positions and visual importance of different regions, thus better avoiding tracking failure issues in low-texture environments. Visual saliency or visual attention mechanism refers to mimic the human vision system to select the most salient and interesting features from natural scenes for further processing under different tasks. This is also very important for visual navigation because visual saliency awareness directs the agent’s perceptual attention towards the salient regions containing sufficient visual features in the process of approaching the target. There are several datasets used for saliency prediction. By analyzing the data of those datasets, we can ﬁnd that these datasets have the following characteristics. (1) Saliency is highly relevant to dynamic objects or the dynamic part of the object. (2) Newly appearing objects are more noticeable than old ones. (3) When the scene is cluttered or there is no obvious dominant object in the scene, the attention will be biased to the center. However, this saliency does not completely describe everything the visual navigation should attend to, and even some saliency will cause the failure of the visual SLAM, such as the saliency associated with dynamic objects. Therefore, we should make our saliency prediction model focusing on the right stuff.

Ground-truth Saliency Map Computation  
====
We propose a novel approach to compute the ground-truth saliency map by incorporating both geometric and semantic information. Our visual SLAM method adopts the feature-based method’s strategy, which extracts and matches features. Therefore, we should make our saliency prediction model focusing on the regions with rich features.

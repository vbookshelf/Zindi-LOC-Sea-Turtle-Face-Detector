## Zindi-LOC-Sea-Turtle-Face-Detector
A method to detect sea turtle faces using a segmentation approach combined with connected components.

<br>

<img src="http://bee.test.woza.work/assets/turtles1.png" width="700"></img>

<br>

I created this solution for the Local Ocean Conservation - Sea Turtle Face Detection knowledge competition on Zindi.<br>
https://zindi.africa/competitions/local-ocean-conservation-sea-turtle-face-detection

The notebook included in this repo describes how to use a segmentation approach combined with connected components to detect sea turtle faces. I've used a pre-trained MobileNet encoder combined with a U-Net decoder. This is a simple single model setup without any ensembling or fold averaging. The model was trained on Google Colab for 30 epochs. Training time was approx. 30 seconds per epoch when using a Tesla T4 GPU.

The model produced a leaderboard IOU score of 0.828. It has a size of approx 27MB.

It's possible to get a leaderboard score of approx. 0.87 by using larger encoder networks like Densenet161. However, I believe that even though this model's leaderboard score is slighly lower, its small size combined with mobilenet's speed makes it a better candidate for use in a production system.

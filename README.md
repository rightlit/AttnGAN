# AttnGAN-revision for Colab

This is AttnGAN revised version for Google Colab.

Refer to [https://github.com/taoxugit/AttnGAN](https://github.com/taoxugit/AttnGAN) for original source version, <br>
it is implementation for the paper [AttnGAN: Fine-Grained Text to Image Generation with Attentional Generative Adversarial Networks](http://openaccess.thecvf.com/content_cvpr_2018/papers/Xu_AttnGAN_Fine-Grained_Text_CVPR_2018_paper.pdf).

Refer to troubleshooting [issues](https://github.com/rightlit/AttnGAN-rev/issues) while running with original source code. 

### Dependencies
python 3.6

Pytorch 1.7.0+cu101


**Data**

1. Download preprocessed metadata for [birds](https://drive.google.com/open?id=1O_LtUP9sch09QH3s_EBAgLEctBQ5JBSJ) [coco](https://drive.google.com/open?id=1rSnbIGNDGZeHlsUlLdahj0RJ9oo6lgH9) and save them to `data/`
2. Download the [birds](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html) image data. Extract them to `data/birds/`
3. Download the [flowers](http://www.robots.ox.ac.uk/~vgg/data/flowers/102/) image data. Extract them to `data/flowers/`
4. Download [coco](http://cocodataset.org/#download) dataset and extract the images to `data/coco/`


**Sampling**
- Run `python main.py --cfg cfg/eval_bird.yml --gpu 1` to generate examples from captions in files listed in "./data/birds/example_filenames.txt". Results are saved to `DAMSMencoders/`. 
- Run `python main.py --cfg cfg/eval_flower.yml --gpu 1` to generate examples from captions in files listed in "./data/flowers/example_filenames.txt". Results are saved to `DAMSMencoders/`. 
- Change the `eval_*.yml` files to generate images from other pre-trained models. 
- Input your own sentence in "./data/birds/example_captions.txt" if you wannt to generate images from customized sentences. 

**Examples generated by AttnGAN**


 bird example              |  bird example
:-------------------------:|:-------------------------:
the medium sized bird has a dark grey color, a black downward curved beak, and long wings. | the bird is dark grey brown with a thick curved bill and a flat shaped tail.
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_0_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_0_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_0_g2.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_1_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_1_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_1_g2.png)
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_0_a0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_0_a1.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_1_a0.png)![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_1_a1.png)
bird has brown body feathers, white breast feathers and black beak | this bird has a dark brown overall body color, with a small white patch around the base of the bill.
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_2_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_2_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_2_g2.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_3_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_3_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_3_g2.png)
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_2_a0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_2_a1.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_3_a0.png)![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_3_a1.png)
the bird has very long and large brown wings, as well as a black body and a long black beak. | it is a type of albatross with black wings, tail, back and beak, and has a white ring at the base of its beak.
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_4_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_4_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_4_g2.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_5_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_5_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_5_g2.png)
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_4_a0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_4_a1.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_5_a0.png)![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_5_a1.png)
this bird has brown plumage and a white ring at the base of its long, curved brown beak. | the entire body is dark brown, as is the bill, with a white band encircling where the bill meets the head.
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_6_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_6_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_6_g2.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_7_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_7_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_7_g2.png)
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_6_a0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_6_a1.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_7_a0.png)![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_7_a1.png)
this bird is gray in color, with a large curved beak. | a large gray bird with a long wingspan and a long black beak.
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_8_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_8_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_8_g2.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_9_g0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_9_g1.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_9_g2.png)
![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_8_a0.png) ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_8_a1.png) | ![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_9_a0.png)![](models/bird_AttnGAN2/Black_Footed_Albatross_0001_796111/0_s_9_a1.png)

 flower example              |  flower example
:-------------------------:|:-------------------------:
the petals of the flower are pink in color and have a yellow center. | this flower is pink and white in color, with petals that are multi colored.
![](models/netG_epoch_600/image_06734/0_s_0_g0.png) ![](models/netG_epoch_600/image_06734/0_s_0_g1.png) ![](models/netG_epoch_600/image_06734/0_s_0_g2.png) | ![](models/netG_epoch_600/image_06734/0_s_1_g0.png) ![](models/netG_epoch_600/image_06734/0_s_1_g1.png) ![](models/netG_epoch_600/image_06734/0_s_1_g2.png)
![](models/netG_epoch_600/image_06734/0_s_0_a0.png) ![](models/netG_epoch_600/image_06734/0_s_0_a1.png) | ![](models/netG_epoch_600/image_06734/0_s_1_a0.png)![](models/netG_epoch_600/image_06734/0_s_1_a1.png)
the geographical shapes of the bright purple petals set off the orange stamen and filament and the cross shaped stigma is beautiful. | the purple petals have shades of white with white anther and filament
![](models/netG_epoch_600/image_06734/0_s_2_g0.png) ![](models/netG_epoch_600/image_06734/0_s_2_g1.png) ![](models/netG_epoch_600/image_06734/0_s_2_g2.png) | ![](models/netG_epoch_600/image_06734/0_s_3_g0.png) ![](models/netG_epoch_600/image_06734/0_s_3_g1.png) ![](models/netG_epoch_600/image_06734/0_s_3_g2.png)
![](models/netG_epoch_600/image_06734/0_s_2_a0.png) ![](models/netG_epoch_600/image_06734/0_s_2_a1.png) | ![](models/netG_epoch_600/image_06734/0_s_3_a0.png)![](models/netG_epoch_600/image_06734/0_s_3_a1.png)
this flower has large pink petals and a white stigma in the center | this flower has petals that are pink and has a yellow stamen
![](models/netG_epoch_600/image_06734/0_s_4_g0.png) ![](models/netG_epoch_600/image_06734/0_s_4_g1.png) ![](models/netG_epoch_600/image_06734/0_s_4_g2.png) | ![](models/netG_epoch_600/image_06734/0_s_5_g0.png) ![](models/netG_epoch_600/image_06734/0_s_5_g1.png) ![](models/netG_epoch_600/image_06734/0_s_5_g2.png)
![](models/netG_epoch_600/image_06734/0_s_4_a0.png) ![](models/netG_epoch_600/image_06734/0_s_4_a1.png) | ![](models/netG_epoch_600/image_06734/0_s_5_a0.png)![](models/netG_epoch_600/image_06734/0_s_5_a1.png)
a flower with short and wide petals that is light purple. | this flower has small pink petals with a yellow center.
![](models/netG_epoch_600/image_06734/0_s_6_g0.png) ![](models/netG_epoch_600/image_06734/0_s_6_g1.png) ![](models/netG_epoch_600/image_06734/0_s_6_g2.png) | ![](models/netG_epoch_600/image_06734/0_s_7_g0.png) ![](models/netG_epoch_600/image_06734/0_s_7_g1.png) ![](models/netG_epoch_600/image_06734/0_s_7_g2.png)
![](models/netG_epoch_600/image_06734/0_s_6_a0.png) ![](models/netG_epoch_600/image_06734/0_s_6_a1.png) | ![](models/netG_epoch_600/image_06734/0_s_7_a0.png)![](models/netG_epoch_600/image_06734/0_s_7_a1.png)
this flower has large rounded pink petals with curved edges and purple veins. | this flower has purple petals as well as a white stamen.
![](models/netG_epoch_600/image_06734/0_s_8_g0.png) ![](models/netG_epoch_600/image_06734/0_s_86_g1.png) ![](models/netG_epoch_600/image_06734/0_s_8_g2.png) | ![](models/netG_epoch_600/image_06734/0_s_9_g0.png) ![](models/netG_epoch_600/image_06734/0_s_9_g1.png) ![](models/netG_epoch_600/image_06734/0_s_9_g2.png)
![](models/netG_epoch_600/image_06734/0_s_8_a0.png) ![](models/netG_epoch_600/image_06734/0_s_8_a1.png) | ![](models/netG_epoch_600/image_06734/0_s_9_a0.png)![](models/netG_epoch_600/image_06734/0_s_9_a1.png)


**Reference**

- [StackGAN++: Realistic Image Synthesis with Stacked Generative Adversarial Networks](https://arxiv.org/abs/1710.10916) [[code]](https://github.com/hanzhanggit/StackGAN-v2)
- [Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks](https://arxiv.org/abs/1511.06434) [[code]](https://github.com/carpedm20/DCGAN-tensorflow)

# AlexNet
### Alex主要使用到的新技术点如下：
   *  <font size="16" color="black" >（1）成功的使用ReLU作为CNN的激活函数，并验证了其效果在较深的网络超过了Sigmoid,成功解决了Sigmod在网络较深时的梯度弥散问题</font>
   *  <font size="16" color="black">（2）训练时使用Dropout随机忽略一部分神经元，以避免模型过拟合。</font>
   *   <font size="16"  color="black">（3）在CNN中使用重叠的最大池化。此前CNN中主要使用的是平均池化，AlexNet全部使用最大池化，避免了平均池化的模糊效果。并且Alex提出让步长比池化核的尺寸小，这样池化层的输出之间会有重叠和覆盖，提升了特征的丰富性。</font>
   *   <font size="16"  color="black">（4）提出了LRN层，对局部神经元的活动创建竞争机制，是的其中相应比较大的值变得相对更大，并抑制其他反馈较小的神经元，增强了模型的泛化能力。</font>
   * <font size="16"  color="black">（5）使用CUDA加速深度卷积网络的训练，Alex分布在两个GPU上，在每个GPU的显存中存储一半的神经元参数。因为GPU互相通信方便，不需要经过主机内存。同时Alex设计让GPU之间通信只在网络的某些层进行，控制了通信性能的损耗。</font>
   * <font size="17"  color="black">（6）数据增强：图像截取+水平翻转镜像</font>


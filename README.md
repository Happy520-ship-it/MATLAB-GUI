一、课题介绍

随着汽车数量的增加，城市交通状况日益受到人们的重视，如何进行有效的交通管理更是成为了人们关注的焦点。智能交通系统通过车辆检测装置对过往的车辆实施检测，提取有关交通数据，达到监控、管理和指挥交通的目的。因此，它已成为世界交通领域研究的重要课题。 车牌识别系统作为智能交通系统的一个重要组成部分，已在高速公路、城市交通和停车场等项目的管理中占有无可取代的重要地位。它在不影响汽车状态的情况下，由计算机自动完成车牌的识别，从而降低交通管理工作的复杂度。
该课题为基于MATLAB的汽车出入库识别系统，带有丰富的人机交互GUI界面。目前毕业设计选题中，传统车牌识别不易得到高分，必须要在此基础上有所创新方得可以避开其他雷同课题，，不会轻易被导师被否决。因此建议在车牌识别基础上加入出入库，判别是否为库内车牌，并且实行计时收费。整个设计在一个GUI界面上完成。
传统基础版：中规中矩的车牌识别
靓点1版本：可做成复杂背景的车牌识别
靓点2版本：可做成具备判断是否为库内车牌的案例，并且计时计费（本课题）
靓点3版本：可做成具备语音播报的车牌识别

二、基本流程
车牌识别部分：

①图像预处理：在整个车牌识别系统中，由于采集进来的图像为真彩图，再加上实际采集环境的影响以及采集硬件等原因，图像质量并不高，其背景和噪声会影响字符的正确分割。和识别，所以在进行车牌分割和识别处理之前，需要先对车牌图像进行图像预处理操作。

②车牌定位：首先对车牌的二值图片进行形态学滤波，使车牌区域形成一个连通区域，然后根据车牌的先验知识对所得到的连通区域进行筛选，获取车牌区域的具体位置，完成从图片中提取车牌的任务。

③车牌分割：首先对车牌进行水平投影，去除水平边框；再对车牌进行垂直投影。通过对车牌进行投影分析可知，与最大值峰中心对应的为车牌中第二个字符和第三个字符的间隔，与第二大峰中心距离对应的即为车牌字符的宽度，并以此为依据对车牌进行分割。 

④字符识别：本文采用模板匹配方法来对车牌进行识别。识别过程中，首先建立标准字库，再将分割所得到的字符进行归一化，将归一化处理后的字符与标准字库里的字符逐一比较，最后把误差最小的字符作为结果显示出来。

出入库部分：

①汽车入库记录北京时间，车库位数减一；
②汽车出库记录北京时间，车库位数加一；
③计算停车时长，按标准计算停车费用；

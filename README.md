## CSC591/ECE 542 - Neural Networks: Proj-C

### Team 117

- Kartik Rawool (khrawool)
- Kartiki Bhandakkar (kbhanda3)
- Subodh Gujar (sgujar)

Final predictions are in the jupyter notebook file.

### Overview

The ability to walk efficiently, safely, and attentively is a natural human trait that is disrupted by lower limb amputations. To restore basic walking function, amputees often rely on prosthetic devices. To improve the comfort and safety of these devices, we seek to create a system that identifies the terrain using data from inertial measurement units (IMUs) in the prosthetic leg. Our prosthetic leg currently uses both visual and inertial sensors. The paper [1] proposed a novel vision-based context prediction framework for lower limb prostheses to simultaneously predict human’s environmental context for multiple forecast windows using Bayesian neural networks. We are exploring the possibility of terrain identification without visual data. By adapting the control of the prosthetic leg to changes in the surrounding terrain, we
can enhance its functionality. The paper [2] investigated the use of machine learning algorithms to automatically identify running surface from wearable motion sensors to quantify running exposures and loading and injury risk for a runner.


### How to run? Steps for running the code:

1. Run all the cells in ```competition_notebook.ipynb``` to up-sample the y data and train Bi-LSTM model and perform the prediction on the test data. After predicting the value downsample the y data to match the frequency of the test data.
2. If you don't want to train the model load the ```bi_lstm_v1.keras``` and run the cells to upsample test data and make the prediction. After predicting the value downsample the y data to match the frequency of the test data.

### Dataset

The training data includes the following 4 classes: (0) indicates standing or walking on solid ground, (1) indicates going down the stairs, (2) indicates going up the stairs, and (3) indicates walking on grass. For different users, multiple sessions were conducted with a start time of 0. We combined all labels for visualization. It can be observed that there is a class imbalance with class 0 having the maximum number of instances. 

### References:
[1] B. Zhong, R. L. d. Silva, M. Li, H. Huang and E. Lobaton, ”Environmental Context Prediction for Lower Limb Prostheses With Uncertainty Quantification,” IEEE Transactions on Automation Science and Engineering, vol. 18, no. 2, pp. 458-470, April 2021, doi: 10.1109/TASE.2020.2993399.


[2] P. C. Dixon, K. H. Sch ̈utte, B. Vanwanseele, J. V. Jacobs, J. T. Dennerlein, J. M. Schiffman, P.-A. Fournier, and B. Hu, “Machine learning algorithms can classify outdoor terrain types during running using accelerometry data,” Gait amp; Posture, vol. 74, pp. 176–181, 2019.


[3] R. Moura Coelho, J. Gouveia, M. A. Botto, H. I. Krebs, and J. Martins, ”Real-time walking gait terrain classification from foot-mounted inertial measurement unit using convolutional long short-term memory neural
network,” Expert Systems with Applications, vol. 203, p. 117306, Oct. 2022.

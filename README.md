to install the bank card detector, you need Python 3.7.7 

> git clone https://github.com/gaoyuanliang/bank_card_detection.git
>
> cd bank_card_detection
>
> pip3 install -r requirements.txt
>
> wget https://github.com/fchollet/deep-learning-models/releases/download/v0.4/xception_weights_tf_dim_ordering_tf_kernels_notop.h5

download the pretrain model of bank card detection from the following url

> https://drive.google.com/file/d/10H70SUi1C5R79cu-27u-bg9ytnZ8JV9F/view?usp=sharing

to use the model to tag the image, we have four cases

**Test case #1**

download the test image by 

> wget https://www.mashreqbank.com/egypt/en/images/Platinum-Credit-Card_tcm74-220679.jpg

the image looks like

![alt text](https://www.mashreqbank.com/egypt/en/images/Platinum-Credit-Card_tcm74-220679.jpg)

run the test code

> from bank_card_detection import bank_card_detection
>
> bank_card_detection('Platinum-Credit-Card_tcm74-220679.jpg')

you will see the following output since the image itself is a credit card

> {'tag': 'bank_card', 'score': 0.9966258}

**Test case #2**

download the test image by 

> wget https://ichef.bbci.co.uk/news/1024/media/images/67649000/jpg/_67649781_160757669.jpg

the image looks like

![alt text](https://ichef.bbci.co.uk/news/1024/media/images/67649000/jpg/_67649781_160757669.jpg)

run the test code

> bank_card_detection('_67649781_160757669.jpg')

you will see the following output since the image itself is a credit card

> {'tag': 'bank_card', 'score': 0.9973912}



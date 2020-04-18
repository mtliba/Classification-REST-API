# Classification-REST-API
simple Keras imagenet classification Flask REST API , VGG , ResNet50 , InceptionV3 , Xception .

* to run : 
assume tenserflow already installed  
requirements :

```shell
$ pip install keras
$ pip install numpy
$ pip install Pillow
$ pip install flask gevent requests
```
* Starting the Keras server
clone this repo and put you image within server file 

start The Flask + Keras server , access the REST API via http://127.0.0.1:5000 : 
```shell
$ python server.py
```
Requests can be submitted via curl or by running simple_request.py , case of using curl response will be json object  :
```shell
$ curl -X POST -F image=@image.jpg 'http://localhost:5000/predict?model=VGG16'
```
specify your image path after image=@ and the name of your desired classifier after ?model= , by running simple_request.py ResNet50 is the defaul model  

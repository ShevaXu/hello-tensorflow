# Hello TensorFlow

Have fun learning [TensorFlow](https://www.tensorflow.org).

## Installation

[Docker installation](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/g3doc/get_started/os_setup.md#docker-installation) is highly recommended for experimental trial:

```
docker pull tensorflow/tensorflow
``` 

It is also on `gcr.io/tensorflow/tensorflow` besides Docker Hub.

## Examples

### Board

This example shows how to run a simple *logistic regression* and visualize it using *TensorBoard*:

```
$ docker run -it -v $PWD:/board -w /board -p 8888:8888 tensorflow/tensorflow bash

root@63410e8c4372:/board# mkdir log && python board.py
...
root@63410e8c4372:/board# tensorboard --logdir log --host 0.0.0.0 --port 8888
Starting TensorBoard 41 on port 8888
(You can navigate to http://172.17.0.2:8888)
```

* `-p` and `--host 0.0.0.0` setting together make *TensorBoard* accessible from host's browser;
* `-v` (optional) maps a volume into the container so that you can modify you script on your host machine with any IDE.

## Refs

* [Python API](https://www.tensorflow.org/api_docs/python/tf/Session) (Stable since 1.0)
* [TensorBoard: Visualizing Learning](https://www.tensorflow.org/get_started/summaries_and_tensorboard)

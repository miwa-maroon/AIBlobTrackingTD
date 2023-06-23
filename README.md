# AIBlobTrackingTD

# LiDAR
YDLiDAR X2
Hokuyo is expensive for me, someone buy me 

# develop process
1. see if the method work with one sample data
2. if so, set label as blobs postions
3. training in colab
4. convert onnx
5. run onnx in touchdesigner

or

1. collect lidar points and blob track chop data
2. train with 2 data above by (tensorflow or pytorch)
3. convert onnx
4. run onnx in touchdesigner

# Methods
### training to make AI model
- data clustering(x, y)
  - K-Means(sk-learn)
  - MiniBatchiKmeans(if i use more data, it's faster than kmeans)
  - Point-Net(Pytorch, tensorflow)
  - Point-Net++(Pytorch, tensorflow)
  - KPConv(Pytorch)
  - PointCNN(Pytorch)
  - VoteNet(Pytorch)
  - PointConv(tensorflow)
- convert to image
  - Histogram-Based Approach with CNN (tensorflow or pytorch)
- object detectin
  - VoteNet(Pytorch, tensorflow)
  - Frustum PointNet(tensorslow)
### run model
- ONNX -> because it's fitted for runtime


# Problems
### How predicted disappared object due to occlusion
- Temporal Analysis(predict by past motion using KalmanFilter)
- Use RNN or LSTM to predict current location by past movement

# result
- data clustering(x, y)
  - K-Means(sk-learn) -> Not good
  - Point-Net(Pytorch, tensorflow) ->
  - Point-Net++(Pytorch, tensorflow) ->
  - KPConv(Pytorch) ->
  - PointCNN(Pytorch) ->
  - VoteNet(Pytorch) ->
  - PointConv(tensorflow) ->
- convert to image
  - Histogram-Based Approach with CNN (tensorflow or pytorch) ->
- object detectin
  - VoteNet(Pytorch, tensorflow) ->
  - Frustum PointNet(tensorslow) ->

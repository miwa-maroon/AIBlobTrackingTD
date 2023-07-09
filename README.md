# AIBlobTrackingTD

# LiDAR
YDLiDAR X2
Hokuyo is expensive for me, someone buy me 

# develop process
1. collect lidar points
2. Create model (PointNet and PointPillar)
3. Train
4. Test
5. Convert onnx


1. collect lidar points and blob track chop data(0.1msec)
2. Create model (LSTM or RNN)
3. train with 2 data above by (tensorflow or pytorch)
4. convert onnx
5. run onnx in touchdesigner

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
  - OpenPCDet(Pytorch)
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

### a few points in the case of long distance
- Data agumentation
- 

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

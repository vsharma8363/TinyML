# Training Basics
- Batch Size - Number of samples to push through at every inference step during training before adjusting model weights
  - Higher Batch Size = Less Accurate Model = Faster Training Time
  - Lower Batch Size = More Accurate Model = Slower Training Time
  
- Train/Validation/Test
  - Train - Training data, usually ~60%
  - Validation - Used to measure performance of model after each training step
  - Test - Used to measure true overall performance of the model

# Model Conversions
- TFLite Converter
  - Converts TF models into special, space-efficient format for use on resource constrained devices
  - Can apply optimization that reduce model size and make it run faster
- TFLite Interpreter
  - Runs converted TFLite mdel using most efficient operations
  
# Model Optimizations
- Quantization
  - By default, weights are stored as 32-bit FP numbers, for high-precision
  - Quantization reduces the precision so they fit into 8-bit integers (4x size reduction)
  - Quantized model runs faster --> CPU does faster math with integers than floats
  - Often has minimal loss in accuracy

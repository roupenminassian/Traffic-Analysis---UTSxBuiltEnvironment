# Traffic Analysis Project

This project provides tools and scripts for analyzing traffic from videos. It uses computer vision techniques and deep learning models to detect vehicles and measure their speeds.

![Description of your GIF](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExcnMxMWg2YmlwbDRmaGw3N3Z3MXJncGpmZGY0YTlrMmxyOHpudHp1diZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/iL0J1oTqMMwjojl1Hx/giphy.gif)

## Features

- **Vehicle Detection**: Identify and classify vehicles in various lanes.
- **Bird's-Eye View Transformation**: Transform the video frame to get a top-down view, making it easier to analyze traffic patterns.
- **Lane Detection**: Automatically detect lanes to segregate vehicles.
- **Speed Measurement**: Calculate the speed of each detected vehicle.
- **Data Aggregation**: Summarize and group detected data for easier analysis.
- **Integration with Transformers Library**: Utilizes pretrained models from Hugging Face's model hub for object detection.

## Prerequisites

Make sure you have the following libraries installed:

```
pip install opencv-python matplotlib transformers timm torch torchvision
```

## Usage

1. **Point Selection**: The script starts by allowing users to select four points on the first frame of the video. These points are used to transform the video frame to get a bird's-eye view.

2. **Frame Processing**: Each frame is then processed to detect vehicles, measure their speeds, and identify the lanes they are in.

3. **Data Aggregation**: After processing all frames, the script aggregates the data to give a summary of the number of vehicles detected for each type and in each lane.

4. **Output**: The final data is presented in a pandas DataFrame format, showing aggregated data for each timestamp, label (vehicle type), and lane.

## Code Structure

1. **Video Loading and Initialization**: Loads the video and initializes necessary parameters.
2. **Mouse Callback for Point Selection**: Allows users to select points on the video frame.
3. **Bird's-Eye View Transformation**: Transforms the video frame to get a top-down view using the selected points.
4. **File Operations**: Includes merging frames from different sources and creating an aggregated dataset.
5. **Annotation Parsing**: Parses annotation files to identify objects in frames.
6. **Model Initialization and Training**: Loads pretrained DETR model, fine-tunes it on the dataset, and pushes it to Hugging Face's model hub.
7. **Object Detection in Video**: Processes each video frame to detect vehicles, measure their speeds, and identify the lanes they are in.
8. **Data Aggregation and Output**: Aggregates the detected data and outputs it in a pandas DataFrame format.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)

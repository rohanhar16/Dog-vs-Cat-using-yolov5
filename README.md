<head>
	<h1>Dog and Cat Recognition using YOLOv5</h1>
</head>
<body>
	<h2>Project Overview</h2>
	<p>This project demonstrates how to train a custom object detection model using YOLOv5 and use it to recognize dogs and cats in images. The dataset used in this project is available in the dataset folder, which contains images of dogs and cats along with their corresponding annotations.</p>
  <h2>Setup</h2>
<p>To get started, clone the YOLOv5 repository by running the following command:</p>
<pre><code>!git clone https://github.com/ultralytics/yolov5.git</code></pre>

<p>Then navigate to the yolov5 directory and install the required packages:</p>
<pre><code>%cd yolov5
!pip install -r requirements.txt</code></pre>

<h2>Data Preparation</h2>
<p>To split the data into training and validation sets, run the data_prep.py script:</p>
<pre><code>python data_prep.py</code></pre>
<p>This script will split the images and their corresponding annotations into training and validation sets and move them to the images/train, labels/train, images/val, and labels/val directories.</p>

<h2>Training</h2>
<p>To train the YOLOv5 model on the dataset, run the following command:</p>
<pre><code>!python train.py --img 398 --batch 10 --epochs</code></pre>
<p>This will start the training process with the specified hyperparameters.</p>

<h2>Inference</h2>
<p>To test the model on new images, run the detect.py script:</p>
<pre><code>!python detect.py --source path/to/image --weights path/to/weights</code></pre>
<p>Replace path/to/image with the path to the image you want to test and path/to/weights with the path to the trained weights. This script will output the image with bounding boxes around the detected dogs and cats.</p>

<h2>Conclusion</h2>
<p>With this project, you have learned how to train a custom object detection model using YOLOv5 and use it to recognize dogs and cats in images. You can use this knowledge to train models for other object detection tasks as well.</p>
</body>

# Qualcomm® CM2290 Open Kits Bert-QA-demo Developer documentation

## Introduce

The project relies on the CM2290 development kit to take advantage of the diversity and powerful computing power of the development kit. Use a TensorFlow Lite model to answer questions based on the content of a given passage.

The CM2290 development board can be used for the development of AI robots. After training the mechanical energy of the model, users can develop robots with natural language dialogue


The project was built on x86 hosts using cross-compiler tools and has been implemented in Qualcomm ® CM2290 open suite

The project was built in x86 host with across complier tool and has been tested in Qualcomm® CM2290 Open Kits.

Qualcomm® CM2290 SoC Open Kits

![CM2290](../res/2290-DK-4-150x150.webp)

## Materials and Tools used for the project

1. Hardware materials

Except for the Open Kits,The following hardware materials are also needed:

* Type-C usb line

using the usb line to develop on Qualcomm® CM2290 SoC Open Kits.

![usb line](../res/usb.png )

* Charger

Direct power supply for Qualcomm® CM2290 SoC Open Kits.

![charger](../res/charger.jpg )


## Environment configuration

This section mainly describes the source and configuration of some open source projects or third-party tools needed in the development process.

### TensorFlow  -BERT Question and Answer

The model can be used to build a system that can answer users’ questions in natural language. It was created using a pre-trained BERT model fine-tuned on SQuAD 1.1 dataset.

BERT, or Bidirectional Encoder Representations from Transformers, is a method of pre-training language representations which obtains state-of-the-art results on a wide array of Natural Language Processing tasks.

This app uses a compressed version of BERT, MobileBERT, that runs 4x faster and has 4x smaller model size.

SQuAD, or Stanford Question Answering Dataset, is a reading comprehension dataset consisting of articles from Wikipedia and a set of question-answer pairs for each article.

The model takes a passage and a question as input, then returns a segment of the passage that most likely answers the question. It requires semi-complex pre-processing including tokenization and post-processing steps that are described in the BERT paper and implemented in the sample app.


## Configure and Usage
Start the CM290 and connection CM290 to host by Type-c usb.
### 1. Configure
In the conf directory, a json configuration file is provided. This configuration file is relatively simple. It mainly configures the gstreamer camera pipeline, gstreamer udpsink push pipeline, and traditional depth estimation algorithm parameters.

### 2. Usage
The executable files in the bin directory do not require additional command line parameters. The parameters used by the program are configured by the json file, so you only need to put the configuration file in the same directory to execute the program.

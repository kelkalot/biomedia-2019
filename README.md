# biomedia-2019
ACM-Grand-Challenge-2019-Biomedia

## What is this task about?

The task differs from existing medical imaging tasks, in that it uses only multimedia data (i.e., images and videos) 
and no medical imaging data (i.e., CT scans). A further innovation is its focuses on two non-functional requirements: 
using as little training data as possible and being computationally effective.

The task focuses on images of the gastrointestinal (GI) tract that were recorded by a special endoscopic device
used during normal colonoscopies. 
The task is to develop approaches that can detect abnormalities and diseases in early stages.

The ultimate goal of the task is not only disease detection, but also perform it in an efficient and fast way and 
the generation of automatic text reports (summaries) of findings in multimedia content. 
The task works together with medical experts, who provide ground truth and help to develop it towards 
addressing the specific challenges of automatic text reports.

This year, participants in this task are offered three subtasks.

1) Detection: Detection of diseases with as few images in the training dataset as possible.

2) Efficient detection: Solve the classification problem in a fast and efficient way.

3) Report generation (Experimental): Automatically create a text-report for a medical doctor for three video cases. 

Participants can participate in as many subtasks they want.
A list of what exactly to submit for evaluation will be released with the test dataset first of June. 

## What data is provided?

The dataset consists of more than 10,000 images, annotated and
verified by medical doctors (experienced endoscopists), including
16 classes showing anatomical landmarks, phatological findings or
endoscopic procedures in the GI tract with different number of images per each class, 
split into training and testing sets. The anatomical landmarks are
Z-line, pylorus and cecum, while the pathological finding includes
esophagitis, polyps and ulcerative colitis. In addition, we provide
two set of images related to removal of polyps, the "dyed and lifted
polyp" and the "dyed resection margins", as well as some more classes related to the GI tract endoscopic procedures.
The classes provided are:
* blurry-nothing
* colon-clear
* dyed-lifted-polyps
* dyed-resection-margins
* esophagitis
* instruments
* normal-cecum
* normal-pylorus
* normal-z-line
* out-of-patient
* polyps
* retroflex-rectum
* retroflex-stomach
* stool-inclusions
* stool-plenty
* ulcerative-colitis

The dataset consist of
images with different resolutions from 720x576 up to 1920x1072
pixels and organized in a way where they are sorted in separate
folders named accordingly to the content. Some of the included
images have a green sub-picture in the image illustrating the
position and configuration of the endoscope inside the bowel, by
the use of an electromagnetic imaging system (ScopeGuide, Olympus
Europe). This sub-picture may support the interpretation of the image.

As mentioned before, the whole dataset is split onto two equally sized development and test datasets.
Pre-extracted features for all data (visual) will also be provided.
The ground truth for the data is collected from medical expert annotations (GI endoscopists).

Download details for the development dataset Kvasir: A Multi-Class Image Dataset for Computer Aided Gastrointestinal Disease Detection can be found here: https://github.com/biomedia-2019/wiki/Data-Release

For the automatic report generation we will use three videos depicting diseases or findings that can be found in the 
Kvasir dataset. 
The goal is to generate reports describing the three videos for medical experts with having a automatic report generation in mind. 
The evaluation of the reports will be done by three medical doctors.
The videos for the evaluation and the exact evaluation criterias will be provided first of June.


## How is the performance measured?

For the evaluation of detection we use the standard metrics:

* **True positive (TP)**<br>The number of correctly identified samples. The number of frames with an endoscopic finding which correctly is identified as a frame with an endoscopic finding.
* **True negative (TN)**<br>The number of correctly identified negative samples, i.e., frames without an endoscopic finding which correctly is identified as a frame without an endoscopic finding.
* **False positive (FP)**<br>The number of wrongly identified samples, i.e., a commonly called a "false alarm". Frames without an endoscopic finding which is erroneously identified as a frame with an endoscopic finding.
* **False negative (FN)**<br>The number of wrongly identified negative samples. Frames without an endoscopic finding which erroneously is identified as a frame with an endoscopic finding.
* **Recall (REC)**<br>This metric is also frequently called sensitivity, probability of detection and true positive rate, and it is the ratio of samples that are correctly identified as positive among all existing positive samples.
* **Precision (PREC)**<br>This metric is also frequently called the positive predictive value, and shows the ratio of samples that are correctly identified as positive among the returned samples (the fraction of retrieved samples that are relevant).
* **Specificity (SPEC)**<br>This metric is frequently called the true negative rate, and shows the ratio of negatives that are correctly identified as such (e.g., the fraction of frames without an endoscopic finding are correctly identified as a negative result).
* **Accuracy (ACC)**<br>The percentage of correctly identified true and false samples.
* **Matthews correlation coefficient (MCC)**<br>MCC takes into account true and false positives and negatives, and is a balanced measure even if the classes are of very different sizes.
* **F1 score (F1)**<br>A measure of a test’s accuracy by calculating the harmonic mean of the precision and recall.

We will also evaluate how much training data has been used to achieve good results.

For the evaluation of the processing time the organizers will run the code provided by the participants on the same 
hardware and measure the time from input to output weighted by accuracy of the output. 
Details about the hardware will be provided to the participants before submitting their code 
(it will be a multi-core system with CUDA support).

The automatic generated report will be assessed manually from three of our medical partners in terms of how 
useful it is for them and if it satisfies existing demands for documentation of endoscopic procedures. 
The assessment will follow a list of requirements that will be provided to the participants.


## Who are the task organizers?
* Pål Halvorsen, paalh@simula.no, Simula Research Laboratory
* Michael Riegler, michael@simula.no, SimulaMet & University of Oslo
* Andreas Petlund, andreas@augeremedical.com, Augere Medical
* MD Pia Smedsrud, pia@simula.no, Augere Medical, Simula Research Laboratory
* MD Thomas de Lange, t.d.lange@medisin.uio.no, Oslo University Hospital
* MD Kristin Ranheim Randel, Kristin.Ranheim.Randel@kreftregisteret.no, Cancer Registry of Norway
* MD Peter Thelin Smidt, peter.thelin-schmidt@sll.se, Karolinska Hospital
* Trine B. Haugen, tribha@oslomet.no, Oslo Metropolitan University
* Mathias Lux, mlux@itec.aau.at, Alpen-Adria-Universität Klagenfurt
* Duc-Tien Dang-Nguyen, uctien.dangnguyen@uib.no, University of Bergen


## Where to get more information?
Detailed information on the task including description of the data, provided features, run submission, etc. 
can be found on the task wiki: https://github.com/biomedia-2019/wiki

If you need help or have any questions please contact Pål Halvorsen or Michael Riegler.

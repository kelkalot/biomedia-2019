# The Biomedia ACM MM Grand Challenge 2019
A Multimedia in Medicine Grand Challenge

![Simula logo](simula_logo_main.png) 

![Augere logo](Augere_logo-noncentered.png)

## What is this challenge about?

The Biomedia Grand Challenge focuses on the emerging field of medical multimedia.
In the field of multimedia, a trend towards medical applications can be observed. This fact is underlined by several newly emerging medical related workshops and special session in multimedia related conferences like MEDICO (http://www.multimediaeval.org/mediaeval2018/medico/) and MMHEALTH (https://mmhealth.uni-oldenburg.de). Nevertheless, even with these initiatives it seems there is still a long way to establish medical multimedia as a mainstream field within the multimedia community.

With this challenge, we hope to encourage the multimedia community to help improve the health care system. 

Through application of their knowledge and methods we can reach the next level of detection and interpretation of abnormalities, giving better computer and multimedia assisted diagnosis systems. In previous research in this area, computer vision and medical imaging have created visual augmentations of both the interior and exterior of the human body, such as AI for detecting skin cancer. To automatically detect and locate abnormalities, visual representations are not sufficient. There is a need for image and video processing, analysis, information search and retrieval, in combination with other sensor data and assistance from medical experts, and it all needs integration and efficient processing. Tackling the challenge can for example be addressed by leveraging techniques from multiple multimedia-related disciplines, including methods such as machine learning (classification), multimedia content analysis and multimodal fusion. 

This year the challenge will focus on the *gastrointestinal (GI) tract* with an aim to detect and classify abnormalities. 
Medical domain experts are included in the organization and evaluation of the results. 
As industry partner this year we include Augere Medical in the organization, who develops an automated screening and CAD system for GI tract examinations. Medical and industry experts will also be present at the ACM MM conference to provide direct feedback and possibilities to interact with researchers directly.

It is a typical assumption that visual analysis, as it is already provided by the computer vision and medical image processing communities today, is capable of already providing viable and practical approaches to healthcare multimedia challenges. Although we concede that these methods are indeed essential contributors to promising approaches, we realize the limitations of analysing images and videos alone in medical fields such as endoscopy, ultrasound, etc., because of the complexity and needs of medical experts and patients. Neither does it make enough use of the multitude of additional information sources including sensors and temporal information.

The challenge can be seen as very challenging and hard to solve and evaluate. Due to its novel use case, we hope to motivate a lot of researchers to have a look into the field of medical multimedia. Performing research that can have societal impact will be an important part of multimedia research in the future. We hope that the challenge can help to raise awareness of the topic, and also provide interesting and meaningful use cases to researchers.


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

Download details for the development dataset Kvasir: A Multi-Class Image Dataset for Computer Aided Gastrointestinal Disease Detection can be found here: https://github.com/kelkalot/biomedia-2019/wiki/Data-Release

For the automatic report generation we will use videos depicting diseases or findings that can be found in the 
Kvasir dataset. The goal is to generate reports describing the videos for medical experts with having an automatic report generation in mind. The evaluation of the reports will be done by three medical doctors.
The videos for the evaluation and the exact evaluation criterias will be provided via https://www.dropbox.com/sh/1bkopp53k01fc1i/AAB5-gdjpGrPjFbbSGEmUgfsa?dl=0


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

For the evaluation of the processing time the organizers will run the code provided by the participants on the same 
hardware and measure the time from input to output weighted by accuracy of the output. 
Details about the hardware will be provided to the participants before submitting their code 
(it will be a multi-core system with CUDA support).

The automatic generated report will be assessed manually from three of our medical partners in terms of how 
useful it is for them and if it satisfies existing demands for documentation of endoscopic procedures. 
The report will be evaluated based on usefulness, correctness and innovation.

## Prizes
Augere Medical AS rewards the best contributions with prizes of a total of $2,000 USD distributed over the winners. The number of winners will depend on the number of participants and the quality of the results. The organizers reserve the complete right in the final judgement and decision.

The winners of the challenge are required to provide a technique report describing the details of the winning algorithms, and provide the source code to the organizers. The organizers will also run the released the code to test the reproducibility of the winner algorithms. The winners will give a presentation during the conference.

## Who are the task organizers?
* Pål Halvorsen, paalh@simula.no, SimulaMet
* Michael Riegler, michael@simula.no, SimulaMet & University of Oslo
* Håkon Kvale Stensland, haakonks@simula.no, Simula & University of Oslo
* Andreas Petlund, andreas@augeremedical.com, Augere Medical
* MD Pia Smedsrud, pia@simula.no, Augere Medical, Simula Research Laboratory
* MD Thomas de Lange, t.d.lange@medisin.uio.no, Oslo University Hospital
* MD Kristin Ranheim Randel, Kristin.Ranheim.Randel@kreftregisteret.no, Cancer Registry of Norway
* MD Peter Thelin Smidt, peter.thelin-schmidt@sll.se, Karolinska Hospital
* Trine B. Haugen, tribha@oslomet.no, Oslo Metropolitan University
* Mathias Lux, mlux@itec.aau.at, Alpen-Adria-Universität Klagenfurt
* Duc-Tien Dang-Nguyen, uctien.dangnguyen@uib.no, University of Bergen


## Where to get more information?
Detailed information on the task including description of the data, provided features, submission, etc. 
can be found on the task wiki: https://github.com/kelkalot/biomedia-2019/wiki

If you need help or have any questions please contact Pål Halvorsen or Michael Riegler. Please mark the email with *ACM Grand Challenge Biomedia-2019*.

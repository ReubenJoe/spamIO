# spamIO: A Text and Image-Based Spam Classifier
<div id="top"></div>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

This work explores deep learning techniques in order to facilitate the detection of text-based and image-based spam.

## Table of contents
<ol>
  <li>
    <a href="#project-description">Project Description</a>
  </li>

  <li>
    <a href="#dataset-description">Dataset Description</a>
  </li>
  <li>
    <a href="#project-structure">Project Structure</a>
  </li>
  <li>
    <a href="#getting-started">Getting Started</a>
    <ul>
      <li><a href="#prerequisites">Prerequisites</a></li>
      <li><a href="#installation">Installation</a></li>
    </ul>
  </li>
  <li>
    <a href="#results">Results</a>
  </li>
   <li>
    <a href="#contributions">Contributions</a>
  </li>
   <li>
    <a href="#contact">Contact</a>
  </li>
</ol>
<p align="right">(<a href="#top">back to top</a>)</p>

## Project Description
With the rapid development of internet, there are several loopholes that are created in cyberspace and is under constant threat from being exploited by hackers. Growing internet and the increasing importance of emails in our daily lives, spams have become a common phenomenon posing serious threats, as it gives rise to undesired emails. One of the most common threats is that of spam. Hackers and spammers are using innovative and novel techniques to deceive both novice and experienced internet users. Spam consumes vital computation power and resources. Thereby, it becomes important to filter out the spam contents. Nowadays, spam is transmitted via different medium such as images, sms etc. Both the text and image spam messages are developed in such a manner that it surpasses through the traditional spam filters and firewall technologies. In our work, we would be developing frameworks for classifying both text as well image contents for spam and ham. We have followed a novel implementation strategy for text spam and image spam classifier model where we attempted to cover the loopholes in the existing techniques and present our approach. Also, we have used spam score as the metric for adjudging a give message or an image as spam or ham. On comparing our approach with several classical models, it could be inferred that our model performs significantly better.
<p align="right">(<a href="#top">back to top</a>)</p>

## Dataset Description
<b>[Email Spam Dataset](https://www.kaggle.com/datasets/nitishabharathi/email-spam-dataset)</b><br/>
The email spam dataset is taken from Kaggle. The dataset has 5572 rows and 2 features.
These two features are:
<ul><li>Message – It consists of the email message</li>
<li>Category – It classifies whether the email message is spam/ham.</li></ul>
<p>Out of the 5572 email messages, 4825 messages were of category ‘ham’ (constituted approximately 86.6% of total messages) and 747 messages were of category ‘ham’ (constituted approximately 13.4% of total messages).

<b>[ISH Dataset](https://users.cs.northwestern.edu/~yga751/ML/ISH.htm#dataset)</b><br/>
This dataset contains both spam and ham images in JPEG format which are collected from original emails. It is a publicly available dataset that can be found in the Northwestern University website. There are 810 ham and 929 spam images in total. The number of unique spam and ham images is 879 and 810 respectively.

<b>[Dredze Dataset](https://www.cs.jhu.edu/~mdredze/datasets/image_spam/)</b><br/>
This dataset contains 3 sets of images. Personal Ham (PHam) has 2,021 images in which there are 1,517 unique images. Personal Spam (PSpam) has 3,298 images in which there are 1,274 unique images. Finally, the Spam Archive (SpamArch) has 16,028 files of various formats like JPEG, PNG, GIF, etc. in which there are 3,039 unique images.


<p align="right">(<a href="#top">back to top</a>)</p>

## Project Structure
    spamIO
    .
    │
    ├── Image_Feature_spam.ipynb
    ├── Text_Based_Spam.ipynb
    ├── .ipynb_checkpoints/
<p align="right">(<a href="#top">back to top</a>)</p>

## Getting Started
Follow these instructions to setup the project.

### Prerequisites
Project is created using:
* Jupyter Notebook
* Python version: 3.9.0
* Tensorflow version: 2.8.0
* Keras version: 2.8.0
* Numpy version: 1.22.3
* Pandas version: 1.2.4
* Matplotlib version: 3.4.1
* MissingNo: 0.5.0
* Seaborn: 0.11.2
* Sklearn
<p align="right">(<a href="#top">back to top</a>)</p>

### Installation
1. Create a virtual environment in conda prompt using the following commands:
    * Make a virtual environment
 
      ```$ conda create -n [ENV_NAME] python=[PYTHON_VERSION]```
      <br>
      where ``ENV_NAME`` is the name of the virtual environment and ``PYTHON_VERSION`` is the version of python.
      
    * Activate the virtual environment
    
      ```$ conda activate [ENV_NAME]```
   
2. Add the virtual environment in the jupyter notebook using the following commands:
    * Install the ipykernel
    ```$ pip install --user ipykernel```

    * Manually add the kernel
    ```$ python -m ipykernel install --user --name=[ENV_NAME]```
    where ``ENV_NAME`` is the name of the virtual environment.
    
3. Clone the project repo into the virtual environment
   
   ```$ git clone https://github.com/ReubenJoe/spamIO.git```
   
4. Download the required datasets from the links provided in the <a href="#dataset-description">Dataset Description</a>.
5. Place the dataset ``.csv`` file in the same level as that of the  ``.ipynb`` file (as shown in the project structure).
6. Execute the file using the following commands:

    ```$ ipython --TerminalIPythonApp.file_to_run='Image_Feature_spam.ipynb'```<br>
    ```$ ipython --TerminalIPythonApp.file_to_run='Text_Based_Spam.ipynb'```
<p align="right">(<a href="#top">back to top</a>)</p>

## Implementation Screenshots
### Input for Text Spam
<img width="700" alt="image" src="https://user-images.githubusercontent.com/92254224/173565015-001bbdca-f1d6-4bd2-a8e2-990999716de8.png">

### Input for Image Spam
<img width="700" alt="image" src="https://user-images.githubusercontent.com/92254224/173565062-b1966f6c-6c69-45f6-b550-d6492aa68490.png">

### Text Spam Detection
<img width="700" alt="image" src="https://user-images.githubusercontent.com/92254224/173565083-81c26ced-1f46-49d6-aa9f-26c3878145dc.png">

### Image Spam Detection
<img width="700" height="500" alt="image" src="https://user-images.githubusercontent.com/92254224/173565204-ff29aa3a-49ad-4d8a-88d0-9a5eab5d210f.png">

### Image Ham Detection
<img width="700" height="600" alt="image" src="https://user-images.githubusercontent.com/92254224/173565275-89744b86-a082-4c5e-ac52-4f8ce833b26b.png">

<p align="right">(<a href="#top">back to top</a>)</p>

## Results
Upon implementing various approaches for text classification such as Naïve Bayes, SVM, LSTM, we observed that SVM (linear kernel) had the highest accuracy of 99.15% after fixing the class imbalance. It is followed by the baseline approaches where the class imbalance with SVM is not considered thereby giving an accuracy of 99.10% followed by LSTM and Naïve Bayes respectively. The results can be observed in the table below.

| Model | Accuracy (%)     |
| :-------- | :------- |
| **SVM (fixing class imbalance)** | **`99.15`** |
| SVM (without fixing class imbalance) | `99.10` |
| CNN | `98.35` |
| Naïve Bayes | `97.27` |
| LSTM | `94.33` |
| BPNN | `97.27` |

Upon implementing various approaches for image classification such as CNN, DNN, we observed that CNN outperformed DNN by having an accuracy of 97.54 as compared to DNN which had an accuracy of 95.34. The results could be observed from the following table.

| Model | Accuracy (%)    |
| :-------- | :------- |
| **CNN** | **`97.54`** |
| DNN | `95.34` |
<p align="right">(<a href="#top">back to top</a>)</p>

## Contributions
Contributions are what make open source such a fantastic environment to learn, inspire, and create. Any contribution you could provide to this existing work is much appreciated.
Please fork the repository or create a pull request if you have any suggestion for betterment. Subsequently, you could also open an issue for queries. Also, Don't forget to give the project a star!
<p align="right">(<a href="#top">back to top</a>)</p>

## Contact
&nbsp;<a href="mailto:reubenvarghesejoseph@gmail.com"><img src="https://cdn-icons-png.flaticon.com/512/5968/5968534.png" width="30px"></a>
&nbsp;&nbsp;<a href="https://github.com/ReubenJoe"><img src="https://cdn-icons-png.flaticon.com/512/733/733553.png" width="30px"></a>
&nbsp;&nbsp;<a href="https://www.linkedin.com/in/reuben-joseph-88981a21a/"><img src="https://cdn-icons.flaticon.com/png/512/3536/premium/3536505.png?token=exp=1655205000~hmac=14d969e01bdd5560e5cbb315a57e2da2" width="30px"></a>
<p align="right">(<a href="#top">back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/ReubenJoe/spamIO.svg?style=for-the-badge
[contributors-url]: https://github.com/ReubenJoe/spamIO/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ReubenJoe/spamIO.svg?style=for-the-badge
[forks-url]: https://github.com/ReubenJoe/spamIO/network/members
[stars-shield]: https://img.shields.io/github/stars/ReubenJoe/spamIO.svg?style=for-the-badge
[stars-url]: https://github.com/ReubenJoe/spamIO/stargazers
[issues-shield]: https://img.shields.io/github/issues/ReubenJoe/spamIO.svg?style=for-the-badge
[issues-url]: https://github.com/ReubenJoe/spamIO/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/reuben-joseph-88981a21a/

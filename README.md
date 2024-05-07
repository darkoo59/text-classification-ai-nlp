<h1 align="center" id="title">AI text classification (xlm-roberta-base and bert-base-uncased models) 🤖</h1>




<a name="readme-top"></a>
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
<h3 align="center">TripAdvisor Reviews AI/NLP Classification</h3>

  <p align="center">
    <br />
    <a href="https://github.com/darkoo59/text-classification-ai-nlp/issues">Report Bug</a>
    ·
    <a href="https://github.com/darkoo59/text-classification-ai-nlp/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#credits">Credits</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->

## About The Project

<a name="#about-the-project"></a>

This project aims to analyze hotel reviews from TripAdvisor using natural language processing (NLP) techniques. The main objectives include sentiment analysis, rating prediction, and classification of review sentiments into predefined categories.

<h2><b>Features</b></h2>
While we continue to refine and expand our offerings, you can expect the following features:

<ul>
    <li>
        <strong>Data Loading:</strong> Load TripAdvisor hotel reviews dataset from a CSV file.
    </li>
    <li>
        <strong>Data Preprocessing:</strong> Preprocess the reviews by balancing classes, tokenizing, and encoding.
    </li>
<li>
<strong>Model Training:</strong> Train a sequence classification model using the preprocessed data.
</li>
    <li>
        <strong>Evaluation:</strong> Evaluate the trained model on test data using accuracy and mean absolute error (MAE) metrics.
    </li>
      <li>
        <strong>Prediction:</strong> Predict review ratings for new input texts.
    </li>
      <li>
        <strong>Documentation:</strong> Provide comprehensive documentation for understanding and replicating the project.
    </li>
</ul>

<h2><b>Get In Touch</b></h2>
<a name="#built-with"></a>
If you have any questions about the project or suggestions for improvement, don't hesitate to reach out to the author (Darko Selaković) directly. Your feedback is invaluable to me.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

<a name="#built-with"></a>

* [![Python]][Python-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->

## Getting Started

To get a local copy up and running follow these simple example steps.

### Prerequisites

  1. pandas: Data manipulation library for data loading and preprocessing.
  2. numpy: Numerical computing library for array operations.
  3. scikit-learn: Machine learning library for evaluation metrics such as accuracy and MAE.
  4. transformers: Library for using pre-trained NLP models and tokenization.
  5. torch: Deep learning framework for model training and evaluation.

### Installation

1. Contact owner for more info
2. Clone the repo
   ```sh
   git clone https://github.com/darkoo59/text-classification-ai.git
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Credits

<a name="#credits"></a>

1. Dataset: The TripAdvisor hotel reviews dataset used in this project is sourced from <a href="https://www.kaggle.com/datasets/andrewmvd/trip-advisor-hotel-reviews">Kaggle</a>. The dataset used for training and validation consists of 20,493 rows and 2 columns (Review and Rating). Approximately 2,000 rows were utilized for training, aiming for optimal execution time during testing. Subsequently, the success rates were calculated based on 50 new rows from the dataset.
2. Transformer Models: Pre-trained transformer models (e.g., BERT, XLM-RoBERTa) are sourced from the Hugging Face model hub.


<!-- USAGE EXAMPLES -->

### Implementation

Implementation of both models are in files here in repository.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

See the [open issues](https://github.com/darkoo59/university-simulation/issues) for a full list of proposed features (and
known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## New knowledge about the topic


  - After conducting my research, I have come to the realization that multi-class classification, particularly in my case where I classify comments into five classes (rating 1 - negative, rating 2 - below average, rating 3 - average, rating 4 - above average, rating 5 - positive), is not significantly more complex than binary classification. It mostly involves adjusting the model parameters differently. However, the training time is indeed longer. Additionally, it is worth mentioning that the model cannot be completely certain whether a comment is below average, average, or above average because it is ultimately a subjective assessment. However, the model performs exceptionally well in identifying positive and negative comments. Furthermore, models would achieve even better results if trained on a larger dataset.

  - Both scripts involve defining and tuning model parameters such as number of epochs, batch size, evaluation strategy, and model saving strategy. However, the parameters might vary slightly between different models, requiring careful adjustment to achieve optimal performance.While both projects rely on similar metrics for evaluating model performance, such as accuracy and mean absolute error (MAE), there might be differences in how those metrics are used or interpreted, especially if the models are tailored to specific tasks or datasets. While the steps for tuning the model and evaluating performance are similar, it may be necessary to tailor those steps to the specifics of each model. For example, adjusting the number of epochs or batch size may have a greater impact on one model compared to another. After testing the models, interpreting the results may differ due to differences in model characteristics and performance. For example, one model may excel at identifying positive comments, while another may perform better at distinguishing between different shades of negative or average comments and this is directly related to how you setup parameters of each model.

  - Testing time on the same data with similar configurations for two different models can vary based on various factors such as model architecture, complexity, and computational resources. In our case, testing time is nearly 3 times longer for the RoBERTa model compared to the other model. This longer testing time for the RoBERTa model could be attributed to several reasons. RoBERTa is a larger model compared to the other model. Larger models often require more computational resources and time for processing due to the increased number of parameters and computations involved in inference. The RoBERTa model may require more memory and computational resources during inference, leading to longer testing times, especially if the available resources are limited or if the model is running on hardware with lower specifications. The level of optimization and implementation efficiency can also affect testing time. If one model is optimized more effectively or implemented with more efficient algorithms, it may have shorter testing times compared to less optimized models.

  - The findings suggest that the models can deliver highly accurate results, particularly in identifying positive and negative comments. However, it's noteworthy that categorizing comments as "average," "below," or "above" average may depend on the subjective perception of the user at that moment. In essence, while the models excel at recognizing the extremes of sentiment, such as strongly positive or negative comments, the nuanced distinctions between average, below, or above-average sentiments are inherently subjective and context-dependent. Therefore, while the models can provide valuable insights into sentiment analysis, it's important to acknowledge the limitations and subjectivity inherent in interpreting and categorizing sentiment in text data.

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any
contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request.
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTACT -->

## Contact

Darko Selaković - darko.selakovic11@gmail.com


<p align="right">(<a href="#readme-top">back to top</a>)</p>





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-url]: https://github.com/darkoo59/instagram-analytics/graphs/contributors

[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge

[forks-url]: https://github.com/darkoo59/instagram-analytics/network/members

[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge

[stars-url]: https://github.com/darkoo59/instagram-analytics/stargazers

[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge

[issues-url]: https://github.com/darkoo59/instagram-analytics/issues

[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555

[linkedin-url]: [https://linkedin.com/in/othneildrew](https://www.linkedin.com/in/darko-selakovic-370792250/)

[Python]: https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54

[Python-url]: https://www.python.org/

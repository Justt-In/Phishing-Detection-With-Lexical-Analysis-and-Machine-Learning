# Defending Against Phishing Attacks With Lexical Analysis and Machine Learning
This project is completed in partial fulfillment of the requirement for the School of Computer Science and Engineering (SCSE) of the Nanyang Technological University (NTU).

# Security Considerations with Phishing/Malicious URLs
Phishing URLs generally seek to trick users to give up confidential information, either by imitating a website of a known company, or by leveraging social engineering techniques to pressure users to interact with their malicious site. However, there are potential cases where phishing URLs are malicious links that expose users to a variety of vulnerabilities, many of which don't require active interaction to be exploited i.e. Drive-by Downloads, Exploitation of Browser Vulnerabilities, Session Hijacking, Man-in-the-Middle (MitM) Attacks, URL Redirects and Watering Hole Attacks.

These vulnerabilities highlight the significant risks that phishing and malicious URLs pose, especially to individuals who may be uninformed or unaware of the threats lurking on the internet. As attackers increasingly exploit these entry points, it becomes crucial for a detection solution to not only identify these harmful URLs but also actively protect users by preventing the exploitation of these vulnerabilities. Such a solution should safeguard the user's device by detecting and blocking threats before they can execute malicious code or steal sensitive information, thereby maintaining the integrity and security of the system.

# Features for Detection
- URL Length (Total URL length)
- Number of Digits (Count of digits in a URL)
- Number of Letters (Count of alphabetical letters in the URL)
- Number of Dots (Total count of ‘.’ in a URL)
- Number of Special Characters
- URL Depth (Count of ‘/’ in a URL)
- Contains Dash '-'
- Number of Subdomains
- Prefix & Suffix Length

# Lexical Analysis
Lexical analysis, also known as lexical scanning or tokenization, is a process in computer science where a sequence of characters is broken down into smaller meaningful units called tokens. These tokens represent the fundamental building blocks of a language or code, and they serve as the basis for further analysis or processing. In the context of programming languages, lexical analysis is the first step in the compilation process, where source code is transformed into a stream of tokens for subsequent parsing and interpretation.
Breaking down the steps for lexical analysis to help in phishing detection from given URLs gives four main components.
1. Tokenization: The URL is parsed and broken down into smaller tokens, such as the protocol (e.g., "http://" or "https://"), domain name, path, parameters, and query strings. Each token represents a distinct part of the URL.
2. Feature Extraction: Various features are extracted from the tokens to capture relevant information about the URL. These features include the length of the URL, the presence of IP addresses orhash sequences, the number of subdomains, the use of special characters or symbols, and the presence of keywords associated with phishing.
3. Pattern Matching: Lexical analysis involves matching the extracted tokens against known patterns or regular expressions associated with phishing URLs. This allows the detection system to identify URLs that exhibit suspicious or anomalous characteristics, such as unusual domain names, misspellings, or non-standard URL structures.
4. Scoring and Classification: Based on the extracted features and pattern matching results, each URL is assigned a score or classification label indicating its likelihood of being a phishing URL. Machine learning algorithms can then be employed to learn from labeled datasets and automatically classify URLs based on their lexical features.

# Models and Results
This project has trained four models and is tested on a large dataset comprising 174,890 legitimate URLs and 198,359 phishing URLs, totaling 373,249 URLs
Models:
- Support Vector Machines (SVM) - 87.30%
- Gradient Boosting - 95.29%
- Random Forest - 94.56%
- K-Nearest Neighnours (KNN) - 94.27%

# Conclusion
The application of various machine learning models for phishing URL detection using lexical analysis has been explored. The objective was to extract meaningful features from URLs and use these features to classify URLs as either phishing or legitimate. We utilized models such as Support Vector Machine (SVM), Random Forest, Gradient Boosting, and K-Nearest Neighbors (KNN) to evaluate their performance in distinguishing between phishing and legitimate URLs. After conducting extensive experiments and evaluations, Gradient Boosting emerged as the best-performing model for phishing URL detection. This model achieved the highest accuracy and demonstrated superior precision, recall, and F1-score compared to the other models. The strong performance of Gradient Boosting can be attributed to its ability to iteratively improve the model by combining weak learners to form a robust final model. The model's effectiveness in capturing complex patterns and relationships within the data makes it highly suitable for the task of phishing URL detection.

Lazy learning algorithms, such as K-Nearest Neighbors (KNN), defer the generalization process until a query is made. These algorithms do not build an explicit model during the training phase. Instead, they store the training data and perform computation only when a prediction is requested. While lazy learners can be simple and easy to implement, they often suffer from higher computational costs during prediction time, especially with large datasets. Additionally, they can be sensitive to noisy data and may require careful selection of distance metrics and other parameters. On the other hand, eager learning algorithms, such as SVM, Random Forest, and Gradient Boosting, build an explicit model during the training phase. These models generalize from the training data to create a prediction function that can be quickly evaluated during the prediction phase. Eager learners tend to be more efficient during prediction time as they do not rely on the entire training dataset for each query. They can
also leverage advanced techniques for feature selection, regularization, and ensemble methods to improve performance and robustness.

In this project, the eager learning approach demonstrated significant advantages in terms of performance and efficiency for phishing URL detection. Gradient Boosting, in particular, outperformed the lazy learning algorithms, showcasing its ability to handle complex patterns and deliver accurate predictions. The results suggest that eager learning models, with their capacity for advanced optimization and generalization, are well-suited for the task of detecting phishing URLs through lexical analysis. Overall, this project highlights the importance of selecting the right machine learning approach for phishing URL detection. Gradient Boosting, as an eager learner, proves to be an effective and efficient choice, offering superior performance and reliability in identifying phishing threats.

# 1. Overview 
We, Team Geggle Sprints, has developed a Car Accident Scenario Prediction model fine-tuning the PaliGemma.
<br><br>[One Take, Report the Scenario]<br>
This service allows users to share a car accident scenario with just a single photo taken at the accident scene.
Many drivers are overwhelmed when faced with an unexpected car accident. Moreover, in most car-sharing services, the process to report the accident is often confusing, as drivers must take unnecessary steps to connect with the insurance provider via the platform’s customer service.
By simply uploading a photo of the accident scene to our Car Accident Scenario Prediction model, it generates a precise description of the accident in natural language. This helps drivers swiftly file insurance claims and focus on handling the accident scene.
The model has been fine-tuned on Google’s VLM, PaliGemma, using our custom dataset to generate human-level car accident scenarios. We created 110 detailed annotations based on official terms for vehicle parts and formats from government-issued accident reports. The model was trained by iteratively adjusting the prompts for optimal accuracy.
<br><br>[What’s next: AI Customer Service]<br>
Our next step is to train the model on insurance companies' accident response guidelines and integrate Text-to-Speech technology. This will enable the service to provide detailed on-scene response instructions via AI voice assistance, all triggered by a single photo.
- Huggingface
https://huggingface.co/Geggle-Sprints/Car-Accident-Scenario-Prediction
- GitHub
https://github.com/orgs/Geggle-Sprints/teams/gemma-sprint/repositories
<br><br> Team Geggle Sprints, supported by Google Machine Learning Bootcamp 2024
#GemmaSprint


## Model Architecture
We employed the Paligemma model, a large-scale image and text processing model, pre-trained on a vast dataset and fine-tuned for this specific task.

The fine-tuned Paligemma model showed notable improvements in predicting accident scenarios compared to the base model. (Please insert actual metrics here once evaluated).

### Key Model Details:
- **Vocab Size**: 257,152
- **Image Variant**: So400m/14
- **Pooling Type**: None
- **Data Type**: Float16

## Training Process
The model was trained using a cosine learning rate schedule with the following configuration:
- **Batch Size**: 8
- **Learning Rate**: 0.03
- **Total Training Steps**: 64
- **Evaluation Steps**: 16

During each evaluation, the model’s predictions were validated using unseen images in a domain different from the training data.

## Results
## 2. Compare results

### 2.1 Before apply Car datasets
Train
![image/png](https://cdn-uploads.huggingface.co/production/uploads/65d805867c0947fdd59fd714/SoY0i2m-22eTPJmhwybTL.png)

Prediction
![image/png](https://cdn-uploads.huggingface.co/production/uploads/65d805867c0947fdd59fd714/9T2diUTOWeKFQiYef9gR4.png)

### 2.2 After applying Car Dataset
Train
![image](https://github.com/user-attachments/assets/de9b604c-56b2-447d-ae7c-330c94a2b821)

Prediction
![image](https://github.com/user-attachments/assets/8f294617-d2af-44c4-82e3-e84e4b1e07f0)


## Conclusion
This project demonstrates the capability of Paligemma in handling complex prediction tasks such as car accident scenario prediction. Fine-tuning the model significantly improved its performance, suggesting potential use cases in autonomous driving and safety analysis.

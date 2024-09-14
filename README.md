# 🦙🚀 Fine-Tuning LLaMA-Factory with Math Dataset

Welcome to this **LLaMA-Factory fine-tuning project**! In this guide, we’ll walk you through setting up and fine-tuning the `Gemma-2-2B-Chat` model using the **Math Word Problems 200k** dataset from Hugging Face. By the end, you'll see how fine-tuning impacts performance with a **before and after comparison**! 🌟

---

## 🚀 Project Overview

This project demonstrates how to:
- 🛠️ **Fine-tune the `Gemma-2-2B-Chat` model** on a math word problems dataset.
- 🎛️ **Visualize the fine-tuning process** using Gradio's interactive UI.
- 📊 **Evaluate the model's performance** before and after fine-tuning.

> **Model Used**: [Gemma-2-2B-Chat](https://huggingface.co/models)
>
> **Dataset**: [Math Word Problems 200k](https://huggingface.co/datasets/microsoft/orca-math-word-problems-200k?row=12)

---

## 🔑 Setup Instructions

### 1️⃣ **Get Your Hugging Face Token**:
- Head over to [Hugging Face](https://huggingface.co/settings/tokens), generate your token, and store it in the **keys section** of your Google Colab environment.

---

## 🌟 Results

### 📐 Fine-tuning vs. Original Model

Here’s a comparison of **model responses** before and after fine-tuning with a real example. It demonstrates how the fine-tuning process enhances the model’s ability to handle specific mathematical word problems.

#### **Question 1:**
**"Jungkook is in 5th place. Find the number of people who crossed the finish line faster than Jungkook."**

- **Original Model Response**:
  ```
  You're asking for the number of people who finished faster than Jungkook. 
  
  Here's the problem:
  
  * We know Jungkook is in 5th place. 
  * To figure out who finished faster, we need to know the order of finishers.
  
  **Without knowing the actual finish order, we can't answer this question.** 
  
  To help me figure it out, can you give me the complete list of finishers? 😊 
  ```

- **Fine-tuned Model Response**:
  ```
  If Jungkook is in 5th place, then 4 people crossed the finish line faster than him.
  ```

> **Leave space for a video demo** showcasing queries and responses before and after fine-tuning.

---

## 🎛️ Fine-Tuning Parameters on T4 GPU

The fine-tuning was optimized for a **T4 GPU** on Google Colab, ensuring a training duration of about **30 minutes for 3 epochs**. These parameters can be adjusted depending on the available hardware, but the following settings are ideal for T4 GPUs:

- **Max Samples**: Limited to handle the GPU capacity, but could be increased with more powerful GPUs.
- **Epochs**: 3
- **Batch Size**: Adapted to the GPU to ensure no out-of-memory errors.
- **Learning Rate**: Suitable for gradual improvement without overfitting.

This setup balances training time and performance, keeping the training process efficient and effective for a mid-range GPU like T4.

![image](https://github.com/user-attachments/assets/3b04e1ce-0ef3-4e87-a766-204e3c3f58f5)


---

## 🏆 Acknowledgments

Special thanks to the original LLaMA-Factory project! Check out their official GitHub repository for more details:

🔗 [LLaMA-Factory GitHub](https://github.com/hiyouga/LLaMA-Factory?tab=readme-ov-file)

--- 

## 🤖 About the Dataset

This project leverages the [Math Word Problems 200k](https://huggingface.co/datasets/microsoft/orca-math-word-problems-200k?row=12) dataset from Microsoft. It contains 200,000 math word problems, allowing the model to gain skills in solving a variety of real-world math problems.

![image](https://github.com/user-attachments/assets/907c2483-d565-4501-993d-1d7987cc5d57)


---

## 🏁 Conclusion

The fine-tuning process showcased a clear improvement in the **Gemma-2-2B-Chat** model's ability to solve math-related word problems. By leveraging the **Math Word Problems 200k** dataset, we significantly enhanced the model’s responses, as seen in the example above. With **more powerful hardware**, further improvements could be made by increasing the **maximum samples per dataset** and **extending the training duration**.

This setup was carefully adjusted for a **T4 GPU** in Google Colab, balancing the trade-offs between training time and model quality. However, if you have access to more robust GPUs, you can easily fine-tune these parameters for even better results!

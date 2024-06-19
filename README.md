Here's a sample README file for your project:

```markdown
# Data-Driven Relationships: Exploring WeChat Conversations of Couples

In today's digital age, communication through messaging apps has become an integral part of our daily lives. Among these apps, WeChat stands out, especially in China, as a primary platform for personal and professional communication. For couples, WeChat is not just a messaging tool but a medium through which they share their lives, emotions, and experiences. Understanding these conversations can provide valuable insights into relationship dynamics and emotional health.

## Project Overview

This project aims to use data analytics to examine WeChat conversational data between couples. By applying various data science techniques, we uncover patterns and trends that reflect the nature of these interactions. The analysis includes data cleaning, descriptive statistics, sentiment analysis, and topic modeling, culminating in an interactive dashboard to visualize the findings.

## Data Source

We used the [WeChatMsg](https://github.com/LC044/WeChatMsg) application from GitHub to export chat history from WeChat. This application provides a convenient way to extract and manage chat records. The data can be exported in CSV or JSON format and includes textual, audio, video, and image data.

## Data Cleaning

The imported data contains the following columns:
- `localId`: A unique identifier for each message
- `TalkerId`: An identifier for the user participating in the conversation
- `Type`: The type of message (all values are `2` for text messages)
- `SubType`: Subtype of the message (all values are `1`)
- `IsSender`: Indicates if the message is sent by the user (`1`) or received (`0`)
- `CreateTime`: Timestamp of when the message was created, in Unix time format
- `Status`: Status of the message (e.g., sent, received)
- `StrContent`: The content of the message in Chinese
- `StrTime`: Human-readable timestamp of when the message was created
- `Remark`: Additional remarks or notes associated with the message
- `NickName`: Nickname of the user who sent the message
- `Sender`: Unique identifier for the sender's WeChat ID

## Descriptive Statistics

### Vocab Cloud (Chinese Tokenization)

We created a vocabulary cloud to visualize the most commonly used words in the conversations using the Jieba library for Chinese text segmentation.

### Chat Frequency vs. Time

We analyzed how chat frequency changes over time to identify patterns in communication, creating visualizations to show message counts by month and day.

### Average Chat Frequency Within a Day

We examined the average number of messages exchanged within different times of the day to understand daily communication habits.

## Sentiment Analysis

Using a fine-tuned version of the RoBERTa model on Chinese vocab, we classified messages as positive, negative, or neutral. This provided insights into the emotional tone of the conversations, with daily sentiment trends visualized in the interactive dashboard.

## Interactive Dashboard

We developed an interactive dashboard using the Dash framework to visualize the analyzed data. The dashboard allows users to explore sentiment data dynamically, select specific months, and view chat histories for particular days.

## Topic Modeling Using Gen AI

We used a pre-trained Llama2 model to summarize daily conversations, identifying common themes and subjects discussed. This provided a concise and engaging summary of the interactions, highlighting the essence of the conversations.

## Getting Started

### Prerequisites

- Python 3.7 or higher
- Required Python libraries: pandas, numpy, matplotlib, jieba, wordcloud, transformers, dash

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/wechat-relationship-analysis.git
   cd wechat-relationship-analysis
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Acknowledgments

- Thanks to the [WeChatMsg](https://github.com/LC044/WeChatMsg) team for their useful application.

```

# Unbody: The Only API You Need to Build AI-Native Solutions

Welcome to **Unbody**, the go-to API for developers who want to build scalable, real-world AI solutions without needing a PhD in machine learning. With Unbody, you can integrate powerful AI capabilities directly into your applications, making AI development more accessible and straightforward than ever before.

## 🚀 Key Features

- **Data Integration**: Seamlessly integrates data from various sources and formats (text, images, videos, etc.).
- **Model Flexibility**: Supports multiple AI models, including OpenAI and open-source alternatives, enabling custom solutions for different use cases.
- **Automated Pipelines**: Automates the entire AI development process from data ingestion and processing to model deployment and monitoring.
- **Scalability**: Designed to handle large datasets and scalable AI applications.
- **Security and Compliance**: Built-in features to ensure data privacy, security, and compliance with industry standards.
- **Multimodal Capabilities**: Supports applications requiring multimodal input and output, such as search engines that handle text, images, and videos.
- **Media Streaming and CDN**: Integrates with media streaming APIs and CDNs for efficient content delivery.
- **Real-time Monitoring**: Provides real-time analytics and monitoring to optimize AI models and data flow.

## Use Cases

Unbody can be used for a variety of AI applications, including but not limited to:

- **Multimodal Search Engines**: Enhance search capabilities by allowing users to query across text, images, and videos using semantic search.
- **Custom AI Chatbots**: Build chatbots that understand and interact using natural language, tailored to your specific data.
- **Product Recommendation Engines**: Develop recommendation systems that personalize user experiences and drive engagement.
- **AI Assistants**: Create AI-driven assistants to automate tasks and improve productivity.
- **Profile Matching Engines**: Design matching algorithms for recruitment, dating, or networking platforms.
- **Custom RAG APIs**: Provide tailored AI experiences by combining data retrieval with generative responses.


## 📦 Installation
```bash
npm install @unbody-io/ts-client
```

## 🛠️ Usage

Unbody is designed to be simple and intuitive. Here's a quick example to get you started with a RAG:

```js
const unbody = new Unbody({
    apiKey: "API_KEY",
    projectId: "PROJECT_ID",
});

const query = "A movie director";
const prompt = "Explain why these information are related to each other.";

const queries = [
  // Google Docs
	unbody.get.googleDoc.limit(3)
                      .search.about(query)
                      .generate.fromMany(prompt, ["title","autoSummary"]),

  // Paragraphs
	unbody.get.textBlock.limit(3)
                      .search.about(query)
                      .generate.fromMany(prompt, ["text"]),

  // PDFs, .DocX, .RTF
  unbody.get.textDocument.limit(3)
                      .search.about(query)
                      .generate.fromMany(prompt, ["title","autoSummary"])

  // Images
  unbody.get.imageBlock.limit(3)
                      .search.about(query)
                      .generate.fromMany(prompt, ["autoCaption","autoOCR"])

];

const response = await unbody.exec(queries);
console.log(response);

```

For more detailed usage, check out our [documentation]([https://github.com/yourusername/unbody/wiki](https://www.unbody.io/docs)).

## 📚 Documentation

For full documentation, including advanced usage, API reference, and more, please visit our [Docs]([https://github.com/yourusername/unbody/wiki](https://www.unbody.io/docs)).

## 💡 Examples

We’ve provided a few example projects to help you get started with Unbody:

- **Text Generation:** An example project showcasing the text generation capabilities.
- **Image Captioning:** Learn how to generate captions for images using Unbody.
- **Chatbot Development:** Build an AI-powered chatbot from scratch.

## 🤝 Contributing
Soon...

## 🛡️ License
Soon...

## 📫 Contact

Have questions, suggestions, or feedback? Feel free to open an issue or reach out to us at [hello@unbody.io](mailto:hello@unbody.io).

## 🌟 Support
If you find Unbody helpful, please give us a star ⭐ on GitHub and spread the word!

# Unbody: The Only API You Need to Build AI-Native Solutions

Welcome to **Unbody**, the go-to API for developers who want to build scalable, real-world AI solutions without needing a PhD in machine learning. With Unbody, you can integrate powerful AI capabilities directly into your applications, making AI development more accessible and straightforward than ever before.

## 🚀 Key Features

- **AI-Native API:** Specifically designed for building AI-native solutions that are scalable and efficient.
- **Developer-Friendly:** Built for developers who want to focus on building, not diving into complex ML theories.
- **Flexible and Scalable:** Supports a wide range of use cases, from simple AI integrations to complex, large-scale AI systems.
- **Open Source:** Community-driven and open-source, with a focus on collaboration and continuous improvement.
- **Easy Integration:** Quick and easy setup with comprehensive documentation and support.

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

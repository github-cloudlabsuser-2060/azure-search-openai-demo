# Backend Application Documentation

This document provides an overview of the backend application for the Azure Search OpenAI Demo project, located in the `app/backend/` directory.

## Overview

The backend application is built using [Quart](https://quart.palletsprojects.com/), a Python framework for asynchronous web applications. It serves as the core logic layer that interfaces with both the Azure Cognitive Search and OpenAI services, providing a seamless integration to power the Chat App's functionality.

## Features

The backend application supports a variety of features, including:

- **Configurable Options**: Dynamically configurable options for the frontend, such as enabling GPT-4V, Semantic Ranker, Vector Search, User Upload, Speech Input, and Speech Output. See [`config()`](../../../../../../c:/Users/azureuser/Downloads/azure-search-openai-demo-main/azure-search-openai-demo-main/app/backend/app.py) for more details.
- **Chat and Ask Tabs**: Supports different RAG (Retrieval Augmented Generation) approaches for the Chat and Ask tabs, allowing for customizable interaction modes. The primary logic for these features is located in the `app/backend/approaches` directory.
- **Integration with Azure AI and OpenAI**: Utilizes Azure Cognitive Search for querying data and OpenAI's ChatCompletion API for generating responses based on the search results.

## Configuration

The backend application can be configured through environment variables and the `config()` function. Some of the key configurable features include:

- `CONFIG_GPT4V_DEPLOYED`: Enables GPT-4V options in the frontend.
- `CONFIG_SEMANTIC_RANKER_DEPLOYED`: Enables Semantic Ranker option.
- `CONFIG_VECTOR_SEARCH_ENABLED`: Enables Vector Search option.
- `CONFIG_USER_UPLOAD_ENABLED`: Allows users to upload documents.
- `CONFIG_SPEECH_INPUT_ENABLED`: Enables speech input feature.
- `CONFIG_SPEECH_OUTPUT_ENABLED`: Enables speech output feature.

## Deployment

The backend application is designed to be deployed as an Azure App Service. The deployment configuration can be found in the [main.bicep](../../../../../../c:/Users/azureuser/Downloads/azure-search-openai-demo-main/azure-search-openai-demo-main/infra/main.bicep) file, which includes settings for runtime, authentication, and network access.

## Customization

To customize the backend for your specific needs, consider modifying:

- **Approaches**: The logic for Chat and Ask tabs in the `app/backend/approaches` directory to match your data and desired interaction patterns.
- **Configuration**: The `config()` function and environment variables to enable or disable features as needed.

For more detailed customization instructions, refer to the [Customizing the backend](../../../../../../c:/Users/azureuser/Downloads/azure-search-openai-demo-main/azure-search-openai-demo-main/docs/customization.md#customizing-the-backend) section in the project documentation.

## Conclusion

The backend application of the Azure Search OpenAI Demo project provides a robust and flexible foundation for building chat applications powered by Azure Cognitive Search and OpenAI. By leveraging Quart and the provided customization options, developers can tailor the application to meet their specific requirements.
# Multimodal Video Querying and Interaction System

This project implements a sophisticated question-answering system that interacts with video content using multimodal AI. By combining text, image, and video processing models, this system allows users to query and interact with video data through text-based inputs, returning relevant frames, captions, and responses.

### Project Overview
The system integrates multiple advanced AI technologies to build a Multimodal Retrieval-Augmented Generation (RAG) system. It leverages multimodal embedding models, large vision language models (LVLMs), and cloud infrastructure to handle complex queries involving video data.


### Key Features
1. Multimodal Embeddings: Utilizes the BridgeTower model to create embeddings from video frames and captions, mapping them into a joint semantic space for effective similarity-based retrieval.

2. Video Processing Pipeline: Extracts frames and generates captions from videos using Whisper for transcription and LLaVA 1.5 for captioning and visual question answering.

3. Multimodal Retrieval: Uses LanceDB and LangChain to store and retrieve high-dimensional vectors, ensuring that relevant video segments are returned based on user text queries.

### Technologies Used :-
1. BridgeTower: Multimodal embedding model for joint image-caption representations.
2. Whisper: Model for automatic speech recognition and transcription from videos.
3. LLaVA 1.5: Large Vision Language Model for generating captions and answering questions based on visual data.
4. LanceDB: Vector database for storing and retrieving multimodal embeddings.
5. LangChain: Framework for building retrieval pipelines.
6. Intel Cloud APIs: Access multimodal models via PredictionGuard and deploy with Intel Gaudi AI accelerators.


### Project Architecture

1. Multimodal Embedding: Video frames and captions are processed and embedded in a shared semantic space using BridgeTower.
2. Video Processing: Videos are pre-processed by extracting frames, transcribing audio with Whisper, and generating captions with LLaVA 1.5.
3. Vector Database: Embedded data is stored in LanceDB, enabling efficient vector searches.
4. Retrieval and Response Generation: Upon receiving a text query, the system retrieves relevant video segments and generates a contextual response using LVLMs.

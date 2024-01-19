# MonReader

This project develops a machine learning model for classification tasks in the field of computer vision. In the notebook, a three-layer CNN model is trained on the low-resolution images of a book from the mobile. The trained model extracts the relevant features and patterns from the low-resolution image and classifies them as 'flip' and 'not flip'.

Let's start with a small description of the relevance of this project to an industrial application. MonReader is a new mobile document digitization experience for the blind, researchers, and everyone else needing fully automatic, high-speed, and high-quality document scanning in bulk. It is composed of a mobile app and all the user needs to do is flip pages MonReader handles everything: it detects page flips from a low-resolution camera preview and takes a high-resolution picture of the document, recognizing its corners and crops it accordingly, and it dewarps the cropped document to obtain a bird's eye view, sharpens the contrast between the text and the background and finally recognizes the text with formatting kept intact, being further corrected by MonReader's ML powered reactor.

Here, I am focusing on the first step of the MonReader process, i.e. detecting a page flip from low-resolution images, which triggers subsequent steps from capturing high-resolution images to reading text.

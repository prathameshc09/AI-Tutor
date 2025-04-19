**Key Learnings from the project.**

**Flask App Setup:**

We set up a Flask application and configure it to connect to a MongoDB database called ai_tutor.

**File Upload Handling:**

The /upload route handles the PDF file upload. It checks for the presence of the file, saves it to a specified directory, and then calls the function to extract text from the PDF.

**PDF Text Extraction:**

The extract_text_from_pdf function uses PyPDF2 to read the PDF file and extract text from each page.

**Store Extracted Text:**

The extracted text is stored in the pdfs collection in MongoDB. The uploaded file is deleted after processing to save space.

**Response:**

The server responds with a JSON object that includes a success message and the extracted text.

**Conclusion:**

This implementation allows users to upload a PDF file, automatically extracts the text upon upload, stores it in MongoDB, and returns the extracted text in the response.

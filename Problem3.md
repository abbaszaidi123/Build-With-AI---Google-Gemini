# Problem Statement: Building a Streamlit Application for Gemini LLM Chat

## Background
In this project, you are tasked with creating a Streamlit application that utilizes the Google Generative AI model (Gemini) to facilitate a conversational experience. The Gemini model is a Large Language Model (LLM) capable of generating text responses based on user input.

## Task
Your objective is to develop an interactive Streamlit chat application that allows users to input questions, receives responses generated by the Gemini LLM, and maintains a chat history.

## Steps

1. **Environment Setup:**
   - Ensure Python is installed on your machine.
   - Make sure to have Python installed on your machine.
   - Create a requirements.txt file and add the following dependencies in the list 
        - streamlit
        - google-generativeai
        - python-dotenv
   - Install the necessary Python packages using the following command:
     ```bash
     pip install -r requirements.txt
     ```

2. **API Key Configuration:**
   - Acquire a Google API key and set it as an environment variable, preferably in a `.env` file.
   - Confirm that the Google API key is accessible using the `os.getenv("GOOGLE_API_KEY")` command.

3. **Gemini Model Configuration:**
   - Configure the Gemini model with the provided Google API key using `genai.configure(api_key=os.getenv("GOOGLE_API_KEY"))`.

4. **Streamlit App Initialization:**
   - Initialize the Streamlit app with a page title and header using `st.set_page_config()` and `st.header()`.

5. **Initialize Chat Session:**
   - Create a session state to store the chat history. If it doesn't exist, initialize it as an empty list (`st.session_state['chat_history'] = []`).

6. **Load Gemini Pro Model:**
   - Load the Gemini Pro model using `genai.GenerativeModel("gemini-pro")` and start a chat session.

7. **User Input Interface:**
   - Create a text input box for users to input questions using `st.text_input()` and provide a key for tracking changes.

8. **Ask Button:**
   - Implement a button (e.g., "Ask the question") to trigger the Gemini model with the user input.

9. **Gemini Response Function:**
   - Create the function `get_gemini_response(question)` to interact with the Gemini model and retrieve responses.

10. **Display Response:**
    - If the "Ask the question" button is clicked and there is user input, call the `get_gemini_response()` function and display the generated response using `st.subheader()` and `st.write()`.

11. **Chat History Display:**
    - Display the chat history using `st.subheader()` and iterate through the stored chat history, showing the role (User/Bot) and the corresponding text.

12. **Run the Application:**
    - Run the Streamlit application locally using the command:
      ```bash
      streamlit run app.py
      ```

13. **Test the Application:**
    - Test the application by asking various questions and observing the responses and chat history.

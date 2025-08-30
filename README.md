# AlgoRhythms
📘 StudyMate – An AI-powered PDF Q&amp;A system for students. Upload textbooks, notes, or research papers and get instant, context-aware answers. Built with Python, Streamlit, FAISS, and Hugging Face, it makes studying faster, smarter, and more interactive.
# frontend 
import streamlit as st

st.set_page_config(page_title="StudyMate PDF Q&A", layout="centered")
st.title("StudyMate: AI-Powered PDF Q&A System")

st.sidebar.header("Upload your PDFs")
uploaded_file = st.sidebar.file_uploader("Select a PDF file", type=["pdf"])

st.write("Ask a question about your study material:")

question = st.text_input("Question", "")

if uploaded_file and question:
    with st.spinner("Processing..."):
        # Import backend logic here; for demo, assume function answer_question exists
        answer = answer_question(uploaded_file, question)
        st.success("Answer:")
        st.write(answer)

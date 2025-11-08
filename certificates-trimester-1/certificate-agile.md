import PyPDF2

path = r"\\wsl.localhost\Ubuntu-24.04\home\ravou\holbertonschool-france-certificates-ibm\image\IBMDesign20251108-31-af5jco.pdf"

with open(path, "rb") as file:
    reader = PyPDF2.PdfReader(file)
    for page in reader.pages:
        print(page.extract_text())


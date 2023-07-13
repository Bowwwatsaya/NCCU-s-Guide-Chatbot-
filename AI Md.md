**NCCU’s Guide Chatbot**

**Project Description**

NCCU’s Guide Chatbot is designed to make navigating the NCCU campus easier and more accessible for foreign students. Our team noticed that the navigation tools provided by the school are not foreign-friendly due to the platform being mainly in Chinese and hard to access. We also notice the inconsistency of the building name as some do not have English or Pinyin names, making it even more confusing for foreigners. As we breakdown the school’s map and went through all the available resources, we came to a conclusion on how we are going to go forward with our Chatbot. The main feature of our chatbot is being able for users to ask any questions about building names in either Chinese, English, and Pinyin, subject names, and subject codes. The outcome would include the building name in all Chinese, English, and Pinyin, the bus number, the closest bus stop, and a Google Map link that will directly bring you to the specific location. Putting all the information together and making the platform into a chatbot allows students to save time searching for places and provide all the detailed information that the existing tools do not provide.

**Getting Started**

Our project is available on Google Collab which is a website that allows you to run the code without downloading any program. This is the construction to use our NCCU’s Guide Chatbot.

1\. Download the building information dataset and upload it to your Google Drive.

[Click here to download the building dataset](https://docs.google.com/spreadsheets/d/1dmc4Ky6EDZLD6zuzny7ENDGRd7iMZXSi/edit?pli=1#gid=526785390)

2\. Go to our project Colab link below. [Click here to open our project Colab](https://colab.research.google.com/drive/1ge4b-3qHhqCWXI-to1mOVUTRDN80w2Tz?usp=sharing)

Please save a copy of this file in your drive [Go to File \> (Click) Save a copy in Drive]

![](media/ac85419484eac71405032c66644ef1b5.png)

3\. Before processing, please put your Openai API Key in the code. If you don’t have one, no worries. Please [click here to create your](https://platform.openai.com/account/api-keys).

After you have already created your Openai API Key, please copy it and paste it in the code according to the picture. Then run the code until this cell.

![](media/fdb5a127f0bac2a2d5a0c6a777001097.jpg)

4.After you finished uploading the dataset file to your Google Drive and already ran API code. (Click) File at the left bar \> drive \> my drive and find the dataset file. Then copy path the link and paste it at this code

![](media/ff384f14328277640650f468f53b9469.jpg)

![](media/8e765716b8ff987711ddc14b7ed7f3c3.jpg)

5\. Run all the code

6\. Enjoy using our NCCU’s Guide chatbot by putting your questions or queries on Gradio and see the results.

![](media/d81b8b57ad27995385f86fc81fd35a29.png)

**File Structure**

In our project, we collected building data from qrysub.nccu.edu.tw and organized it in an Excel file. Our project files and their structure are as follows:

1.  **Building Data File**: The main Excel file where we combined all the data. It consists of 18 sheets, with each sheet representing a different building. The sheets are named based on the building's name in Pinyin. Each sheet contains the following columns: Building name in English, Building name in Chinese, Building name in Pinyin, Subject in English, Subject in Chinese, Subject code, Room number, Nearest bus stop in Chinese, Bus number, and Google Map link. This file consolidates all the building data in one place, making it easier for us to manage and access the information for each building.   
    However, having many sheets in one file is too complicated for the python to read the file. Therefore, we combine the information of each building in one excel sheet at the end. The columns are still the same as the previous file.

    The sources of all NCCU building came from as follows:

    1.  qrysub.nccu.edu.tw Data: On this website, only the building’s name in Chinese and English, the subject’s name in Chinese and English, the subject code, and the classroom numbers are available. We download all of the data on this website to Excel. Once we import data our resource does not provide the Pinyin name of each building. We manually put each name into Google Translate and copy the Pinyin name from there.
    2.  行動政大 Application Data: gather bus number and bus stop data from the 行動政大 application, which have the most detailed information about the bus schedule and bus stops.
    3.  Google Maps Data: We pinned the location of each building separately on google maps based on the building’s name and copied the Google Map link to Excel for enabling easy access to precise building locations.
2.  **README.md** : This file provides an overview and instructions for using NCCU’s Guide Chatbot project.
3.  **NCCU'S GUIDE CHATBOT.ipynb :** Our main python file contains the NCCU's Guide Chatbot project. It contains the code for the chatbot, allowing users to interact with the system, ask questions about NCCU buildings, and receive relevant information.

**Analysis**

Our analysis involves using the "llama-index" module to create a question-answering system for the NCCU Buildings dataset. We set the OpenAI API key and install libraries like pandas and llama-index for modifying data and indexing.

We read the data from the Excel file into a Pandas dataframe and create a GPTPandasIndex for efficient querying. The LLMPredictor, PromptHelper, and ServiceContext modules manage language model selection and parameter settings.

For user interaction, we develop a question-answer prompt template and use the "ask_ai" function's query engine to produce answers based on user input. Finally, we use Gradio to build a user interface that can be launched and shared with others.

In summary, our analysis involves data collection, library setup, querying with llama-index, and creating a user-friendly chatbot interface.

The main insight gained from our chatbot is the ability to ask questions about NCCU buildings and receive answers based on the information available in the dataset. This is related to our previous problem statement ‘How to navigate the NCCU campus’.

**Results**

**![](media/0bbe894054be91110394106c17e19d2a.png)**

Our NCCU's Guide Chatbot successfully responds to user inquiries by providing details about NCCU buildings. The "llama-index" library is used by the chatbot to efficiently index and query the building data. The "get-3.5-turbo" language model produces responses that are precise and contextually relevant.

Users can interact with the chatbot by inputting their questions about NCCU buildings. After processing the questions, the chatbot provides informative responses based on the available data. The responses are displayed in the user interface, allowing users to obtain the desired information easily. The combination of the "llama-index" library and the "get-3.5-turbo" language model resulted in an efficient system for indexing, querying, and generating accurate responses. Although the image feature mentioned in the code was not available, the chatbot's overall performance is still accessible.  
Further improvements can be made by expanding the dataset, refining prompts, and incorporating additional features based on user feedback.The NCCU's Guide Chatbot is a useful tool for guide users to the buildings at NCCU.

**Contributors**

Karin Sumritluan 陳琪玲 : poster, data collection, Git-hub, presentation

Natcha Jaibumrung 文晶晶 : coding, data collection, Git-hub, Presentation

Ratchadaporn Leungphetngam 陳秋天 : coding, data collection, Git-hub, and presentation

Watsayaporn Srimueanghao 史沃天 : coding, data collection, Git-hub, and presentation

Edric Kee Hong Zhao 紀宏釗 - data collection and presentation

**Acknowledgments**

We would like to sincerely thank Professor Pien Chung-Pei, our instructor for Introduction to AI class, for his advice and assistance throughout the development of our NCCU's Guide Chatbot project. His expertise and knowledge have been helpful for developing our project and guiding us in overcoming obstacles.

We also would like to deeply appreciate other teams who provided assistance and support during the development of our NCCU's Guide Chatbot project. Their collaboration, feedback, and contributions have been invaluable in improving the functionality and effectiveness of our chatbot.

Lastly, thank you to each member of the team who is involved in this project. Your effort, dedication, and teamwork were important for creating our chatbot. It is through your hard work and commitment that we have been able to create a practical and helpful tool for NCCU students and others.

**Reference**

1.The NCCU building data source

<https://www.google.com/maps>

<https://qrysub.nccu.edu.tw./>

<http://sgnweb.nccu.edu.tw/mnccu/>

2.Model Reference  
<https://huggingface.co/llamaindex>

3.Prompt Reference

[https://gpt-index.readthedocs.io/en/v0.5.27/how_to/customization/custom_prompts.htm](https://gpt-index.readthedocs.io/en/v0.5.27/how_to/customization/custom_prompts.html)

4.Gradio Reference

<https://www.gradio.app/guides/sharing-your-app>

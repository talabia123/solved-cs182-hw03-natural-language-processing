Download Link: https://assignmentchef.com/product/solved-cs182-hw03-natural-language-processing
<br>
Welcome to the third homework of CS182, in this assignment, you will learn about processing and generating text. Specifically, you will build a neural network to generate news headlines, through the training of an LSTM-based language model. Then you will train a Transformer to summarize news articles.

<h1><a id="user-content-deliverables" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#deliverables" aria-hidden="true"></a>Deliverables</h1>

To complete each assignment, you must fill in, the two provided Jupyter notebooks with your solution, this might lead you to edit Python files in this folder.

Through the Notebook, you will produce 2 model files in the .ckpt format. These are part of your deliverables and should be uploaded with your project, as they will be tested against an <strong>unreleased test set</strong> for each notebook.

To prepared your ZIP deliverable, read and follow instructions in the “Preparing a Submission” section.

<h1><a id="user-content-installation" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#installation" aria-hidden="true"></a>Installation</h1>

This assignment requires Python 3. If you plan to complete this assignment with a local machine, and not in the Google Colab, please install Python 3.

<h2><a id="user-content-linux--mac-os" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#linux--mac-os" aria-hidden="true"></a>Linux / MAC Os</h2>

Installing on Linux is very similar to the previous assignments. You can run the following:

To create a virtual environment. Running:

will install the python requirements for the assignment. <strong>Make sure that you are running a version of python &gt;= 3.5</strong>. If you are not (which can be checked with <code>python3 --version</code>) install an updated version of python using the instructions here: <a href="https://www.tecmint.com/install-python-in-ubuntu/" rel="nofollow">https://www.tecmint.com/install-python-in-ubuntu/</a>

Open one of the .ipynb assignment files through Jupyter in a browser and make sure you are using the right Python environment by going into the “Kernel” tab “change kernel” and selecting the correct kernel to run the code in (Python 3).

You now must install the required packages for the assignment. If you are using a GPU-enabled machine:

Otherwise:

<h2><a id="user-content-windows" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#windows" aria-hidden="true"></a>Windows</h2>

Windows is not officially supported. There is a chance that you will be able to get this working with Anaconda on windows, however we strongly suggest using a virtual machine (virtual box) with an installation of linux, as it will likely be more stable, and the GSIs will be able to provide additional assistance.

<h2><a id="user-content-colab" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#colab" aria-hidden="true"></a>Colab</h2>

You can use our modified Notebooks for the Google Colab. Google Colab notebooks can be used with a CPU, or with a K-80 GPU (on this assignment, it seems to give a 5x training speed boost). The Notebooks we have shared on Google Colab have been modified so that it is easy to access the datasets in your Google Drive, and save the model files. If you opt for this option, you will have to duplicate the folder on Google Drive and work on the assignment in your copy. However, you must recuperate the models, and verify that they work locally before submitting your files. he dataset files are available for download in this folder: <a href="https://drive.google.com/open?id=1TNhUy9ldZ5mv_GLNNmCBFnLfT3DXwntF" rel="nofollow">https://drive.google.com/open?id=1TNhUy9ldZ5mv_GLNNmCBFnLfT3DXwntF</a> You must be logged in on your UC Berkeley Google account to see the folder, and you must duplicate it (copy it to your own drive) to have write access over the files. The .ipynb can be opened into the Google Colab by double clicked and selecting “Open with Colaboratory”.

<h1><a id="user-content-downloading-the-data" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#downloading-the-data" aria-hidden="true"></a>Downloading the Data</h1>

To download the data, run the following command from the assignment root directory:

If you get the error “bash: ./download_data.sh: Permission denied” run <code>chmod +x download_data.sh</code> and try again.

<h1><a id="user-content-preparing-a-submission" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#preparing-a-submission" aria-hidden="true"></a>Preparing a Submission</h1>

To prepare a submission, run the following command from the assignment root directory:

This will create a “submission.zip” file which can be submitted for the homework. You may get a warning if the files required do not exist – please pay attention to this, as we will not be responsible if you forget to include these files in the zipped folder. Check that your submission contains:

<ul>

 <li>“1 Language Modeling.ipynb” and “2 Summarization.ipynb”</li>

 <li>“capita.py”, “transformer.py”, “transformer_attention.py”, “transformer_layers.py”</li>

 <li>Your model files (.index, .cptk, .data) for each notebook. The names of the models you upload should match the names you put in the Jupyter notebooks. This should be a total of 6 files.</li>

</ul>

If you get the error “bash: ./prepare_submission.sh: Permission denied” run <code>chmod +x download_data.sh</code> and try again.

<h1><a id="user-content-questions" class="anchor" href="https://github.com/Dhanush123/cs182/tree/master/assignment3#questions" aria-hidden="true"></a>Questions</h1>

Ask your questions on Piazza. If you have questions about the creation of the dataset or the assignment, contact Philippe Laban (<a href="/cdn-cgi/l/email-protection#2f5f474643434e4d6f4d4a5d444a434a56014a4b5a"><span class="__cf_email__" data-cfemail="90e0f8f9fcfcf1f2d0f2f5e2fbf5fcf5e9bef5f4e5">[email protected]</span></a>) or John Canny (<a href="/cdn-cgi/l/email-protection#afcccec1c1d6efcdcaddc4cac3cad681cacbda"><span class="__cf_email__" data-cfemail="0467656a6a7d446661766f6168617d2a616071">[email protected]</span></a>). If you are an instructor looking for the unreleased test-set and Solution notebooks, you can contact us as well.

5/5 - (2 votes)

<pre>virtualenv .env --python=python3</pre>

<pre><span class="pl-c1">source</span> .env/bin/activate</pre>

<pre>pip3 install -r requirements_gpu.txt</pre>

<pre>pip3 install -r requirements.txt</pre>

<pre>bash download_data.sh</pre>
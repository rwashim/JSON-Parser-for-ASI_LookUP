# JSON-Parser-for-ASI-ASI_LookUP

![ASI](https://github.com/rwashim/JSON-Parser-for-ASI-ASI_LookUP-/assets/44086222/47d4e50e-5e0f-4639-ab7f-556e0a44a626)



The script is designed to retrieve and process information from the ASI platform, generating detailed reports in Excel workbooks. For data parsing and organizing, it only accepts ASI JSON output files, and for sheet indexing, it only accepts Excel workbook (.xlsx) files. 



**What is ASI?**

Attack Surface Intelligence (ASI) is a feature provided by SecurityScorecard that allows users to expand and deepen their understanding of cyber threats from a viewpoint that ranges from global to granular1.

ASI provides direct access to SecurityScorecard’s data with more than 4.1 billion IP addresses scanned every 10 days across 1500+ ports globally1. Using powerful search capabilities, you can find and correlate the latest information on IPs, open ports, and vulnerabilities, threat actors, ransomware group campaigns, and other data points.

ASI is a powerful tool for understanding and managing cyber threats, providing a comprehensive view of the threat landscape and enabling effective remediation strategies.

**NOTE:** Only SecurityScorard's ASI JSON output is compatible with this script.

**1.   Purpose:**

The script is designed to retrieve and process information from the ASI platform, generating detailed reports in Excel workbooks. For data parsing and organizing, it only accepts ASI JSON output files, and for sheet indexing, it only accepts Excel workbook (.xlsx) files. 


2.  **Prerequisites:**

    1.  Python 3.x installed on the system.

    2.  Need to install required Python packages:

        1.  Ensure that you have the pip package manager installed. If
            you don't have pip, you can install it using the following
            command:

            > python -m ensurepip --upgrade

2.  Open a terminal or command prompt and navigate to the directory where the requirements.txt file is located.

3.  Run the following command to install the packages listed in the requirements.txt file:

    > pip install -r requirements.txt

This command will install all of the packages listed in the  requirements.txt file. If any of the packages are already installed, pip will skip them and install only the packages that are not yet installed.

3.  **Script Overview:**

The ASI Lookup script performs the following tasks:

-   Parses JSON data into different tables and stores them in separate worksheets within output.xlsx.

-   Supports input only ASI JSON files.

-   Provides the --index feature to index any workbook.

4.  **Usage:**

    1.  **Command Line Syntax:** Open a command prompt in the script's
        directory and execute the following commands:

        1.  To use JSON file input:

            > python ASI_LookUp-v2.py --json \<filename/filepath>

    2.  To index any workbook:

         > python ASI_LookUp-v2.py --index \<filename/filepath>

    3.  For help and additional information:

          > python ASI_LookUp-v2.py -h


5.  **Using the Script:**

    1.  **Managing ASI JSON:** The ASI Lookup script does not require an
        API Key to operate. This is because the script does not execute
        any ASI queries or communicate with the ASI platform. Instead,
        it simply parses the provided ASI JSON output file and generates
        the requested report.

        1.  **Explanation:**

            -   The script is designed to work offline and does not
                require an internet connection. It processes the ASI
                JSON output file, which is a static file containing the
                results of a previous ASI query. The script analyzes
                this data and generates the report based on the
                specified parameters

        2.  **Steps:**

            -   Obtain an ASI JSON output file. This can be generated by
                executing an ASI query using the ASI platform.

            -   Run the script with the --json parameter followed by the
                path to your ASI JSON output file. For instance:

                > python ASI_LookUp-v2.py --json asioutput.json

2.  **Indexing Workbooks:** The script provides the --index feature,
    which allows you to index any workbook. Indexing a workbook involves
    enhancing its accessibility and searchability by creating an index
    of its contents.

    1.  **Explanation:**

        -   Execute the script with the --index parameter followed by
            the filename or filepath of the workbook you want to index.

        -   The script will create an index of the workbook's contents,
            improving your ability to search for specific information
            within the workbook.

    2.  **Steps:**

        -   Run the script with the --index parameter followed by the
            filename or filepath of the workbook you want to index. For
            instance:

             > python ASI_LookUp-v2.py --index MyWorkbook.xlsx

-   The script will generate an index of the specified workbook,
    enhancing its accessibility and searchability.

7.  **Troubleshooting**:

    1.  Ensure Python 3.x is installed.
    2.  Verify Python packages and their versions.
    3.  Check JSON file format and accessibility

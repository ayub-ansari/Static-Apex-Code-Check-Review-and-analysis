# Static-Apex-Code-Check-Review-and-analysis
Static Apex Code Check, Review and analysis

## Prerequisites and Steps
* Linux based OS- I am using ubuntu.
* Install [ant (Latest version)](https://howtoprogram.xyz/2016/10/14/install-apache-ant-ubuntu-16-04-lts-xenial-xerus/)
* Download the [latest version](https://help.github.com/articles/basic-writing-and-formatting-syntax/)- it would be a zip file
* Extract that zip file- it will make a folder with name of PMD Zip file
* Open terminal and change your directory to that PMD folder
* Create a folder ‘scan’- you can manage your own - I just created to keep my stuffs in different folders. You just need to adjust the path in below given script while executing the script
* Download all XML files from [here](https://help.github.com/articles/basic-writing-and-formatting-syntax/). Actually these are defined Rulesets for each type of code check. For example, performance.xml will check the performance issues in the apex code like SOQL/DMLs inside loop.
* Run the below given script. 
     ~~~
     ./bin/run.sh pmd -d "./scan/ap_code/classes" -f html -R "./scan/security.xml,./scan/performance.xml,./scan/apexunit.xml"   - reportfile "./scan/codereview.html" -language apex
     ~~~
     - "./scan/ap_code/classes"     is directory path of folder where all apex code is.
     - "./scan/security.xml,./scan/performance.xml,./scan/apexunit.xml"    is comma separated paths of rulesets that we are going to execute
     - ./scan/codereview.html"   is direcoty path and name of file in which you are going to store the result of code scan.
* Now go to path and there should be a file codereview.html in scan folder with results

## Links
* https://pmd.github.io/pmd-5.5.2/pmd-apex/rules/index.html
* http://www.jitendrazaa.com/blog/salesforce/automated-code-review-for-apex-in-salesforce-static-code-analysis-video/


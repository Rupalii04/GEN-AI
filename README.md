# GENAI-Aliq-Tshirt
Project revolves around the use of generative AI features lang chain chroma, db , Sql database which asks the questions from the application about the t shirt prices and using gen ai the app will answer the same using GOOGLEPALM model.

# Steps for deployment using AWS RDS AND EC2 INSTANCE 

1. Create a RDS database for mysql database.
2. After creation of database copy its endpoint and go to mysql workbench.
3. Write the Hostname as rds endpoint url .
4. Connect with local db.
5. Now run DB_CREATION_ATLIQ_T_SHIRTS.SQL file in your server.
6. go to the untitled file run the proper code in local server.


 # DEPLOYMENT OF Streamlit on AWS EC2 instance 

 1. Create an ec2 instance with linux AMI.
 2. CONNECT the instance WITH PUTTY GEN FOR windows user.
 3. AFTER CONNECTING RUN THE FOLLOWING COMMANDS.

1. sudo su
2. yum update
3. yum install git
4. git clone < url of github repo >
5. pip install python3 
6. python3 -m venv myenv
7. source myenv/bin/activate
8. python3 -m pip install --upgrade --no-dips --force -reinstall -v requirements.txt
9. pip install --upgrade streamlit
10. python3 -m streamlit run main.py


NOTE: IF THE ERROR COMES IN INSTALLING THE REQUIREMENTS.TXT OR IT GET STOPPED DURING THE INSTALLATION DO THESE STEPS

Your disk usage shows that you still have a significant amount of free space available (26G on /). The "No space left on device" error could be related to the /tmp directory or the file system where temporary files are stored during the installation process.

Steps to Resolve:
Clean Up the /tmp Directory:
Sometimes, the temporary directory can fill up, causing issues during large installations. Try cleaning up the /tmp directory:


sudo rm -rf /tmp/*


Specify a Different Temporary Directory:
You can direct pip to use a different directory with more space for temporary files during installation. For example, you can use the /home/ec2-user/ directory:


TMPDIR=/home/ec2-user/ pip install torch sentence-transformers


Retry Installation:
After cleaning up or setting a different temporary directory, try running the installation command again.

These steps should help resolve the issue and allow the installation to proceed.



THIS WILL DEPLOY YOUR APPLICATION IN THE SERVER.

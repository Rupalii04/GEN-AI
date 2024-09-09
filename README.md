# GENAI-Aliq-Tshirt
Project revolves around the use of generative AI features lang chain chroma, db , Sql database which asks the questions from the application about the t shirt prices and using gen ai the app will answer the same using GOOGLEPALM model.

# Steps for deployment using AWS RDS AND EC2 INSTANCE
Create a RDS database for mysql database.
After creation of database copy its endpoint and go to mysql workbench.
Write the Hostname as rds endpoint url .
Connect with local db.
Now run DB_CREATION_ATLIQ_T_SHIRTS.SQL file in your server.
go to the untitled file run the proper code in local server.

# DEPLOYMENT OF Streamlit on AWS EC2 instance
Create an ec2 instance with linux AMI.

CONNECT the instance WITH PUTTY GEN FOR windows user.

AFTER CONNECTING RUN THE FOLLOWING COMMANDS.

sudo su

yum update

yum install git

git clone < url of github repo >

pip install python3

python3 -m venv myenv

source myenv/bin/activate

python3 -m pip install --upgrade --no-dips --force -reinstall -v requirements.txt

pip install --upgrade streamlit

python3 -m streamlit run main.py

NOTE: IF THE ERROR COMES IN INSTALLING THE REQUIREMENTS.TXT OR IT GET STOPPED DURING THE INSTALLATION DO THESE STEPS

Your disk usage shows that you still have a significant amount of free space available (26G on /). The "No space left on device" error could be related to the /tmp directory or the file system where temporary files are stored during the installation process.

Steps to Resolve: Clean Up the /tmp Directory: Sometimes, the temporary directory can fill up, causing issues during large installations. Try cleaning up the /tmp directory:

sudo rm -rf /tmp/*

Specify a Different Temporary Directory: You can direct pip to use a different directory with more space for temporary files during installation. For example, you can use the /home/ec2-user/ directory:

TMPDIR=/home/ec2-user/ pip install torch sentence-transformers

Retry Installation: After cleaning up or setting a different temporary directory, try running the installation command again.

These steps should help resolve the issue and allow the installation to proceed.

THIS WILL DEPLOY YOUR APPLICATION IN THE SERVER.

# RSA-Spring-Boot-Unikernel
RSA-Encryption Java Spring-Boot Application packaged as ".war"-File.

(Application running as "UniK"-Unikernel)

First of all: 
If the Application is running as a unikernel, the file has to be uploaded to the unikernel before the enrcyption.
This can be done via the OSv-Dashboard, with the REST-commands (File-upload).

1.) Get information about the application-commands:
http://instance-ip:8081/rsa-0.0.1-SNAPSHOT/encryption/getInformation

2.) Read a file from your unikernel-system:
Example URI: http://instance-ip:8081/rsa-0.0.1-SNAPSHOT/encryption/startProcess/File.Extension/PathToFile/
Explaination: "PathToFile" -> the user has to set the path to the file, which should be encrypted.

3.) Set the bit-range of the public-key:
Example URI: http://instance-ip:8081/rsa-0.0.1-SNAPSHOT/encryption/setBitRange/<value>

4.) Start the encryption of the file:
Example URI: http://instance-ip:8081/rsa-0.0.1-SNAPSHOT/encryption/startEncrypt

5.) Start decrypting the file:
Example URI: http://instance-ip:8081/rsa-0.0.1-SNAPSHOT/encryption/startDecrypt/PathToFolder/
Explaination: "PathToFolder" -> the user has to set the path to the folder, where the application should save the decrypted file.


# Audio-Video-Auth system
  - Introduction.
  - Problem Statement.
  - Solution Of The Problem.
  - Description.
  - Technologies used.
  - How we build It.
  - Conclusion.
<br>
<br>

**Introduction:**
<br>
<br>
  Authentication(Auth) is a process of validating a user by getting credential details which the user only knows. By which organizattion can provide details or services for the beneficiary of the user. There are many types of Auth system that were used from the era of computer's. But for every authentication there might be a loop which could lead to Access Control over the user's account or service. This will make a impact on privacy of the user and security of the organization. Due to improper authentication system, attacks like password or pin cracking, phishing, zero-day vulnerablity, etc..! are occurring in day-to-day life. So, Many alternative ideas have been developed by the organization to ensure the security and privacy of the end user. Some new authentication system's are based on biometrics, genetical, heart beat scanner authentication systems.
  
  Authentication systems like biometrics are validated without crendialal but validadted by users unique finger prints and retina. Each Human have a unique fingerprint and retina Which can be used as crendential's for the user's. there are also many bimetrics auth like Voice fingerprinting, Face recognition.
  <br>
  <br>
 **Problem Statement:**
 <br>
 <br>
  "Authentication measures of Caller ID / PIN (personal identification numbers) / Security Questions / Device Signatures are sometime inadequate and intrusive. Identify creative methods of Customer Authentication which can be used on various channels. This should be done without deteriorating the customer experience."
  
  By the above problem statement we came to the conclusion that Called ID/ PIN / Security Quetions / Device Signature are In-secure in modern Authentication system. And these are sometimes can be deteriorating to the customers experience. So, We want to find a alternative way.
  <br>
  <br>
**Proposed Solution:**
<br>
<br>
  In order to find a new way for authentication system we have found a simple and most efficient way using REST API in cloud. Like old school tech we have also used a simple way like PIN. But there will be Two-way auth. after entering the PIN our mobile app will send a POST request to our API server with data of Person's 180 degree video with Audio of the person. Then the data will be encrypted. Then the data will be validated by the backend Server.
  
  On Backend API server! We have used Python Audio Fingerprinting and multiple images of video. Before Login while registering the account we will fingerprint both audio and video of the user. For audio it will be fingerprinted by Python fingerprinting lib. And we have used our own algorithm to fingerprint the video.
  
  When those fingerprinting matches it will validate and produce a session for the user and encrypt the data. Then it will be delevired to the user and the session will be started.
  <br>
  <br>
**Description:**
<br>
<br>
  Our Authentication System is a isolated system where we cannot interept the request and change the response. We can't also upload and alterrated data to the rest API and get the session of the account. Only can be sent from our own software or mobile app. We have configured by the signature of the device with the REST API on the backend
  
<br>
<br>
**Technologies used:**
<br>
<br>
  - Dejavu = It is a Audio finger printing Lib used to memorize the audio file. we have used it to memorize the users Input and store the Audio file.
              - Docs: https://github.com/worldveil/dejavu 
  <br>  
  - MYSQL  = We haved used MYSQL for storing fingerprinted data of the audio. Our real plan is to store data in blockchain using 'Hyperledger'. In future case we will              impliment the blockchain in storing fingerprinting data
  <br>
  - face-recognition = We also used face recognition due to its optimized output. If we use ML based fingerprinting we need more number of power and time. Insted we                            can store a fingerprinted data and compare those data to validate.
              - Docs: https://pypi.org/project/face-recognition/
  <br>
  
  - flask = We have used flask for creating a REST full API to communicate with backend of the server. By usinig API in software build's we can optimize the                       performence of the app and high accurate results.
  <br>
  - Firebase = We have used Firebase for storing user's video fingerprinting data's.

<br>
<br>
**How we are going to build It:**
<br>
<br>
  We have to start from building the REST API structure. By creating routes for the API we can move to next part. We also want to config the Dejavu and Face recognition in different terminals so that we can do multiple task at a same time. Then we want to connect them with REST API. By connecting with that we can move to next part. 
  
  For Authentication and encryption we have made a signature for the APP and software using sha-256. and we will use to encrypt the data sending from the software to the backend server.
<br>
<br>
**Conclusion:**
<br>
<br>
  We conclude that the technologies we have used and tested are the best innovative and a futuristic way in the usage of a banking sector for their authentication system and data storing technologies.
  

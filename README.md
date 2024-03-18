# Outfits API
#
This is the backend api for the outfits Frontend React app. It contains the models and logic to allow the frontend application to perform CRUD operations.

#
* [Deployed Back-End page](https://outfit-backend-797953668660.herokuapp.com/)
* [Deployed Front-End page](https://outfit-ms-4ee7085bae68.herokuapp.com/)
#
## **Contents**
- [**Planning and Project Conception**](#planning-and-project-conception)
	    - [**Project Goals**](#project-goals)
	    - [**Site Goals**](#site-goals)
	    - [**Future Goals**](#future-goals)
	    - [**Agile Planning**](#agile-planning)
		        - [**GitHub Project Board**](#github-project-board)
		        - [**Github Issues**](#github-issues)
		        - [**ERD Plan for backend models**](#erd-plan-for-backend-models)
		        - [**API Endpoints**](#api-endpoints)
- [**Testing**](#testing)
	    - [**Manual Testing**](#manual-testing)
	    - [**Test cases**](#test-cases)
	    - [**Integration Testing**](#integration-testing)
	    - [**Code Validation**](#code-validation)
- [**Bugs**](#bugs)
	    - [**Bugs encountered during development**](#bugs-encountered-during-development)
- [**Technologies**](#technologies)
	    - [**Languages used**](#languages-used)
	    - [**Databases**](#databases)
	    - [**Cloud storage and deployment services**](#cloud-storage-and-deployment-services)
	    - [**Frameworks, tools and libraries**](#frameworks-tools-and-libraries)
		        - [API Back-End](#api-back-end)
		        - [REACT Front-End](#react-front-end)
	    - [**Installed Libraries and packages**](#installed-libraries-and-packages)
- [**Deployment**](#deployment)
	    - [Steps to set up and deploy the project:](#steps-to-set-up-and-deploy-the-project)
		        - [**Gitpod**](#gitpod)
		        - [**ElephantSQL**](#elephantsql)
		        - [**Environemental variables and settings.py**](#environemental-variables-and-settingspy)
		        - [**Heroku**](#heroku)
	    - [**Connect a Frontend app with the Backend API**](#connect-a-frontend-app-with-the-backend-api)
		        - [**API Heroku config vars settings**](#api-heroku-config-vars-settings)
		        - [**Axios library**](#axios-library)
		        - [**Steps to Fork the repository**](#steps-to-fork-the-repository)
		        - [**Steps to clone the repository**](#steps-to-clone-the-repository)
- [**Credits**](#credits)
	    - [Code Institute](#code-institute)
	    - [Resources for creating the rating field in post model:](#resources-for-creating-the-rating-field-in-post-model)
	    - [Bug fixes sources:](#bug-fixes-sources)

## **Planning and Project Conception**
### **Project Goals**

1. To use Django Rest Framework to create RESTful APIs for a Frontend Application.
2. To connect a frontend app to a backend api.

[Back to top](#)

### **Site Goals**
1. To build an API which contains models for frontend features for a social media site.
2. To convert django models into JSON by defining serialisers.
3. To use these models as the architecture for the custom components for the frontend app such as the Post component. 
4. To  set up authentication, permissions and url routing manage access to site features and actions.

### **Future Goals**
- To add the event model to the api to expand the possible features.

[Back to top](#)
#
### **Agile Planning**
#### **GitHub Project Board**

* This project was made using agile methodologies. Epics and user stories.

[Back to top](#)

#### **ERD Plan for backend models**
 * The plan for this project is based on the Code Institute Moments walkthrough project. 
 * Most of the models are the same except for the post model which has been customised to better suit the needs of the site owner and users.
 * Initial plans were to include an event model, but that has been assigned as a future feature to help focus on the minimal viable product of  the site. 

![Database]()

[Back to top](#contents)

#### **API Endpoints**
```
/
dj-rest-auth/login/
dj-rest-auth/logout/
dj-rest-auth/registration/
dj-rest-auth/password/change/
dj-rest-auth/token/refresh/
profiles/
profiles/<int:pk>/
posts/
posts/<int:pk>/
comments/
comments/<int:pk>/
likes/
likes/<int:pk>/
followers/
followers/<int:pk>/
```
[Back to top](#contents)

## **Testing**
### **Manual Testing**
- The outfits api was tested manually throughout development  using django rest framework. 
- API Endpoints and CRUD functionality was tested for each feature. 
- The API endpoints were also checked in the deployed site to see if they were working and checked throughout the frontend development to ensure front and backend integration.

### **Test cases**
Below are some test cases that were implemented throughout development to check correct functionality: 
- Check login/logout and registration functionality.
- Check that access to post, comments, profiles, followers and likes POST, PUT and DELETE Metods are restricted to authorised users. 
- Get methods are checked via api endpoints.
- Filter function was checked using keywords.
- POST method was tested for Posts, comments, likes and followers
- POST method for dj-rest-auth/registration/ to create a profile tested
- POST method for /dj-rest-auth/password/change/ to change password tested
- PUT mehtod for profiles/id, posts/id and comments/id tested
- DELETE method for posts/id, comments/id, likes/id, followers/id tested

[Back to top](#contents)

### **Integration Testing**
The outfits API has also gone through integration testing via testing the features on  the frontend site.

[Back to top](#)

### **Code Validation**
- The python code was monitored for errors and adjusted throughout development using the gitpod IDE problems tab.
- In the final code review, I opened all python files and corrected any problems that were left.
    - Only minor issues like blank line at end of file remained.
- The only issues I did not fix are the line too long warnings from the automatically generated settings.py variable which contains long strings. 
    - I left these strings intact rather than breaking them up into smaller strings for the sake of avoiding potential issues.



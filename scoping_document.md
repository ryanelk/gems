# TABLE OF CONTENTS
1. [INTRODUCTION](#introduction)
2. [USER JOURNEY](#user-journey)
   1. [Description of Usage Profiles (Stakeholders)](#description-of-usage-profiles-stakeholders)
   2. [User Journey](#user-journey-1)
3. [FUNCTIONAL DESCRIPTION](#functional-description)
   1. [Overview of Epics](#overview-of-epics)
   2. [Overview of User Stories](#overview-of-user-stories)
      1. [Onboarding and Installation](#onboarding-and-installation)
      2. [Information and Instructions for Using the App](#information-and-instructions-for-using-the-app)
      3. [Use in the Foreground Process](#use-in-the-foreground-process)
      4. [Receiving a Notification](#receiving-a-notification)
      5. [Accessibility](#accessibility)

# INTRODUCTION
GEMS is a notes app aimed at encouraging consistent creativity in bite-sized chunks. GEMS engages users by gamifying the logging of daily musings, small wisdoms, and observations and then presenting the user's own content back to them for their amusement.

The interaction points and user experience are mapped based on a user journey. The resulting requirements are assigned to “epics”, or descriptions of the requirements at a high level of abstraction. These epics describe the individual contact points and general functions throughout the process that are required for usage and acceptance of the app. In turn, the epics are used to derive the detailed requirements in the form of user stories (software requirements formulated in everyday language). Through this approach, the individual requirements are structured as they are incorporated in the development process.

# USER JOURNEY

## Description of Usage Profiles (Stakeholders)
The following key usage profiles and stakeholders are integrated in the user journey, or overall process, and described in their roles:

#### App User
All persons who use the app: Submit content, can browse and edit past content, are notified with their previous content.

## User Journey
App usage is divided into different phases, based their content submitted and time spent with the app. In each phase, persons are assigned motivations or requirements that meet their expectations of the app and guide them intuitively through the process.

![Figure 1: User Journey](user_journey.png "User Journey")

#### *Idea* phase
In this phase, a person decides to get more information about the app, in this case, its purpose and how it would suit the user specifically. The information should reassure the user that the app will work with them, even if they do not *feel* creative.

#### *Installation* phase
A person decides to download the app (Google Play Store) and, after the technical installation process, is given an introduction to the app the first time it is opened. In this introductory phase, app users are given an overview of the functionality (through hand-drawn cards); are asked for the necessary consent; and guided through the notification and other settings. Settings will include notification frequency and reminders to contribute (for now). 

#### *Usage* phase
The usage phase is subdivided into three main areas, with *User Background* requiring a certain threshold of user-generated content before activation.

1. **Content**

   User submits content which will be stored (based on date) and analyzed for categorizable information. User will also have ability to browse and search through submitted content for edits and removal.

2. **Background**

   User will receive local notifications reminding them to submit content. This will continue until the threshold to activate the *User Background* phase is reached.

3. **User Background**

   User will receive local notifications containing their submitted content once content threshold is reached. The frequency of these notifications will be determined by user at installation phase (and changeable later on in settings). The time at which these notifications are sent are determined by app.

#### *Uninstallation* phase
A person can uninstall the app at any time, completely deleting all the data stored in it.

# FUNCTIONAL DESCRIPTION

## Overview of Epics
The app functions are divided into user process phases (with direct ties to the user journey) and general support processes. An overview of the epics is depicted below:

#### Process Phases of Use
| # | Epic | Description |
|---:|--------|--------------|
| 1 | Onboarding and Installation | All processes that take place the first time the app is used (such as consent, data privacy, language selection) |
| 2 | Information and Instructions for Using the App | Help tools for using the app (such as user manual, tutorial), as well as publication information for the app |
| 3 | Use in the Foreground Process | App functions while in focus (such as submitting content, editing content) |
| 4 | Use in the Background Process | App functions in idle mode (such as receiving notifications, changing settings) |

## Overview of User Stories
The requirements GEMS must satisfy, and which define its functional scope, are formulated below in the usual format of a user story, unless specified otherwise:

_“As &lt;stakeholder&gt;, I want &lt;goal&gt;, so that &lt;reason&gt;.“_

The corresponding acceptance criteria supplement the specification of the requirements by defining the conditions that the software must fulfill to satisfy user needs..

### Onboarding and Installation
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E01.01 | As an app user, the first time I launch the app, I want to receive an introduction to how it works so that I feel that I understand the purpose and use of the app (app motivation). | 1. An introduction to how the app works is displayed the first time the app is launched. <hr/> 2. The introduction to how the app works is not displayed when the app is launched subsequently.<hr/>3. The explanatory content is available to app users in the respective functional areas. |
| E01.02 | As an app user, the first time I launch the app, I want to be notified about the terms of use and privacy provisions (data privacy screen) and grant my consent, so that I know how my data will be used within the app. | 1. By using the app, the user accepts the terms of use and privacy provisions.<hr/>2. The terms of use can be displayed within the app.<hr/>3. The consent prompt is shown only the first time a user launches the app. |
| E01.03 | As an app user, the first time I use the app, I want to be asked whether the application is allowed to send me local notifications, so that I can get notifications in a variety of situations. | 1. The app’s notification settings are queried before the app is used for the first time. This enables local notifications. <hr/>2. The prompt no longer appears after the first time the app is used but settings can be adjusted later in the app.|
| E01.04 | As an app user, I want the app to be displayed in my language the first time I use it, so that I can understand how to use the app. | 1. The configured system language is detected.<hr/>2. If the content is not available in the detected system language, English is selected by default.<hr/>3. The first version of the app is expected to be available also in languages other than English. |
| E01.05 | As an app user, I want to see help functions and settings for accessibility during the onboarding process, so that I can use the app. | 1. Accessibility is provided depending on the options available in the respective operating system. |

### Information and Instructions for Using the App
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E02.01 | As an app user, I want to have access to instructions, so that I can understand the app and its functions. | 1. An explanation of the app’s various functions will be provided. |
| E02.02 | As an app user, I want to be able to display publication information for the app, so that I can see who is responsible for development and content of the app. | 1. There is a “Publication information” item in the menu.<hr/>2. The publication information contains the usual information required. |
| E02.03 | As an app user, I want to be able to display the terms of use and data privacy information at any time, so that I feel reassured about my decision to use the app. | 1. The app provides simple access to the terms of use and data privacy information. |
| E02.03 | As an app user, I want to be assured that I am using the app correctly, so that I do not get discourage or intimidated from using the app. | 1. The app provides feedback for submitting content, indicating that user is taking the right steps, without specifically influencing the type of content user wishes to submit. . |


### Use in the Foreground Process
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E03.01 | As an app user, I want to be able to create and submit new content with ease, so that I can focus primarily on gathering my own thoughts. | 1. The UI will be straightforward and unobtrusive, with intuitive text entry area and submit button.|
| E03.02 | As an app user, I want to be able to control content, so that I can be comfortable with what I've put into the app and restart from scratch if I want to. | 1. The app can be reset to default with a format option, which will delete all content. <hr/>2. Saved content can be deleted in bulk through the edit menu. <hr/>3. Saved content can be edited or deleted through individual view of content. |
| E03.03 | As an app user, I want to be able to adjust the app settings (access permissions, such as notifications) in a menu, so that I can manage the app functions and accesses. | 1. App users can call a menu for app settings. <hr/>2. Notifications, both reminders and user-generated, can be activated and deactivated.<hr/>3. Before access permissions are deactivated, I receive information as to which app functions will no longer work (in full). |

### Receiving a Notification
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E04.01 | As an app user, I want to be able to respond to the notifications I receive, so that I can enact changes based on how it made me feel. | 1. Notification will lead user to app. If notification is a reminder, user will be led to creation page. If notification is user-generated content, user will be brought to edit screen where they can edit, react (for future notification settings), or delete.|
| E04.02 | As an app user, I want to be able to adjust notification frequency, so that I can change settings if it annoys me. | 1. The notification will open the app. From there settings can be reached so notification frequency can be adjusted. |

### Accessibility
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E05.01 | As an app user, I want to have good contrast settings, modifiable font sizes, and an easily readable font, so that I can read the texts in the app easily. | 1. Accessibility regarding contrast and font size/type is provided depending on the options available in the respective operating system. |
| E05.02 | As an app user, I want to have the content in simplified language, so that I can easily understand how to use the app and why I should use it. | 1. The texts and languages are defined by the ordering party. |

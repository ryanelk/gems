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
      3. [Use in the Regular Process](#use-in-the-regular-process)
      4. [Exposure (Contact with an Infected Person)](#exposure-contact-with-an-infected-person)
      5. [Notification of Covid-19 Test Results](#notification-of-covid-19-test-results)
      6. [Triggering a Warning](#triggering-a-warning)
      7. [Parameter Settings](#parameter-settings)
      8. [Technical Support](#technical-support)
      9. [Accessibility](#accessibility)
      10. [Content Management](#content-management)

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
| E01.01 | As an app user, the first time I launch the app, I want to receive an introduction to how it works (app motivation). | 1. An introduction to how the app works is displayed the first time the app is launched.<hr/>2. The introduction to how the app works is not displayed when the app is launched subsequently.<hr/>3. The explanatory content is available to app users in the respective functional areas. |
| E01.02 | As an app user, the first time I launch the app, I want to be notified about the terms of use and privacy provisions (data privacy screen) and grant my consent, so that I know how my data will be used within the app. | 1. By using the app, the user accepts the terms of use and privacy provisions.<hr/>2. The terms of use can be displayed within the app.<hr/>3. The consent prompt is shown only the first time a user launches the app. |
| E01.03 | As an app user, the first time I use the app, I want to be asked whether I consent to the creation of pseudonymized IDs and sending them to devices near me, so that I am informed about how the app works. | 1. Confirmation of the creation of pseudonymized IDs and their transmission to nearby devices by the app is a prerequisite for using the app.<hr/>2. The prompt no longer appears after the first time the app is used. |
| E01.04 | As an app user, the first time I use the app, I want to be asked whether the application can access the smartphone’s Bluetooth function, so that I can control how the app is used on the smartphone. | 1. This user story is tantamount to E01.03. The authorization to use the generation of pseudonymous IDs and send them to nearby devices is already contained in the usage of Bluetooth Low Energy (BLE).<hr/>2. The configuration of the general Bluetooth functions is only possible in the system settings. |
| E01.05 | As an app user, the first time I use the app, I want to be asked whether the application is allowed to send me notifications, so that I can get notifications in a variety of situations. | 1. The app’s notification settings are queried before the app is used for the first time. This enables local notifications. True push notifications from external servers are not supported (APNs/FCM). <hr/>2. The prompt no longer appears after the first time the app is used. |
| E01.06 | As an app user, I want the app to be displayed in my language the first time I use it, so that I can understand how to use the app. | 1. The configured system language is detected.<hr/>2. If the content is not available in the detected system language, English is selected by default.<hr/>3. The first version of the app is expected to be available also in languages other than English. |
| E01.07 | As an app user, I want to see help functions and settings for accessibility during the onboarding process, so that I can use the app. | 1. Accessibility is provided depending on the options available in the respective operating system. |

### Information and Instructions for Using the App
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E02.01 | As an app user, I want to have access to a FAQ list, so that I can find answers to questions I might have about the app. | 1. The app will either contain a link to a web page with FAQs, which is displayed in a browser window, or the web page will be displayed within the app itself. |
| E02.02 | As an app user, I want to have access to instructions, so that I can understand the app and its functions. | 1. An explanation of the app’s various functions will be provided. |
| E02.03 | As an app user, I want to have access to an explanatory video, so that I can understand how to use the app and its functions. | 1. An explanation of the app’s various functions will be provided. |
| E02.04 | As an app user, I want to be able to display publication information for the app, so that I can see who is responsible for development and content of the app. | 1. There is a “Publication information” item in the menu.<hr/>2. The publication information contains the usual information required. |
| E02.05 | As an app user, I want to be able to display the terms of use and data privacy information at any time. | 1. The app provides simple access to the terms of use and data privacy information. |
| E02.06 | As an app user, I want to be able to see various hotlines for technical, privacy-related, health-related, and psychological questions, as well as for verification of test results, so that I can receive further information or answers to my questions. | 1. The app offers access to a technical hotline and a hotline for obtaining a phone TAN.<hr/>2. The times the hotline is available (such as 24/7) is displayed.<hr/>3. Phone numbers can be called directly from the app. |

### Use in the Regular Process
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E03.01 | As an app user, I want to be able to activate and deactivate the app, so that I can switch the functions on and off. | 1. The functions for generating pseudonymized IDs and sending them to nearby devices can be activated and deactivated. <hr/>2. The consequences of activation/deactivation are explained. |
| E03.02 | As an app user, I want to be able to reset to the app to the delivery defaults, so that I can reconfigure it. | 1. The app can be reset to the delivery defaults with a setting option. The saved traces have to be deleted through the system settings. |
| E03.03 | As an app user, I want to be able to adjust the app settings (access permissions, such as notifications) in a menu, so that I can manage the app functions and accesses. | 1. App users can call a menu for app settings. <hr/>2. Notifications can be activated and deactivated.<hr/>3. Access to the functions for generating pseudonymized IDs and sending them to nearby devices can be activated and deactivated.<hr/>4. Before access permissions are deactivated, I receive information as to which app functions will no longer work (in full). |

### Exposure (Contact with an Infected Person)
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E04.01 | As an app user, I want to be notified when a person I have had contact with has reported an infection, so that I can then take the appropriate measures to stop the spread of the virus. | 1. Depending on the notification settings, the app sends a notification to the user.<hr/>2. If the risk assessment for a user changes, a notification informs users that there is news in the app. The actual changed risk assessment is not displayed until the app is opened. |
| E04.02 | As an app user, if I am exposed to the virus, I want to receive instructions from the app, so that I can adapt my behavior to RKI recommendations. | 1. A notification leads the user to the app. The recommendations from the RKI are defined statically in the app. |

### Notification of Covid-19 Test Results
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E05.01 | As the RKI, I want only positive tested users to trigger a one-time warning, so that I can prevent misuse. | 1. Only positive tests can trigger a warning. This is ensured by the verification server and the hotline for the phone TAN procedure.<hr/>2. A warning can only be triggered once for each test. |
| E05.02 | As an app user, in case of a positive test result, I want to receive information about the illness and the necessary next steps, so that I can adapt my behavior to RKI recommendations. | 1. A notification merely informs you that there is news in the app. The test result itself can only be seen in the app. <hr/>2. An info text with defined content is displayed in the app (for example, information about the outcome of the test result, information about necessary measures, a hotline number). |

### Triggering a Warning
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E06.01 | As an app user, I want to be able to scan a QR code provided by a medical professional or test center, so that I can receive my test result in the Corona-Warn-App. | 1. A QR code provided on a flyer from the medical professional or test center can be scanned with the Corona-Warn-App.<hr/>2. An explanatory text is displayed. |
| E06.02 | As an app user, I want to be notified within the Corona-Warn-App as soon as a test result becomes available. | 1. A notification merely informs you that there is news in the app. The test result itself can only be seen in the app.<hr/>2. The notification does not explicitly indicate whether the result is positive or negative. |
| E06.03 | As an app user, if I receive a positive test result, I want to be able to grant my consent to sending the pseudonymized IDs under which I was visible to other people in recent days to the Warn server, so that the people I have been in contact with can be warned by their apps. | 1. The IDs can be sent to the Warn server pseudonymized.<hr/>2. Data transmission is only possible if successfully verified beforehand. This is ensured by the verification server and the hotline for the phone TAN procedure.<hr/>3. Data transmission is only possible if the app user has granted consent beforehand. |
| E06.04 | As an app user, I want to be able to use a manual process (in addition to the digital process), for example, through a call center and without a QR code, to send the pseudonymized IDs under which I was visible to other app users in recent days, to the Warn server, so that the people I have been in contact with can be warned by their apps. | 1. The center responsible can generate a TAN and provide it to the person. (The TAN is generated by a server, not the call center itself.) |
| E06.05 | As an app user, I want to be able to enter a TAN in the app, so that I can use the TAN I have been given to assign my test result to my instance of the app. | 1. It is possible to enter a TAN within the app.<hr/>2. The app verifies the entered TAN and provides feedback as to whether it was correct (must be checked whether technically possible). |
| E06.06 | As an app user, after the TAN is verified, I want to share my pseudonymized IDs voluntarily, so that I can warn persons I may have been in contact with. | 1. The IDs can be sent to the Warn server pseudonymized.<hr/>2. Data transmission is only possible if successfully verified beforehand. This is ensured by the verification server and the hotline for the phone TAN procedure.<hr/>3. Data transmission is only possible if the person has granted consent beforehand. |

### Parameter Settings
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E07.01 | As the RKI, I want to be able to configure the parameters (to the extent the API is able to do this) for risk scoring, so that I can keep up with the latest research findings on virus transmission. | 1. Thresholds can be configured dependent on the provided API.<hr/>2. The app receives dynamic configurations from the RKI that can affect how the risk assessment is calculated. |

### Technical Support
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E08.01 | As an app user, I want to be able to contact a hotline, so that I can resolve any technical problems with the app. | 1. The phone number of the technical hotline is stored in the app. |

### Accessibility
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E09.01 | As an app user, I want it to have audio output, so that I can use the app even if I have impaired vision (or am blind), for example. | 1. Accessibility regarding audio output is provided depending on the options available in the respective operating system. |
| E09.02 | As an app user, I want to have good contrast settings, modifiable font sizes, and an easily readable font, so that I can read the texts in the app easily. | 1. Accessibility regarding contrast and font size/type is provided depending on the options available in the respective operating system. |
| E09.03 | As an app user, I want to have the content in simplified language, so that I can easily understand how to use the app and why I should use it. | 1. The texts and languages are defined by the ordering party. |

### Content Management
| # of user story ID | User story | Acceptance criteria |
|-----------------|------------|--------------------|
| E10.01 | As the RKI, I want to manage the app content centrally, so that I can update texts, links, hotlines, and so on once for all the places in the app. | 1. Content management will be carried out based on RKI requirements.<hr/>2. Content will be differentiated by static and dynamic content, in line with technical feasibility.<hr/>3. In the initial version, updates will be performed through an app update. |

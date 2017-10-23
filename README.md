# Vocabulary-Pusher
A Cross-Platform Gear Aim to help Memorizing Vocabularies
![](https://github.com/tomy0000000/Vocabulary-Pusher/blob/bff650dcf768cb22fb57a95e9a38e788d02977eb/Display%20Pics/Notification.gif?raw=true)

# Introduction
During the months I'm studing for AST Exam, I find it uncomfortable to sqeeze my time out just to memorize more useless vocabluaries. Therefore, I develope these script to help me memorize in a more effective way.

# Installation Guide
## On iPhone
* Install [`IFTTT`](https://itunes.apple.com/app/id660944635) and Setup
	1. Cresate a new Applet
	2. If `Webhooks` -> `Receive a web request`
	3. Event Name: `Vocabulary`
	4. Then `Notifications` -> `Send a notification from the IFTTT app`
	5. Notification: `{{Value1}} {{Value2}} {{Value3}}`
	6. Activate This Applet

* Install [`Workflow`](https://itunes.apple.com/app/id915249334) and Setup
	1. Download and install [`Vocabulary Pusher Appender.wflow`]()
	2. Download and install [`Vocabulary Pusher Archiver.wflow`]()
	3. Download and install [`Search Vocab.wflow`]()

## On Mac
1. Install [`Keyboard Maestro`](https://www.keyboardmaestro.com/main)
2. Install Action [`Send to IFTTT`](https://www.keyboardmaestro.com/main/third-party-actions#SendToIFTTT)
3. Install Macro [`Vocabulary Pusher.kmmacros`]()
4. Get Your IFTTT Key at [`Webhooks`](https://ifttt.com/maker_webhooks) -> `Documentation`
5. Open `Keyboard Maestro Preferences` -> `Variables` and add a new variable named `VP_IFTTTKey` with your IFTTT Key paste in as value
6. Make sure `Keyboard Maestro Engine` is added in Login Item

# Documentation
## To Add Vocabularies...
### On iPhone
1. Run `Vocabulary Pusher Appender` Workflow on iPhone
2. Fill `Key` with English, `Text` with Chinese
3. Add new `Text` item to append more vocabularies at once

### On Mac
Edit `~/Dropbox/Workflow Automation/Vocabulary Pusher/List.txt` directly with following rules:

* One Line for each Vocabulary
* One Tab to seperate English and Chinese

## To Archive/Remove Vocabularies...
### On iPhone
1. Run `Vocabulary Pusher Archiver` Workflow on iPhone
2. Check the Vocabularies you want to archive
Note: When Archive with iPhone, Vocabularies will be saved into `~/Dropbox/Workflow Automation/Vocabulary Pusher/Archive.txt`

### On Mac
Simply Remove Vocabularies from `~/Dropbox/Workflow Automation/Vocabulary Pusher/List.txt`

# If you need to...
## Adjust the Notification Frequency
Simply edit the Macro trigger in `Keyboard Maestro Editor`

## Adjust the Number of Vacbularies Sent Each Time
Simply edit the `Repeat Action Time` in the 5th action of the Macro

## View Vocabulary Pushing History
Check `~/Dropbox/Workflow Automation/Vocabulary Pusher/History.txt`

## View Archived Vocabularies
Check `~/Dropbox/Workflow Automation/Vocabulary Pusher/Archive.txt`

Note: Vocabulary won't be recorded if it was removed manually from Mac

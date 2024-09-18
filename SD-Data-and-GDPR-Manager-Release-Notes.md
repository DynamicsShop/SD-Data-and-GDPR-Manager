## SD Data and GDPR Manager Releases

### 3.1.2

#### Enhancements

- AppSource App - User Groups are retired in 2024 release wave 2 and are replaced with Security Groups. The Rule Card was updated to use Security Groups.

- AppSource App - A change was made to the Assisted Setup functionality.

- AppSource App - The links in the About page were updated.

- AppSource App - The logo in the App was updated to the new logo.

### 3.1.1

#### Enhancements

- AppSource App - AppSource App - A notification was added to SD Data and GDPR Manager pages to show users that they need to activate the licence on first install of the App.

- AppSource App - A change was made to limit the SD ISV Tenant Subscriptions page to display just our SD ISV AppSource Apps and not other SD PTE Apps.

#### Bug Fixes

- AppSource App - An error was raised on encryption of fields that "A call to System.Security.Cryptography...failed with this error message...". SD Data and GDPR Manager was using block size of 256 this has been restricted to 128 by Business Central in BCv22.

- AppSource App - A change was made to the ISV Licence Notification procedure in SD Data and GDPR Manager to fix an issue that would raise an error when the language is changed from English to another language.

- AppSource App - An error will raise in the Assisted Setup import if non sequential enum values exist in the imported data. This was fixed.

- AppSource App - When selecting SD Data and GDPR Manager activity pages in the Tell Me/Search in a BCv22 environment, the activity pages were hanging.

### 3.1.0

#### Enhancements

- BCv21 App - Added the Latest ISV Licence Control to SD Data and GDPR Manager.

- BCv21 App - The Product Activation Page was updated to point to the new CRM URL.

- BCv21 App - The Licence Expiry message/notification was updated to display the App Name as part of the message.

- BCv21 App - A page was created to display all the Simply Dynamics Apps and subscription details for the tenant.

- BCv21 App - The Licence Message displayed on first install of SD Data and GDPR Manager was changed to prompt the user to activate a free trial and to choose Assisted Setup from the Setup Card to create demo data.

- BCv21 App - The links in the About Page were updated to point to new URLs.

- BCv21 App - The ToolTips were updated to look at our new website.

- BCv21 App - The SD Data and GDPR Manager Permissions XML file was replaced with AL permission objects and the names were standardised to our ISV format.

#### Bug Fixes

- BCv21 App - A fix was made to the code for licence key checks on the SD Data and GDPR Manager Role Centre. 

### 3.0.1

#### Enhancements

- BCv19 App - Added the Latest Version of the product and the AppSource URL to the About Page. 

- BCv19 App - Added the Latest ISV Licence Control with fix to Free Trials in Public Environments. 

#### Bug Fixes

- BCv19 App - The Product Activation page was updated to disable the Activate button until a Product Key is filled in. This will avoid an error being raised when Activate is chosen with no Product Key entered. 

### 3.0.0

#### Enhancements

- The message on the prompt to confirm records were exported to a file was updated. 

- The encryption block size was set back to it's original 256 length.

- When choosing the Product Activation action the user is prompted that they need to ensure they have allowed HttpClient Requests in Extension Settings.

- Code was rechecked to ensure that the Licence Expiry Date prompts with 5 days to go is not stopping users from using the product but is only prompting the users. 

- Reverted the change where key for encryption was stored as a separate key for each company. The encryption key passphrase is now stored across the whole product and the action on the Setup Card to allow users import their own encryption key is now removed.

- The key for encryption is now stored as a separate key for each company and not as one key for the product. 

- The order of the Activity Groups in the Role Centre was changed. 

- A change was made to the flowfield count calculation on the GDPR Inactive Monitored Tables Cue. 

- The Ignore option in the On Failure field on the Rule Card was removed as there is now a Disable Flag on the Card. 

- The Assisted Setup and the About actions were removed from the Action menu in the Rules list. 

- A number of Actions were removed from the Role Centre to free up space and the caption on one of the Activity Groups was updated. 

- As per our other products, the Activity Groups in the Role Centre are now searchable in the Tell Me. 

- Visual changes were made to the Rule Card - the Disabled field was re-captioned to Disable and the actions were changed. 

- The Activity Groups on the Role Centre were split out to individual pages and a new SD Data and GDPR Manager Activities - GDPR Data Management activity group was created. 

- The grouping of the Actions in the SD Data and GDPR Manager Monitored Tables Card was changed. 

- Pages were re-captioned from SD Data Manager to SD Data and GDPR Manager. 

- The Activity Groups on the Role Centre were split out to individual pages and a new SD Data and GDPR Manager Activities - GDPR Right To activity group was created. 

- The Activity Groups on the Role Centre were split out to individual pages and a new SD Data and GDPR Manager Activities - GDPR Requests activity group was created. 

- Export Encryption Key and Import Encryption Key actions were surfaced on the Setup Card.  

- Encryption was changed in this BCv17 release to AES 128 bit. Previous code bases (including BCv14 had AES 256 bit encryption). This will have implications for upgrading from earlier versions of SD Data and GDPR Manager. Encrypted data will have to be unencrypted prior to upgrade. 

- An identifier was added to the GDPR Right to Page to indicate the type of request that is being run. 

- The caption on the GDPR Request page was updated to reflect the name of the product. 

- A change was made to the GDPR Monitored Tables list to auto-refresh the Fields count flowfield when users exit the Monitored Tables card. 

- Visual changes were made to the GDPR Monitored tables list and the page was recaptioned.  

- A number of visual changes were made to the Setup Card. 

- Assisted Setup was added to the product. 

- Object Captions were updated to allow the product to be translated if needed.  

- Permission sets were added to the product. 

- Visual changes were made to the Role Centre and to the Activity Groups. 

- A change was made to the placement of the licensing prompt in the product. Users are now prompted to validate the licence on the Setup, on the Rule list and on the GDPR Request list. 

- A disable boolean flag was added to the rule setup card to allow rules to be created but not yet applied or invoked. 

- A change was made to remove the hardcoded value of * on data that is encrypted due to an Encryption Request. This is now a variable on setup that allow the users to define a different encryption marker. 

- A change was made to remove the hardcoded value of Removed from data that is erased due to an Erase Data Request. This is now a variable on setup that allow the users to define a different erase marker. 

- The code base was ported to D365 Business Central v17 and the product was prepared for AppSource submission. 

- The order of the menu Action Groups on the GDPR Request page was changed. 

- An SD Data Manager Customer Demo page was created to show users how encrypted data can be viewed using two function calls. 

- The captions of the pages were updated to reflect the name of the product, SD Data and GDPR Manager. 

- The usage category on pages was updated to allow users to search for SD Data and GDPR Manager pages in the Tell Me. 

- A Role Centre was created for the product. 

- Licensing Activation was added to the product. 

- The name of the App and the App file was changed to reflect our standard product naming conventions.  

#### Bug Fixes

- A fix was made to the issue where automatic encryption on a table was not consistently firing.

- An issue was fixed where users were unable to remove and delete tables from the GDPR Monitored list.  

- A change was made to fix the AL message raised when the GDPR Request action in the GDOR Requests page was chosen. 

- The correct URL was added to the About page. 

- The Name and Description fields in the product were increased from 50 to 100 characters in length as per standard Dynamics 365 Business Central.  

### 2.4.5

#### Enhancements

- BCv14 Private App - A German translation layer was added to the product. 

- BCv14 Private App - The product activation/licensing feature was added to the product.

- BCv14 Private App - Fixed report.

#### Bug Fixes

- BCv14 Private App - Fixed an issue where users could encrypt an already encrypted field.

- NAV 2018 - Fixed an issue in the web client where an error was raised when exporting a portability file.

- NAV 2018 - Fixed an issue where users could encrypt an already encrypted field.

- NAV 2016 - Do not allow users to encrypt an already encrypted field.

- Fixed an issue where SD Data Manager and GDPR was creashing when selecting an extension table.

### 2.4.4

#### Enhancements

- BCv14 Private App - Converted the NAV 2018 objects to AL extensions in BCv14 Private App.

- NAV 2018 - Included the sample data and help files with the NAV 2018 release.

- NAV 2018 - Fixed a compile issue on the SD-UD GDPR Demo Customer List in the NAV 2018 objects when compiled in a D365BC v14 development environment.

- NAV 2018 - Updated the table relation from Object Table to AllObjWithCaption in the NAV 2018 code base.

- Converted the NAV 2016 C/AL code base to NAV 2018 C/Al.

### 2.4.3

#### Enhancements

- Made a change to refresh the User Group Name on selection of User Group.

- Made a change to validate the User Group Name into the field on the Data Manager Rule Card when a User Group is chosen.

- Added new functionality to allow for field level security.

#### Bug Fixes

- Fixed an issue where the field level security check was firing if the field was not modified.

### 2.4.2

#### Enhancements

- Included table 124 to the list of tables that can be modified when using a customer licence.

- GDPR - Made a change to allow modification of "archive" tables when using a customer licence. Archived tables that can be modified using the GDPR functionality are Sales Shipment Header (T 110), Sales Invoice Header (T 112), Return Receipt Header (T 6660), Sales Cr.Memo Header (T 114), Purch. Rcpt. Header (T 120), Purch. Inv. Header (T 122) and Purch. Cr. Memo Hdr. (T 124).

### 2.4.1

#### Enhancements

- Created new sample data. 

- Fields on related tables were not always displayed when editing the related table as filters were being set differently.

- Removed/Hid the standard NAV OneNote, Notes and Links from Setup pages.

- Added our standard About Action to the Setup Pages - Data Manager Rules List and the GDPR Table List - and to the GDPR Request List.

- Made a change to the erasure and encryption logic for reference fields. A message is raised that references will be broken on erasure or encryption of related fields.

- Updated the Readme file. 

- Included the updated Readme file in the release.

- Issued a new release of objects for SD Data Manager GDPR NAV2013R2.

- Created a wrapper for File Management Code unit functions that are used by the export manager to eliminate NAV version dependencies.

- Created a Wrapper function for NameValueBuffer AddEntry.

#### Bug Fixes

- Fixed an issue where deleting a primary table was not cleaning up related tables, fields and restrictions.

- Fixed an issue where fields on related tables were not always displayed when editing the related table.

- Fixed an issue in the import setup.

- Fixed an issue when importing data in the NAV 2013R2 release.

- An update was made to the sample data in the Data Manager GDPR Setup.zip file.

- In the Sample Data files for build 2013R2+ and 2016+ the restricted data fields in table 43006110 for field no 50000 were removed. 

- Fixed an issue in the NAV 2013R2 release where an error was raised when the 'New' Acton on the GDPR Tables List was chosen.

- Fixed an issue in the NAV 2013R2 release where an error was raised when assigning a restricted field value for a field of type option.

- Fixed a compile error in the NAV 2013R2 release in a NAV2013R2 database.

- Fixed a compile error in the 2013R2 release.

- Fixed an issue where the restricted value for a field type of option could not be set in a NAV 2015 database.

- Fixed a compile error in the NAV 2013R2 release in a NAV2015 database.

- Fixed an issue in the erasure request.

- Fixed an issue whereby you could not re-enable disabled related tables.

### 2.4.0

#### Enhancements

- The Activity Cue Groups were split out into individual pages.

- Reviewed and updated the Readme.md file.

- All references to Cebuella were removed from the SD-UTDM objects.

- Update made to the sample data in the Data Manager GDPR Setup.zip file.

- The help.zip web help files were added to the release package.

- A new function was created to allow creation of a new request from a previous request. The user is allowed to select the request type.

- Changes were made to the GDPR activity structure and workflow.

- Added functionality to cater for occasions where a GDPR request results in records returned with common details for distinct unrelated entities.

- Added structural changes and functionality changes to the GDPR Request Card.  Allow users to resend a report.

- Updated the page actions and labels on the GDPR Request List to reflect the cues on the GDPR Activity Cue.

- GDPR - modified the filter set on the Activity Cues.

- GDPR - added an Activity Que.

- GDPR - Added the contact information to the request.

- The Readme was updated to include the GDPR functionality.

- Modified the GDPR functionality to allow for nested related tables.

- Added the Simply Dynamics ISV Import/Export functionality to SD Utilities - Data Manager and GDPR.

- Created GDPR Request Workflow functionality.

- Created Right to Encryption functionality for SD Utilities - Data Manager GDPR.

- Created Right to Portability functionality for SD Utilities - Data Manager GDPR.

- Created Right to Restrict functionality for SD Utilities - Data Manager GDPR.

- Created Right of Erasure functionality for SD Utilities - Data Manager GDPR.

- Created a Right of Rectification functionality for SD Utilities - Data Manager GDPR.

- Created a Right of Access Report for SD Utilities - Data Manager GDPR.

- Created a Right of Information Report for SD Utilities - Data Manager GDPR.

- Created a Decryption Module for SD Utilities - Data Manager GDPR.

- Created an Encryption Module for SD Utilities - Data Manager GDPR.

- Created the GDPR Track Field Table and associated Pages.

- Created the GDPR Track Table and associated Pages.

- Added GDPR functionality to SD Utilities - Data Manager.

#### Bug Fixes

- Fixed an issue with the Data Manager Rules Demo Data import.

- Fixed an issue where a false item was returned on an Encrypted Record.

- Fixed an issue where automatic encryption was set for a table but the records were not automatically encrypting.

- GDPR - fixed an error raised on upload of the GDPR Demo Import.

- Fixed an issue where, when setting a request to complete, the related search records were not being stamped with the closure details.

- Fixed an issue where the State on results was not editable.

- Fixed an issue where if one record was encrypted for a table, the search was not extending to search for potential results that might be decrypted.

- Fixed an issue where a Right to Access Request was marked as Complete and the Completed By and Completed At fields were not updated.

- Fixed an issue where "The filter is not valid for the field" error was received when running a Right to Information Request on a date field.

### 2.3.2

#### Enhancements

- Data Manager: Made an enhancement to allow specified users to bypass Data Manager Rules.

### 2.3.1

#### Enhancements

- Linkbox: 

- Add a setup field to specify document checkout to a default Drop Point check out path.

### 2.3.0

#### Enhancements

Linkbox: 
- Created check in/check out functionality for Linkbox Version Control. 

- Added Edit Permission to Linkbox. 

- Cleaned up code. 

Launch: 
- Upgrade Launch to use Control Suite.

#### Bug Fixes

Linkbox: 
- Fixed Error Message raised when viewing a file in the Drop Point or Versions List. 

- Fixed situation where the View Option was always displaying the same file.

### 2.1.2

#### Enhancements

- Updated readme.txt file. 

- Launch - applied Launch standardised document layouts to the Posted Purchase receipt report.

- Linkbox - enhanced Linkbox file overwrite confirmations.

#### Bug Fixes

- Linkbox - fixed a bug in the scrolling functionality when selecting an Icon for a Drop Point in the Drop Point Card. 

- Linkbox - fixed an issue where when choosing to Edit certain files from the Dropped Files Factbox an error is raised. 

- Linkbox - fixed an issue where Delete Permission on Dropped Files Fact Box not taken into account when you right-click on the Dropped Files Fact Box.

- Launch - fixed alignment issue on the SD-U Customer Payment Receipt Document.

### 2.1.1

#### Enhancements

- Linkbox - enhanced the Icon Scoller picker.

- Linkbox - enhanced the Template functionality - allow users to choose to push out the Templates to the Linked tables and select the template they want to attach to the records. 

- Launch - surface filters on SD-U Bank Acc. Recon. Stmt Document. 

- Launch - surface filters on the SD-U Bank Acc. Recon. Smt Test Document. 

- Launch - improvement in code to allow for barcode record type value. 

- Launch - optimised the image preview generation. 

- Launch - surfaced the newly added Documents to the Role Center. 

- Launch - applied Launch standardised document layouts to the SD-U Customer Payment Receipt Document.

#### Bug Fixes

- Launch - fixed alignment issue on SD-U Sales Return Order Document. 

- Launch - fixed alignment issue on SD-U Purchase Return Order Document.

- Launch - changed the Launch Documents to use the document currency code rather than customer/vendor currency code when deciding the bank details to use on the footer.

- Linkbox - fixed a bug in the auto linking functionality of a Template File to a record.

- Linkbox - fixed a bug in the Version History of Dropped Files Linked to a record. 

- Linkbox - fixed a bug in the Version History of auto-created Template Files. 

- Linkbox - fixed a bug where an error was raised on creation of a new record when a Drop Point (with Versioning turned on) is added to a Card Page. 

- Linkbox - fixed a bug where the Icon Scroller images were not updating. 

- Power BI - fixed an issue where the Return Sales Order as raising an error if there was no BI Setup.

### 2.1.0

#### Enhancements

Launch: 
- All Launch Documents and Reports underwent a code clean up. 

- A Delivery Docket was added to Launch. 

- A Manifest Report was added to Launch. 

- A Bank Account Reconciliation Statement (Posted Entries) was added to Launch. 

- A Bank Account Reconciliation Statement (UnPosted Entries) was added to Launch.

- A Stock Take Report was added to Launch.

- A Sales Return Order was added to Launch.

- A Purchase Return Order was added to Launch. 

- A Balance Forward Statement was added to Launch. 

- A standardised layout was applied across all Launch Documents and Reports. 

- All Field Names and abbreviations were standardised. 

- Decimal formatting was standardised across all Launch Documents and Reports. 

- A new Footer totalling layout and a VAT Grid layout was applied and standardised across the Launch Documents. 

- Positioning of Logos was made consistent across all Launch Documents and Reports. 

- A standard Header and Footer layout and banner, for portrait and landscape layouts, was applied across all Launch Documents and Reports. 

- An enhancement was made to allow users to choose the Background and Foreground Header and Footer Banner Colours that would print on all Launch Documents and Reports using a Colour Picker.

- Enhancements were made to the Remittance Advice Reports in Launch. Captions were changed, fields were resized. 

- Functionality to define and display a Barcode on all Launch Documents and Reports was added to Launch. 

- A Report Info Box was applied to the layout of all Launch Documents and Reports.

- Functionality was added to allow users to dynamically add the fields to print in the Report Info Box. 

- Minor layout changes were made to existing individual Launch Documents and Reports.

- New functionality was added to allow users to select the Background and Foreground Header and Footer Banner Colours by using a colour picker. 

- Improved the resolution of the Report Info Box. 

- Fields and FastTabs for new functionality were added to the Launch Setup Card.

Linkbox: 
- New functionality added to Linkbox to Security Filter Tables and Pages enabling permissions to be set. 

- Updated the Linkbox Setup to include Security Filters.

- New Security Filters for Dropped Files applied. 

- New Security Filters for Drop Areas applied.

- Added Company to membership lookup in Linkbox Security Filters. 

- New Version Control functionality added to Linkbox. 

- Provided Version Edit functionality. 

- When viewing a file in the Drop Area, the file is set to read only. 

- Coded increments for Dropped File Entry No. 

- Created a new Table and Page to list, and provide, Dropped File Version functionality. 

- Created Template functionality for Linkbox.

- Changed functionality to retain the SD Linkbox - Orphan Link Files. 

Profiler: 
- An XMLPort was created to export and import Profile Select List. 

PowerBI: 
- Added Sales Quote Tracking Functionality to PowerBI. 

- Added functionality to provide for CSV Import/Export for BI Date data. 

- Added the PowerBI Setup Page to the SD Utilities Role Centre

#### Bug Fixes

Launch: 
- Fixed bug where the Statement report overwrites any Date Filters that are passed into the report. 

- Fixed bug where colour choices picked using the colour picker were being re-set. 

- Fixed bug where the QR Barcode was not displaying correctly in the Report Information box. 

- Fixed bug in the Launch Report Setup whereby when a new record was added to the Report Info Box Fields for a specific report, the Field No. was not appearing in the order as specified but rather in the order as input. 

- Fix was made to the barcode generation to display as per Launch Report Setup. 

- Minor layout changes were made to existing individual Launch Documents and Reports.

- Fixed bug which allowed a Barcode to be setup on the Launch Report Setup with a DPI of zero. 

- Fixed bug where the List of Reports showing in the Launch Setup was being hard code filtered on an earlier version release. 

- Fixed bug where the InfoBox and Barcode were not being updated. 

Linkbox: 
- Drop Point Icons on List Pages are intermittently not displaying when the List Page is loaded from within the Role Centre.

- Fixed bug where a link is being created to records with no file attached when a record for a Template File that has no File Imported (a blank Filename field) is created. 

- Fixed error raised when an empty file is dragged and dropped into a Drop Point.

Profiler: 
- Remove irrelevant Actions from the Profile Selection List.

### 1.1.0

#### Enhancements

- Linkbox - created XMLPorts for Upgrade to NAVW19.00 - V2.1.0 

- Profiler - created Profiler Date export 

- Power BI - created BI Date XML PortXML Port

#### Bug Fixes

- Launch - fixed bug where statement report overwrites passed in Date Filter

### 1.0.2

#### Enhancements

- Linkbox - Drop Area was not displaying on the Role Center.

- Launch - Unable to run statement when specified from report selection.

### 1.0.1

#### Enhancements

- Documentation fixes.

- Linkbox - Created an XmlPort for setting up control Add-in. 

- Profiler - Refactored the object selection. Rewrote the reports to loop on the questions and do basic formatting of them. 

- Profiler - Renumbered and reordered the Tables and Pages. 

- Cleaned up the objects. 

- Code upgraded to 2016.






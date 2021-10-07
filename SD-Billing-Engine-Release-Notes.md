## SD Billing Engine Releases

### 3.0.0

#### Enhancements

- A Tool Tip was added to the Item Code on the SD Billing Engine Recurring Lines to let the user know that Item No. must be of Type Service.

- A Tool Tip was added to the Item Code on the SD Billing Engine Billing Element Codes to let the user know that Item No. must be of Type Service.

- When enabling the various elements on the Setup checks are made for required fields.

- In the Activity Lines page a change was made so the Item Ledger Entry Source Entry No cannot be updated in Edit Mode.

- Improvements were made to the grouping activity lines functionality on the Suggested Billing lines.

- A previous change to the contents of the source description in the Activity Lines list was reverted to as he functionality was before - showing the filters that were used to get the entry.

- The SD Billing Engine Manual Lines list was updated to allow users to search for the page in the Tell Me as per the pages caption.

- A minor typo fix was made on the Active Contracts list.

- A minor typo fix was made in the SD Billing Engine Setup Card.

- Update the SD Billing Engine External Units of Measure and the SD Billing Engine Activity Advanced Setup pages to allow users to search for these pages in the Tell Me.

- Two flowfield fields on the SD Billing Engine Setup Card were recaptioned. 

- A small typo was fixed on the Recurring Contract Card.

- Allow users to drill down on the Unposted Invoices from the Contract Detail FactBox in the Active Contracts list.

- In the Activity Advanced Setup the Billing Description is now editable as the same Billing Codes can be used several different times for different purposes.

- A minor typo fix was made to the Assisted Setup message prompt.

- The URL for the Learn More in the SD Billing Engine Pages was changed.

- A number of fields in the SD Billing Engine Setup were reordered for ease of user input and understanding.

- The URL Link in the About Page was updated to link to the Billing Engine product on our website.

- Visual changes were made to menu in the SD Billing Engine Setup Card to keep this Setup card consistent with the Setup Cards of our other products.

- Created Permissions Sets for SD Billing Engine.

- Updated the Sales Order Activity Group on the Billing Engine Role Centre to be searchable in the Tell Me.

- Updated the Active Billing Activity Group on the Role Centre to be searchable in the Tell Me.

- The caption on the Historical Billing Activity Group was updated.

- The Billing Type field on the Billing Element Codes list was moved to the first column in the list for ease of input.

- For Contract Lines, the Item Description on the Invoice Line now takes the description for the Item from the Contract Lines as the user may update the description on the Contract Line.

- For Activity Lines, the Item Description on the Invoice Line now takes the description for the Advanced Activity Setup Billing Description as the same Item could have several Billing Codes associated with it. 

- Captions were added to fields, actions, groups etc for future use of translation tool.

- For Invoices generated from Manual Lines, the Billing Description from the Manual Activity Card is now displayed on the invoice lines instead of the item description.

- The Start Dates in the Contract Header and Contract Lines are no longer automatically set to Work Date on creation of the Contract Header and Lines.

- Downgraded all changes made in D365BCv17 version of the product to a D365BCv14 version of the product.

- Created test codeunits for App Source submission.

- Prepared the SD Billing Engine Product for App Source submission.

- Changed the logic in the Generate Invoices for Manual Lines not to amalgamate the manually logged lines into one line per billing code.

- The mandatory fields on the Get Entries dialog in the Activity Lines page were updated to denote mandatory entry required.

- Tooltips were added to the Setup Card to explain the Customer Dimension, Activity Setup Type,  and Dimension Handling fields.

- A change was made to the Suggest Billing Lines to allow users to choose to run for All, Contract, Activity or Manual billing types.

- Visual changes were made to the Contract Card. The Related Entries FastTab was removed and the counts of Posted and Unposted Invoices were moved to the FactBox.

- Start and End Dates were added to the Contract Lines. If a line has expired, the Item No is highlighted with red styling.

- A Start and End Date was added to the Contract Header. When a Contract is out of date the Contract No. on the Active Contracts list is highlighted with yellow styling.

- A number of visual changes were made to the Billing Engine Setup card - captions were renamed and KPI fields were moved.

- Default Dimension Codes and Values were added to the Billing Engine Setup so users can analyse the invoices generated by SD Billing Engine.

- A field caption in the Setup Card was recaptioned. 

- Made a change to populate the Job Codes on Activity Lines from the source line.

- Made a change to check that if enforce Job Code on Activity Lines in the Setup is switched on, then user should be prompted that the Activity Lines should have a Job Code if the Job Code is missing.

- The order of the Activity Groups in the Billing Engine Role Centre was changed.

- Upgraded Billing Engine reports to AL.

- Displayed the Billing Code Description on the Advanced Activity Setup page. 

- Change made to allow Activity Lines be exported to a CSV file.

- The Activity Lines page was tidied up.

- A change was made to allow creation of a billing code and assign to a Manual Template Card.

#### Bug Fixes

- Fixed an issue where Activity Lines were not grouped when the invoice was created.

- For Billing Lines of Type Activity an issue was fixed where incorrect quantities were calculated if the Activity Description was updated on the Activity Line.

- Turning off the Enforce Contract Price flag on the Billing Engine Setup did not find the best price using find best price functionality. The caption was updated to reflect what the functionality was actually meant to do - enforce zero contract prices.

- Setting the Item Category on the Recurring Elements Setup FastTab in the Billing Engine Setup did not limit the items that users could add to the Contract. This is now fixed.

- Captions on the XMLport Objects were incorrect and were updated to use the correct captions.

- The ability to call the Get Entries routine repeatedly without deleting old lines was fixed.

- Start and End Dates on the Contract Lines could not be added to the page using personalisation. The Start and End date fields are now displayed by default on the page.

- Fixed an issue where an error was raised when generating invoices for a Customer who has two contracts with the same billing code.

- Fixed an issue where there was an error on length when generating a description on the invoice. 

- A fix was made to the Manual Activity Card to display the Billing Description and the Item Description in the Recent Activities FasatTab.

- The Extension FastTab in the Setup Card was removed. For flexibility, a Create Invoice Handler Codeunit and a Create Order Handler Codeunit and functionality were created.

- A fix was made to the Invoices generated for Activity and Manual Lines to show the Description of the Item No and not the Billing Type.

- Fixed an issue where newly created Billing Codes cannot be assigned to a Manual Template Card.

### 2.0.4

#### Enhancements

- BCv14 App - A flag was added on the Setup Card to stamp the generated invoices with the Billing Period.

- BCv14 App -  A change was made to allow users to enter a description line on the Recurring Job Card.

- BCv14 App - A Recurring Enforce Contract Price option was added to the Billing Engine Setup Card.

### 2.0.3

#### Bug Fixes

- BCv14 App - Fixed an issue where the Item Description on Contract Lines was not passing to the generated invoice lines.

- BCv14 App - Fixed an issue where blank lines were being saved on contract lines if a user clicked onto the blank line.

### 2.0.2

#### Enhancements

- BCv14 App - Fixed a visual on the Activity List.

- BCv14 App - Increased length of the Item Description field on the Recurring Line.

- BCv14 App - Increased length of Customer Name field on a Billing Engine page.

### 2.0.1

#### Enhancements

- BCv14 App - Nade a change to the Manual Activity Card where a Billing Code can be added if the Template Code is empty.

- BCv14 App - A change was made to the appearance of the Role Centre.

### 2.0.0

#### Enhancements

- Created an Interface codeunit to allow another of our ISV products interface with SD Billing Engine and generate Sales Orders.

### 1.0.0

#### Enhancements

- A change was made to allow an item to be linked to more that one customer dimension.

- Functionality to Get Entries from ILEs for Sales Returns and Purchase Returns was added to the Activity Advanced Setup page.

- Functionality was developed to allow users easily create credit notes from invoices using the standard NAV create corrective memo process.

- An Activity Statement report was created.

- A change was made to prevent users from running billing again for activity lines that have already been invoiced/billed/are in the archive.

- A change was made to the Contract Header page to prevent users from overtyping the Last Invoice Date and Next Invoice Date fields.

- An exception report was created to highlight activities/ILEs that were not billed.

- On the Activity Lines page external fields were updated to be non-editable.

- For ease of user input, changes were made to the Manual Activity card to set default values and move certain fields to additional fields.  Customer's Currency field was added to the Manual Activity Card,

- A change was made to the Recurring Contract Lines to stop the unit price on the line defaulting to the price on the item card.

- Changes were made to the posting number series on the Billing Engine Setup page.

- Item Category, Enforce Job Code, Job Posting Group Filter to the Billing Engine Setup Card for each of the three elements.

- Added Default Payment Service to the Billing Element Code page.

- Functionality was added to the product to utilise the Default Deferral Template Codes on the Billing Element Codes.

- Visual changes were made to the Billing Element Codes page.

- Visual changes to the Manual Template card - names and descriptions were displayed, fields were regrouped and moved.

- Visual changes were made to the Manual Template List page.

- Made visual changes to the Manual Activity Card - reordering and repositioning fields.

- The Create from Template Action on the Manual Template List page was removed.

- For ease of user input, changes were made to the Create from Template page.

- Columns on the Manual Lines page were re-named and re-ordered.

- The Customer Name was displayed on the Manual Lines Page.

- The Customer Name field on the Activity Advanced Setup page was changed to display only.

- Export XML and Export CSV Actions were added to the Activity Lines page.

- The C/AL code base was converted to AL.

- Allow users for billing lines without a job code, and where the enforce job code is selected, to receive a warning if job codes are missing and generate the invoice. The invoice cannot be posted if the job code is missing.

- On suggested Billing Lines filter the Job Code by Customer.

- Added the job code filed to the manual lines list page.

- Filter the job code on activity lines to the filter specified in the Activity Elements Job Posting Group Filter field on the Setup.

- Job Codes for Sales Lines will be required on the suggested billing lines.

- In the Setup for Recurring Elements when the Enforce Job Code is set to yes, there is now a check on the Billing Lines for those lines without a job code - when generating invoices a warning is raised that a Job code is required, but invoices are generated.

- Made a change to filter items in the contract lines to the filter specified in the Recurring Elements Item Category in the Billing Engine Setup.

- Made a change so that in the Contract Card, after a credit memo is posted, the next invoice date is reverted back.

- Made changes to the Activity Statement.

- Made a change to the Unposted and Posted Invoices flowfield count on the Billing Engine Activity Pages.

- Visual changes made to the position of fields on the Billing Engine Setup Card.

- Changes to billing tables were made as part of the corrective credit memo process.

- Changes made to the request page filters on the Activity Statement report.

- Item codes are not set on the Billing Element Code setup for Recurring Contract Billing Types.

- Made a change to the Get Entries from the ILE function to continue gathering entries if an item has no dimension.

- Fixed an issue with the find best price functionality in SD Billing Engine.

- The Get Entries from the ILE were not including an external unit of measure.

- Tables and pages were renamed as per our ISV standards.

- The SD Billing Engine Role Centre was re-captioned.

- Made a change to the Activity List to notify users if Activity List Items were skipped due to missing dimension values.

- Changes were made to the Recurring Card.

- Cues in the Role Centre were updated to refresh automatically.

- Visual changes were made to the Activity Advanced Setup page.

- Various visual changes such as re-ordering columns, adding fields and re-naming ribbon groups were made to the SD-UB Billing Element Codes page.

- Visual changes were made to the SD-UB Manual Template List to display the Customer Name.

- Visual changes were made to the SD-UB Manual Activity List to rename certain fields on the page.

- Visual changes were made to the SD-UB Recurring Contract List - Sell-to Customer Name displayed and columns were re-captioned.

- Visual changes were made to the SD-UB Activity Advanced Setup page - Customer Name and Billing Descriptions were displayed.

- Renamed the SD-UB Ext. Units of Measure table to SD-UB External UoMs.

- Visual changes were made to the SD Billing Engine Setup card - fields were renamed, reordered, regrouped.

- Pages were re-captioned.

- SD Billing Engine pages and tables were re-ordered and re-numbered as per our ISV standards.

- A change was made on the setup to allow the user to specify any dimension as the Customer Dimension.

- Fields were re-arranged on the Manual Activity List page.

- Filters on the cues on the Activity pages were updated.

- The standard NAV FindBestPrice functionality was added to the product.

- Setup and Units of Measure Mapping actions were removed from the Billing Element Codes page.

- When a Sales Invoice Line is created a blank item line is inserted to denote lines created by a Recurring, Activity, or Manual Element.

- Visual changes were made to the Manual Activity Card.

- Made a change to group lines at the billing stage.

- Changed the mapping on the SD-UB Ext Units of Measure table to a one to one mapping.

- Created Templates for Manual Billing to enable users quickly input manual entries.

- A specialised custom Codeunit was created to get ILE entries.

- A change was made to allow users to configure where to import the data from.

- Created a factbox to show the total  billing count of no. of lines and the total value.

- Changes were made to the navigation flow between pages and unnecessary actions were removed from pages.

- Various changes were made to the Suggested Billing Lines page including adding a progress indicator when the Generate Invoice action is chosen.

- Changes were made to the Activity List.

- Added an action to the activity page to call the Setup Card.

- Actions surfaced on the SD Billing Engine Role Centre were moved to the SD Billing Engine Setup page.

- Removed standard NAV One Note and Links from the SD Billing Engine Pages.

- Created an SD Billing Engine Role Centre.

- Created our standard ISV About page.

- Created SD Billing Engine Codeunits - Manual Lines Archive functionality.

- Created SD Billing Engine Codeunits - Activity Lines Archive functionality.

- Created SD Billing Engine Codeunits - Validation functionality.

- Created SD Billing Engine Codeunits - Suggest ILE functionality.

- Created SD Billing Engine Codeunits - Generate Invoices functionality.

- Created SD Billing Engine Codeunits - Manual Elements.

- Created SD Billing Engine Codeunits - Activity Elements.

- Created SD Billing Engine Codeunits - Recurring Elements.

- Created SD Billing Engine Codeunits - Wrapper.

- Created SD Billing Engine XMP ports.

- Created our standard ISV pages - Role Centre page, Activity KPI pages, About page.

- Created SD Billing Engine Pages.

- Created SD Billing Engine Tables.

#### Bug Fixes

- Fixed an issue in the Copy Configuration in Advanced Setup where the Customer Name is not updated.

- Fixed an issue where on the manual lines the job code was not carried over to the suggested billing lines.

- Fixed an issue where activity lines generated without a job code did not validate.

- Fixed an issue where job codes added on a purchase line were not carried over to the activity lines.

- Fixed a payment service flowfield error in the recurring contracts card.

- Fixed an issue where an error was raised when adding a Billing Code to a Recurring Contract.

- Functionality to Get Entries from ILEs for Sales Returns and Purchase Returns was added to the SD Billing Engine product.

- Additional visual changes were made to the Manual Activity card.

- Validation issues on the Manual Template card and the Manual Activity card were fixed.

- The Billing Frequency field was removed from the Recurring Contract List page.

- Fixed an issue where a customer could not be selected on the Manual Activity card.

- The Create from Template action was removed from the Manual Activity List page.

- An issue in the Recurring Contract Card where deleted invoices were viewable as posted invoices was fixed.

- The caption on the SD Billing Engine Setup page was re-captioned.

- Renamed SD Billing Engine pages to our standard format.

- Fixed a compile error in the Activity Webservice API page.

- A fix was made to a codeunit to get activity entries.

- Issues in the Codeunit for getting Activity Lines from the ILE were fixed.

- Fixed an issue where in the Suggested Billing Lines page, the unit price for manual lines was not inserted into the line.

- Changes were made to the Activity Element fields in the SD Billing Setup card - fields were rearranged and reordered.

- Created a new factbox to show billing information for the individual billing lines.

- Fixed an issue when adding manual records from the Manual Activity Card.

- The Recurring Contract was showing deleted invoices in the Count of Posted Invoices.

- A fix was made to unposted invoice filters when the Suggest Lines function was used.

- A page compile issue was fixed.

- A Recurring Element Contract Lines fact box was created.

- Renamed the SD Billing Engine Pages.

- Renamed SD Billing Engine Pages.

- Changed the URL displayed on the About page.


## SD Billing Engine Releases

### 7.1.2

#### Enhancements

- AppSource App - A change was made to check for Unposted Invoices before running the Suggest Lines. A prompt is raised if Unposted Invoices exist and the Unposted Invoices and Unposted Orders cues in the Role Centre are highlighted in red if unposted transactions exist. 

- AppSource App - A link to the user guide on the DynamicsShop page was added to the About page and to the Manage Subscriptions page.

### 7.1.1

#### Enhancements

- AppSource App - A change was made to allow for Renumbering of Contracts. A composite key on the price change history table was updated.

### 7.1.0

#### Enhancements

- AppSource App - A change was made to take the Payment Method and Payment Terms Code from the Customer Card if the Payment Method and Terms Code are not defined on the Contract.

- AppSource App - A new Licence Activate and Setup Wizard was created.

- AppSource App - The notification to activate the app was added to the standard Business Central role centres.

- AppSource App - Changes were made to the Manage Subscriptions page.

- AppSource App - The Lead Subscription Link from the Request Subscription action in the Product Activation page was updated.

- AppSource App - A new action was added to the Setup Card called View Our Apps. This action opens a page on AppSource pointing to all our Simply Dynamics Ltd apps.

### 7.0.4

#### Enhancements

- AppSource App - A minor mod was made to the SD Billing Engine Generate Sales Order routine.

- AppSource App - The Meter Type Prices, Activity List and Suggested Billing Lines List were updated to allow for 5 decimal places for the Unit Price.

### 7.0.3

#### Enhancements

- AppSource App - An API page was created for SDY UB Asset History (43006463).

- AppSource App - Allow for drill down on Asset History in Live Contract Lines. 

### 7.0.2

#### Enhancements

- AppSource App - Allow users to select number series with relationships on the Contract Cards.

- AppSource App - The table relation between the Project Code and the Customer on the Recurring Line was modified.

- AppSource App - Created a new Contract List to display Activity and Recurring Contracts.

### 7.0.1

#### Bug Fixes

- AppSource App - The new sales doc generator interface, which replaced the create invoices codeunit, was pulling the description from the item rather than from the contract line. 

### 7.0.0

#### Enhancements
 
- AppSource App - Pro Rata Billing functionality was added.

- AppSource App - Incremental Billing functionality was added.

- AppSource App - The create invoices functionality was reworked. The Create Orders Handler and the Create Invoice Handler were set as obsolete and are replaced by a Sales Doc Generation Enum/Interface.

- AppSource App - The Get Entries functionality was reworked.

- AppSource App - A new codeunit Suggest Act. Contracts v2 was created to handle where meter reads are additive and no estimation is required.

- AppSource App - Dimensions were implemented on the Contract Header. Dimensions added to the Contract are stamped on the suggested invoices.

- AppSource App - Contract Dimensions and Billing Engine Setup Dimensions are included in the recalc dimension routine.

- AppSource App - A change was made to pass the option on the Customer Card "Price includes VAT" through to the created invoice.

- AppSource App - An event was added to codeunit 43006464 "SDY UB Suggest Act. Contracts" to allow for modification of billing lines for Activity Contracts.

- AppSource App - A new codeunit Suggest Act. Contracts v2 was created to handle where meter reads are additive and no estimation is required.

- AppSource App - Codeunits 43006440 "SDY UB Billing Wrapper", 43006441 "SDY UB Billing Recurring Items", 43006442 "SDY UB Billing Activity Items", and 43006443 "SDY UB Billing Manual Items" were marked as obsolete and an error is now thrown when the billing routine is run if these codeunits are defined on the setup.

- AppSource App - A change was made to handle the scenario where assets have been uninstalled from a contract prior to the invoice run.

- AppSource App - The Copy Fixed Asset action no longer copies the contract no from the previous asset to the new asset.

- AppSource App - The Validate All and Validate Selected actions now validate by activity date rather than workdate to find the correct contract. 

- AppSource App - The Contract List was changed to allow filtering by Billing Type.

- AppSource App - The count of Contracts on the Billing Code FactBox was split out to a separate count for Activity Contracts and a separate count for Recurring Contracts.

- AppSource App - A change was made to auto select the default billing item when installing assets. 

- AppSource App - A change was made to prevent users from deleting a billing code if it exists on a contract.

- AppSource App - All Billing Engine pages were reviewed and UI changes, tooltip and caption updates were made.

- AppSource App - Additional phrases were added as search phrases for the SD  Billing Engine pages.

- AppSource App - Enhancements were made to the App Request Subscription page.

- AppSource App - A change was made to the licence expiry notification. The logic for checking for expiry dates was reworked.

- AppSource App - The status field was added to the Contract API.

- AppSource App - Changes were made to the Assisted Setup Wizard.

- AppSource App - The Billing Type Option Field was replaced by Billing Method Enum.

### 6.0.1

#### Bug Fixes

- AppSource App - If the Sales Invoices and Posted Sales Invoices were using the same number series, the contract was not updated when the invoice was posted. This was fixed.

### 6.0.0

#### Enhancements

- AppSource App - Create functionality to allow users to create Activity Contracts that will be used for activity based billing invoiced from imported event based metrics.

- AppSource App - A new Billing Engine Meter Read Activity table together with associated functionality was created to allow for activity based billing based on meter reads. 

- AppSource App - A new Billing Engine Meter Read Archive table together with associated functionality was created. 

- AppSource App - Create a new table for Meter Prices to hold the different prices. Prices will be setup per customer, per meter type, and have a start and end date. 

- AppSource App - Functionality was created to allow for situations where the one fixed asset on an Activity Contract could have multiple different types of meter reads. Each different meter read type will appear as a different line on the activity lines and on the sales invoice. 

- AppSource App - Functionality was added to pick up a minimum charge for certain types meter reads. 

- AppSource App - In order to track Contracts costs and profitability, functionality was developed to link Contracts to Jobs. Users can now post costs against the Job as per standard. When an Invoice created by SD Billing Engine is posted the contract revenues are posted to the Job Ledger. 

- AppSource App - If a Recurring Contract or an Activity Contract has a Billing Code that specifies a link to a Job, a Job Template with Task Lines is auto created and linked to the Contract.  

- AppSource App - A link has been added at Contract Line level to hold a Fixed Asset and Serial Number for the Fixed Asset. For Activity Billing the metrics can feed into the system based on a device serial number. 

- AppSource App - Functionality regarding installation and deinstallation of a Fixed Asset on a Contract was reworked and refined.

- AppSource App - A change was made to filter installing an Asset on a Contract by Contract Type as an Asset can be installed on a Recurring Contract to bill the lease and on an Activity Contract to bill the usage. 

- AppSource App - Changes were made to SD Billing Engine to remove the Activity Elements Get Entries Handler from the SD Billing Engine Setup card and to place the Get Entries Handler on the Activity Billing Codes.

- AppSource App - Changes were made in the SD Billing Engine Setup card to rename the Recurring Elements Setup FastTab to Contract Setup and remove some fields.

- AppSource App - An action to the Fixed Assets List was added to the SD Billing Engine Setup Card. 

- AppSource App - The Contracts drilldown on the Setup Card was recaptioned to Recurring Contracts and a drill down to Activity Contracts was surfaced. 

- AppSource App - A boolean option was added to the SD Billing Engine Setup card to hide the meter read comments on the generated Sales Invoice. 

- AppSource App - A change was made to allow users to hide the Billing Type, Billing Code and/or the Billing Period comments on the generated Sales Invoice. 

- AppSource App - In the SD Billing Engine Job Template Card the link with the Billing Code was removed. 

- AppSource App - Rename the Recurring Lines FastTab in the Contract Card to Contract Lines FastTab. 

- AppSource App - Fields in the General FastTab on the Recurring Contract Card and the Activity Contract Card were rearranged.

- AppSource App - A change was made to the meter read table to allow decimal meter reads. 

- AppSource App - A separate page was created for the Activity Contract Lines and the Recurring Contract Lines. 

- AppSource App - A change was made to handle the import of Assisted Data Setup to handle future requests to allow for demo data to be imported from a file. 

- AppSource App - The text inserted onto the invoices for meter reads was updated. 

- AppSource App - The Contract Billing Period is stamped as text on the Posted Sales Invoice Line. This value is now also stamped to a new field on the Posted Sales Invoice Header. 

- AppSource App - A change was made to stamp the Job Ledger Entry Date with the invoice posting date instead of stamping with the work date. 

- AppSource App - Upgrade code was added to upgrade existing versions of Billing Engine v5.0.0 Contracts to the new Contract table structures in v6.0.0. 

- AppSource App - A change was made so that Meter Reads with a Meter Read Date after the Contract's Billing Period shouldn't be brought in to the Suggested Billing Lines. 

- AppSource App - The instructional text in the Uninstall Asset Wizard was updated. 

- AppSource App - A change was made to pass the Fixed Asset No. and Serial No. from the Contract Lines to the Sales Invoices and to the Job Ledger Entries. 

- AppSource App - Job KPI fields were added to the to Contract Detail FactBox. 

- AppSource App - The Quantity and Values posted to the Job Ledger Entry on posting an invoice for a Contract linked to a Job should be negative. 

- AppSource App - A change was made to post the Job Ledger Entry with the Invoice Document No.  

- AppSource App - New fields, Recurring Contract No. and Activity Contract No., were added on the extended Fixed Asset list.  

- AppSource App - In the Fixed Asset list the drill down on the Contract No. was showing two Contract Lines as being on the same Contract but this was incorrect. One Contract was Recurring and the other was Activity. The Contract No. field was split out to show Recurring and Activity Contracts. 

- AppSource App - In the Billing Codes FactBox the Recurring Contracts caption was updated to Contracts. 

- AppSource App - The Contract List action on the Fixed Assets list and Fixed Assets card was only showing Recurring Contracts. This was changed to also show Activity Contracts. 

- AppSource App - A change was made when the Activity Line is validated in the Activity Lines list to transfer the Source Activity Date to the Activity Date field.

- AppSource App - Column headings on the Activity Lines list were updated. 

- AppSource App - If lines for the same serial no. but different meter read types exist in the Meter Read Activity we need to bring in the lines by meter read type into the Activity Lines list. 

- AppSource App - FlowFields were surfaced on the Contract FactBox to show pending and archived/applied price changes. 

- AppSource App - In the Contract Price Worksheet a caption was added to the Set Take Effect Date action that the Take Effect Date is based on the Billing Period Range and not the Billing Date. The ToolTip for the Set Take Effect Date action was also updated. 

- AppSource App - The captions of the Suggest Lines request pages were updated. 

- AppSource App - The Get Entries Handler column in the Billing Element Codes list was set to non-editable for Recurring and Manual Billing Types.  

- AppSource App - A freeze frame was added after the Billing Code on the Billing Element Code list. 

- AppSource App - Some minor changes were made to the Billing Element Codes list. 

- AppSource App - The FlowField count of the Prices field in the Meter Types list was set to recalculate when a new Price for the Meter Type is created in the Meter Type Prices list. 

- AppSource App - An action name in the SD Billing Engine Setup Card was changed and actions were rearranged. 

- AppSource App - Updates were made to ToolTips in the SD Billing Engine Setup Card. 

- AppSource App - Updates were made to the text displayed in the Assisted Setup Wizard. 

- AppSource App - The instructional text in the Install Asset Wizard was updated. 

- AppSource App - The logo in the App was updated to our new logo. 

- AppSource App - The Links in the About Page were updated.   

#### Bug Fixes

- AppSource App - Renumbering a Billing Engine Contract did not renumber the contract lines nor the contract version history.  

### 5.0.1

#### Enhancements

- AppSource App - The Contract Billing Period is stamped as text on the Posted Sales Invoice Line. This value is now also stamped to a new field on the Posted Sales Invoice Header.

- AppSource App - The logo in App was updated to the new logo.

- AppSource App - The links in the About page were updated.
  
- AppSource App - The Power BI Report FactBox was removed from the Role Centre.

### 5.0.0

#### Enhancements

- AppSource App - Tables and pages were created for a Contract Price Adjustment Worksheet, a Pending Price Changes list and a Historic Price Changes list. 

- AppSource App - Functions were created to Get Entries, Suggest Price Change and Apply Price Changes. 

- AppSource App - Changes were made to allow for detailed line level tracking of Contract changes. 

- AppSource App - The Entry Type on Contract Tracking specifies if there was a quantity change or a price change. 

- AppSource App - The Change Type on the Contract Header was updated not to display blanks. The Change Type is now always an increase or a decrease. 

- AppSource App -  Detailed Contract Tracking entries are created from details in the Contract Versions on upgrade to version 4.0.0 of SD Billing Engine. 

- AppSource App - Three cues were added to the Role Centre for Contact Price Changes, Pending Price Changes and Historic Price Changes. 

- AppSource App - Changes were made to the Pending Price Lines to add a FactBox with count of lines and a sum of the quantity. 

- AppSource App - In the Pending Price Changes list a message is displayed to the user when the Process Pending Price Changes action is selected to let the user know that choosing the action will apply all Pending Price changes that have a Take Effect Date less than or equal to the workdate. Otherwise the Pending Price changes will be automatically applied when the user chooses Suggest Lines on the next billing run. 

- AppSource App - In the Contract Price Worksheet the Take Effect Date is now based on the Billing Period Range and not the Billing Date.  The Process Pending Price Changes action was removed. The Pending Price changes are automatically applied when the user chooses Suggest Lines on the next billing run if the take effect date is within the Billing Period Range. 

- AppSource App - An option on the Suggest Price Change was added to keep the current discount or set the discount to 0. 

- AppSource App - A filter on the Currency was added when choosing Suggest Price Changes for a Change Type of Price Book. 

- AppSource App - In the Contract Price Adjustment Worksheet allow a drill through from the Item No to the Item Card. 

- AppSource App - If there are existing lines in the Contract Price Adjustment Worksheet and the Get Contract Price Lines action is selected then prompt the user that existing lines will be cleared. 

- AppSource App - A change was made to limit the SD ISV Tenant Subscriptions page to display just our SD ISV AppSource Apps and not other SD PTE Apps. 

- AppSource App - A change was made to allow users to view the versions of a closed contract from the Recurring Archive Card. 

- AppSource App - The Contract History Detail Report action was removed from the Recurring Archive Card. 

- AppSource App - A change was made to include closed contracts when creating the initial build of contract tracker detail records based on data in the contract tracker summary. 

- AppSource App - An Action was surfaced on the Contract Tracker Summary page to allow drilldown to the Contract Tracker Detail page. 

- AppSource App - Changes were made to the Header and Detail Tracker pages. The Date field was renamed to Change Date and moved to the right of the Entry No. field. 

- AppSource App - The SDY UB Contract History Detail report was retired from the product. 

- AppSource App - An Action to Build the Contract Tracker Detail table was surfaced on the SD Billing Engine Setup card. This action will call upgrade code which creates a new version of all Contracts; builds the Contract Tracker Detail table; updates Creation records in Contract Header to increase; updates Removal records in Contract Header to decrease; and sets an Upgrade Boolean field on the Billing Engine Setup table to false.   

- AppSource App - The KPI groups on the SD Billing Role Centre were cleaned up and rearranged. 

- AppSource App - Decimal formatting was applied to the Contract Tracker page as per the decimal formatting applied to the Contract Detail Tracker page. 

#### Bug Fixes

- AppSource App - When selecting SD Billing Engine activity pages in the Tell Me/Search in a BCv22 environment, the activity pages were hanging. 

- AppSource App - Pending Price changes that had a Take Effect Date less than or equal to the workdate were not automatically applied when Suggest Lines on the next billing run was chosen. 

- AppSource App - Fixed an issue where a new contract created as version 1 had no quantity on the lines, the contract was then modified to have a line quantity. The Contract Tracker functionality created a summary contract tracking header but detail lines were not created for the new version. 

- AppSource App - Summary and Detail Tracker KPIs did not match where Contracts that were created and then closed straight away were not included in the initial build of the Contract Tracker Detail. This was fixed. 

- AppSource App - A change was made to fix an issue where the Current Month KPIs were not filtering on the Current Month. 

- AppSource App - An error was raised in the Assisted Setup import if non sequential enum values exist in the imported data. This was fixed. 

- AppSource App - A change was made to the ISV Licence Notification procedure in SD Billing Engine to fix an issue that would raise an error when the language is changed from English to another language.

### 4.1.1

#### Enhancements

- BCv14 App - The Contract Billing Period is stamped as text on the Posted Sales Invoice Line. This value is now also stamped to a new field on the Posted Sales Invoice Header.

#### Bug Fixes

- BCv14 App - When renumbering a Billing Engine Contract the Contract Lines, Archived Records and Price Change Lines were missing a table relation and were not renumbering correctly. This was fixed.

### 4.1.0

#### Enhancements

- BCv14 App - If there are existing lines in the Contract Price Adjustment Worksheet and the Get Contract Price Lines action is selected then prompt the user that existing lines will be cleared.

- BCv14 App - In the Contract Price Adjustment Worksheet allow a drill through from the Item No to the Item Card.

- BCv14 App - A filter on the Currency was added when choosing Suggest Price Changes for a Change Type of Price Book.

- BCv14 App - An option on the Suggest Price Change was added to keep the current discount or set the discount to 0.

- BCv14 App - In the Contract Price Worksheet the Take Effect Date is now based on the Billing Period Range and not the Billing Date.

- BCv14 App - Changes were made to the Pending Price Lines to add a FactBox with count of lines and a sum of the quantity.

#### Bug Fixes

- BCv14 App - When selecting a different Change Type on the Suggest Price Change page the correct options were not always showing. This was fixed.

### 4.0.2

#### Enhancements

- BCv14 App - A change was made to include closed contracts when creating the initial build of contract tracker detail records based on data in the contract tracker summary.

- BCv14 App - Changes were made to the Header and Detail Tracker pages. The Date field was renamed to Change Date and moved to the right of the Entry No. field.

- BCv14 App - An Action was surfaced on the Contract Tracker Summary page to allow drilldown to the Contract Tracker Detail page.

- BCv14 App - The Contract History Detail Report action was removed from the Recurring Archive Card.

- BCv14 App - A change was made to allow users to view the versions of a closed contract from the Recurring Archive Card.

#### Bug Fixes

- BCv14 App - Summary and Detail Tracker KPIs did not match where Contracts that were created and then closed straight away were not included in the initial build of the Contract Tracker Detail. This was fixed.

### 4.0.1

#### Enhancements

- BCv14 App - A change was made to fix an issue where the Current Month KPIs were not filtering on the Current Month.

- BCv14 App - The KPI groups on the SD Billing Role Centre were cleaned up and rearranged.

- BCv14 App - The SDY UB Contract History Detail report was retired from the product.

- BCv14 App - An Action to Build the Contract Tracker Detail table was surfaced on the SD Billing Engine Setup card. This action will call upgrade code which creates a new version of all Contracts; builds the Contract Tracker Detail table; updates Creation records in Contract Header to increase; updates Removal records in Contract Header to decrease; and sets an Upgrade Boolean field on the Billing Engine Setup table to false.  

### 4.0.0

#### Enhancements

- AppSource App - Code was added to check if the Contract Tracking table is empty on install or upgrade. If empty, the Contract Tracker table is populated.  

- AppSource App - KPIs for Monthly Metrics for value and quantity of New Contracts, Lost Contracts, Revenue Increase, and Revenue Decrease were added to the BCv21 code base. 

- AppSource App - A change was made to bring the Payment Method Code and Payment Terms Code from the Contract Header through to the Sales Invoices. 

- AppSource App - The Contract change at line level item is now shown on the Contract History Detail report. 

- AppSource App - A new Reset Contract action was added to the Contract Card. Choosing this action archives the Contract, reinstates the new Contract with the same contract number and allows the user to modify the Next Invoice Date, Billing Code or Currency Code. 

- AppSource App - A change was made to allow users to edit the Default Payment Method on the Contract Header. 

- AppSource App - A change was made to allow users to edit the Payment Terms on the Contract Header if the status of the Contract Header is New. 

- AppSource App - Standard Links, Notes and Attachments were added to the Contract Header. 

- AppSource App - A field caption was changed on the Setup Card. 

- AppSource App - A ToolTip was updated on the SD Billing Engine Setup Card. 

- AppSource App - The values in the Contract Tracking list were formatted to show fixed decimal places. 

- AppSource App - The Sales Order Activity Panel was removed from the SD Billing Engine Role Centre. The Sales Order Activity Panel can be found by searching the Tell Me. 

- AppSource App - The Versions field on the Recurring Contract Card was set to display when users choose "Show More" on the General FastTab. 

- AppSource App - On the Recurring Contract Card, the Invoicing FastTab was moved to display under the General FastTab. 

- AppSource App - The Billing Code, Customer Name and Status were set to promoted on the General FastTab of the Recurring Contract Card. 

- AppSource App - The SD Billing Engine Permission Object names were standardised to the same format as that in our other Apps. 

- AppSource App - The Licence Message displayed on first install of SD Billing Engine was changed to prompt the user to activate a free trial and to choose Assisted Setup from the Setup Card to create demo data. 

- AppSource App - A page was created to display all the Simply Dynamics Apps and subscription details for the tenant. 

- AppSource App - The Licence Expiry message/notification was updated to display the App Name. 

- AppSource App - An alert notification is raised to prompt users that they need to validate the SD Billing Engine licence. 

- AppSource App - The Product Activation Page was updated to point to the new CRM URL. 

- AppSource App - The ToolTips were updated to look at our new website. 

- AppSource App - The links in the About Page were updated to point to new URLs. 

- BCv14 App - Changes were made to allow for detailed line level tracking of Contract changes.

- BCv14 App - The Entry Type on Contract Tracking specifies if there was a quantity change or a price change.

- BCv14 App - The Change Type on the Contract Header was updated not to display blanks. The Change Type is now always an increase or a decrease.

- BCv14 App - Detailed Contract Tracking entries are created from details in the Contract Versions on upgrade to version 4.0.0 of SD Billing Engine.

- BCv14 App - Tables and pages were created for a Contract Price Adjustment Worksheet, a Pending Price Changes list and a Historic Price Changes list.

- BCv14 App - Functions were created to Get Entries, Suggest Price Change and Apply Price Changes.

- BCv14 App - Three cues were added to the Role Centre for Contact Price Changes, Pending Price Changes and Historic Price Changes.

- BCv14 App - In the Pending Price Changes list a message is displayed to the user when the Process Pending Price Changes action is selected to let the user know that choosing the action will apply all Pending Price changes that have a Take Effect Date less than or equal to the workdate. Otherwise the Pending Price changes will be automatically applied when the user chooses Suggest Lines on the next billing run.

- BCv14 App - Decimal formatting was applied to the Contract Tracker page as per the decimal formatting applied to the Contract Detail Tracker page.

### 3.5.2

#### Enhancements

- BCv14 App - A change was made to the BCv14 App to bring the Payment Method Code and Payment Terms Code from the Contract Header through to the Sales Invoices. 

### 3.5.1

#### Enhancements

- BCv14 App - A new Reset Contract action was added to the Contract Card in the BCv14 code base. Choosing this action archives the Contract, reinstates the new Contract with the same number and allows the user to modify the Next Invoice Date. 

- BCv14 App - A change was made to the BCv14 code base to allow users to edit the Payment Terms on the Contract Header if the status of the Contract Header is New. 

- BCv14 App - A change was made to the BCv14 code base to allow users to edit the Default Payment Method on the Contract Header. 

- BCv14 App - The Contract change at line level item is now shown on the Contract History Detail report in the BCv14 App. 

- BCv14 App - Standard Links, Notes and Attachments were added to the Contract Header in the BCv14 code base. 

### 3.5.0

#### Enhancements

- BCv14 App - KPIs for Monthly Metrics for value and quantity of New Contracts, Lost Contracts, Revenue Increase, and Revenue Decrease were added to the BCv14 code base. 

### 3.4.0

#### Enhancements

- BCv19 App  - The link to the Assisted Setup via GitHub was removed from the Billing Engine Setup. 

- BCv19 App - The D365 BASIC permission set was extended to include SDYUBView permissions. 

- BCv19 App - Changes were made to the text in the Assisted Setup Wizard. 

- BCv19 App - The Latest Version of the product and the AppSource URL were added to the About Page. 

- BCv19 App - Visual changes were made to the request page launched when the Suggest Lines action is chosen. 

- BCv19 App - The Customer Name was added to the Suggest Billing Lines FactBox. 

- BCv19 App - If there is no value in the Posting Description field on the Setup then the Posting Description on the Contract defaults to the Billing Code Description. 

- BCv14 App - Job and Item Category filters were moved from the SD Billing Engine Setup to the Billing Codes. 

- BCv14 App - Versioning of Contracts was added to the BCv14 App. 

- BCv14 App - Visual changes were made to the request page launched when the Suggest Lines action is chosen. 

- BCv14 App - The Customer Name was added to the Suggest Billing Lines FactBox. 

#### Bug Fixes

- BCv19 App - The Job Code specified on the contract lines was not transferred from the contract lines to the suggested billing lines. 

- BCv19 App - The Item Category filter did not work correctly on the Recurring Lines. 

- BCv19 App - Users could not post Sales Invoices without SD Billing Engine Setup permissions. Permission to read Billing Engine Setup was granted to the D365 BUS FULL ACCESS permission set. 

- BCv19 App - Fixed an issue where an error was raised after choosing yes to the Validate Licence prompt. 

- BCv19 App - Contracts could not be Bulk Updated to 'Closed'. 

- BCv19 App - Fixed an issue where Archived contracts could not be reinstated. A new contract is now created based on the details of the Archived contract. 

- BCv19 App - The Assisted Setup Wizard did not populate the Codeunits in the SD Billing Engine Setup card. 

- BCv19 App - The Suggest Billing action did not filter recurring lines by Billing Code. 

- BCv19 App - Fixed an issue with email validation where emails with a full stop failed validation when the Activate Trial action was chosen. 

- BCv19 App -  The Billing Code filter selected from the request page in the Suggest Billing Lines action was not updated on the request page.  

- BCv14 App - The Job Code specified on the contract lines was not transferred from the contract lines to the suggested billing lines. 

- BCv14 App - The Item Category filter did not work correctly on the Recurring Lines.  

- BCv14 App - Users could not post Sales Invoices without SD Billing Engine Setup permissions. Permission to read Billing Engine Setup was granted to the D365 BUS FULL ACCESS permission set. 

- BCv14 App - Fixed an issue where Archived contracts could not be reinstated. A new contract is now created based on the details of the Archived contract. 

- BCv14 App - Contracts could not be Bulk Updated to 'Closed'. 

- BCv14 App - The Suggest Billing action did not filter recurring lines by Billing Code. 

- BCv14 App -  The Billing Code filter selected from the request page in the Suggest Billing Lines action was not updated on the request page.  

### 3.3.0

#### Enhancements

- BCv18 App - Changes were made to the Text Lines that are inserted into the Sales Invoice Lines when the Invoices are generated. 

- BCv18 App - Changes were made to the Suggest Billing Lines request page. The Suggest Billing Date defaults to the workdate. Captions were relabelled. 

- BCv18 App - The auto split functionality was added to the Contract Lines to allow for the Contract Lines to remain in correct order when split. 

- BCv18 App - Functionality was added to the product to allow a snapshot of a Contract to be Archived. A flowfield was added to the Contract Header so users can drill down to view the archives. 

- BCv18 App - Changes were made to the Suggest Billing Lines request page. The Suggest Billing Date defaults to the workdate. Captions were relabelled. 

- BCv18 App - The standard BC action to allow edit in excel was added to the Recurring Contract List. 

- BCv18 App - A new action to Bulk Update Contract Status was added to the Recurring Contract List. 

- BCv18 App - A Line Discount field was added to the Recurring Contract Lines which passes through to the suggested billing lines and to the invoice lines. 

- BCv18 App - When choosing the Product Activation action the user is now prompted that they need to allow HttpClient Requests in Extension Settings. 

- BCv18 App - Contract Versioning functionality was added to the product. New status on the Contract of New, Live or Close. When a Contract is set to a Status of Close, the Contract is moved to an archive table. 

- BCv18 App - Certain cues in the Role Centre were reworked. 

- BCv18 App - The permission to read the SD Billing Engine Setup table was granted to the standard D365 BC Full Access permission set. 

- BCv18 App - The auto split functionality was added to the Contract Lines to allow for the Contract Lines to remain in correct order when split. 

- BCv18 App - When updating from earlier versions of SD Billing Engine the status of any existing Contracts is automatically set to Live. 

- BCv18 App - When the item is chosen on the contract and the Assist Edit on the Unit Prices field is chosen, the best price is added to the Contract Line. 

- BCv18 App - Functionality was added to the product to allow a snapshot of a Contract to be Archived. A flowfield was added to the Contract Header so users can drill down to view the archives. 

- BCv18 App - Additional cues were added to the Role Centre to display Live Contracts and New Contracts. 

- BCv18 App - The value of the Contract is displayed in the Recurring Contract List. 

- BCv18 App - Contract Lines are no longer hardcoded to Items of Type Service. The Billing Code setup can be defined to filter items to a particular type. 

- BCv14 App - A new action to Bulk Update Contract Status was added to the Recurring Contract List. 

- BCv14 App - A Line Discount field was added to the Recurring Contract Lines which passes through to the suggested billing lines and to the invoice lines. 

- BCv14 App - Contract Versioning functionality was added to the product. New status on the Contract of New, Live or Close. When a Contract is set to a Status of Close, the Contract is moved to an archive table. 

- BCv14 App - Certain cues in the Role Centre were reworked. 

- BCv14 App - When updating from earlier versions of SD Billing Engine the status of any existing Contracts is automatically set to Live. 

- BCv14 App - When the item is chosen on the contract and the Assist Edit on the Unit Prices field is chosen, the best price is added to the Contract Line. 

- BCv14 App - Additional cues were added to the Role Centre to display Live Contracts and New Contracts. 

- BCv14 App - When choosing the Product Activation action the user is now prompted that they need to allow HttpClient Requests in Extension Settings. 

- BCv14 App - The value of the Contract is displayed in the Recurring Contract List. 

- BCv14 App - Contract Lines are no longer hardcoded to Items of Type Service. The Billing Code setup can be defined to filter items to a particular type. 

#### Bug Fixes

- BCv18 App - Fixed an issue where the Wizard was not populating the Codeunits on the Assisted Setup.  

- BCv18 App - Fixed an issue with the Line Nos when the Contract Lines are split. 

- BCv18 App - Users cannot post Standard Sales Invoices without SD Billing Engine permissions. 

- BCv18 App - Fixed an error that was raised when text was input on the Contract Line and the Enforce Job Code was switched on in the SD Billing Engine Setup. 

- BCv18 App - When the user hits enter or tab on the Next Invoice Date, the focus now goes to the Next Billing Period field rather than to the Contract Lines. 

- BCv14 App - Fixed an error that was raised when text was input on the Contract Line and the Enforce Job Code was switched on in the SD Billing Engine Setup. 

### 3.2.0

#### Enhancements

- BCv18 App - Add the ability to split Line Nos on the Contract Lines. 

- BCv18 App - Recurring Lines are now ordered by Line No.  

- BCv18 App - Changes were made to Contracts to allow for a new Status option of New, Live or Closed. 

- BCv18 App - Changes were made to the text lines that are automatically inserted onto the Sales Invoice Lines generated by SD Billing Engine. The standard Text is no longer used. Text is now inserted on lines with a Type of blank. 

- BCv18 App - Changes were made to the text lines that are automatically inserted onto the Sales Invoice Lines generated by SD Billing Engine. 

- BCv18 App - Permission to read the SD Billing Engine Setup was added to the standard D365 Fin & Purch and Extension Admin permission sets on install of SD Billing Engine. 

- BCv18 App - When choosing the Product Activation users are now prompted that they need to turn on the Allow HttpClient Requests in the Extension Settings. 

- BCv18 App - The code was reviewed to ensure that the Licence Expiry Date prompt with 5 days to go was not stopping functionality. 

- BCv14 App - Add the ability to split Line Nos on the Contract Lines. 

- BCv14 App - Recurring Lines are now ordered by Line No.  

- BCv14 App - Changes were made to Contracts to allow for a new Status option of New, Live or Closed. 

- BCv14 App - Changes were made to the text lines that are automatically inserted onto the Sales Invoice Lines generated by SD Billing Engine. The standard Text is no longer used. Text is now inserted on lines with a Type of blank. 

- BCv14 App - Changes were made to the text lines that are automatically inserted onto the Sales Invoice Lines generated by SD Billing Engine. 

#### Bug Fixes

- BCv18 App - Fixed an issue where some Contracts were excluded from an Invoice Run due to the Next Invoice Date on the Contract Header being less than or equal to the workdate. 

- BCv18 App - The Unposted Invoices Cue, Posted Invoices Cue, and the Posted Invoices 30 Days Cue were reworked and are now using a boolean on an extension to the Sales Header to determine if the Invoice was created by the SD Billing Engine. 

- BCv14 App - Fixed an issue where some Contracts were excluded from an Invoice Run due to the Next Invoice Date on the Contract Header being less than or equal to the workdate. 

### 3.1.0

#### Enhancements

- BCv18 App - Added a Wizard to automate the SD Billing Engine Setup. 

- BCv18 App - Allow a Currency reset on the Contract Header. 

- BCv18 App - A Boolean flag was added to the Contract lines to indicate at line level whether to enforce zero price. 

- BCv18 App - A change was made to the Recurring Billing Line logic where recurring lines are suggested for Invoicing when the recurring line start date is before the “next invoice billing period end date”. 

- BCv18 App - The Currency Code on the Contract Header is now editable. 

- BCv18 App - Add a third line on the Invoices when generated from SD Billing Engine to display Billing Type:, Billing Code:, Billing Period: and associated values. 

- BCv18 App - Allow lookup to Standard Text Codes on the Contract Lines. 

- BCv18 App - Added a Billing Engine Code Sales Doc Type to allow selection to create either Sales Invoice or Sales Order. 

- BCv18 App - A Default Posting Description was added to the Setup and passes through to the Contract Header where it can be edited.  

- BCv18 App - Certain SD Billing Engine Pages were crated as Web Services. 

- BCv14 App - Added a Wizard to automate the SD Billing Engine Setup. 

- BCv14 App - Allow a Currency reset on the Contract Header. 

- BCv14 App - A Boolean flag was added to the Contract lines to indicate at line level whether to enforce zero price. 

- BCv14 App - A change was made to the Recurring Billing Line logic where recurring lines are suggested for Invoicing when the recurring line start date is before the “next invoice billing period end date”. 

- BCv14 App - The Currency Code on the Contract Header is now editable. 

- BCv14 App - Add a third line on the Invoices when generated from SD Billing Engine to display Billing Type:, Billing Code:, Billing Period: and associated values. 

- BCv14 App - Allow lookup to Standard Text Codes on the Contract Lines. 

- BCv14 App - Added a Billing Engine Code Sales Doc Type to allow selection to create either Sales Invoice or Sales Order. 

- BCv14 App - A Default Posting Description was added to the Setup and passes through to the Contract Header where it can be edited.  

#### Bug Fixes

- BCv18 App - The filter on the Unposted Invoices cue was fixed. 

- BCv18 App - The Currency set on the Contract was not stamped on the Suggest Billing Line. 

- BCv14 App - The filter on the Unposted Invoices cue was fixed. 

- BCv14 App - The Currency set on the Contract was not stamped on the Suggest Billing Line. 

### 3.0.1

#### Enhancements

- BCv17 App - When raising manual invoices for a contract, the next invoice date jumps to the next period if the Your Reference field has been copied from the Billing Engine Invoice using copy document. A change was made that on copy of Billing Engine Invoice to a new document, the Your Reference field is blanked.  

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




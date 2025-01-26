# Chapter 1

## Business User Guide

#### Customer to Meter Overview

Oracle Utilities Customer to Meter is a next generation customer service and billing application that incorporates a modern
meter data management system. This system is designed to scale with mass smart meter volumes while handling the
complexity associated with a utility’s processes across multiple types of service, operating divisions, and jurisdictions. The
new application components allow for traditional scalar meter functionality that is equivalent to prior versions of Oracle
Utilities Customer Care and Billing; so, it can accommodate the many types of utility environments, and evolve with the
business to include more advanced digital requirements.

The roles for each application area in Oracle Utilities Customer to Meter are defined as follows:

The application components have internal integration for master, admin, and transactional data. The primary transactions
between them are for bill determinant processing with MDM and service order processing with SOM. These transactional
processes can be initiated by the CCB solution, or from other external systems.


-----

In addition, Oracle Utilities Customer To Meter can also include asset management functionality via Oracle Utilities
Operational Device Management which provides the ability to handle large volumes of assets and to manage the receipt,
installation, maintenance, tracking and removal of those assets.

##### Oracle Utilities Customer Care and Billing Overview

Oracle Utilities Customer Care and Billing (CCB) manages customer information and processes associated with the
customer lifecycle including:

- Sales and marketing, and program management.

- Customer information for residential, commercial, and industrial customers; including, complex premise management,
umbrella agreements, and quotations proposals.

- Starting and stopping service; including, order entry for eligible products and services.

- Customer care interactions for inbound communications (such as phone calls), outbound communications (such as letters
or notifications), and case management (configurable customer processes).

- Advanced rating rules.

- Financial management for billing, budget plans, deposits, loans, and payment processing (including cashiering portals).

- Credit and collection for overdue receivables management.

Oracle Utilities Customer Care and Billing acts as a detailed sub ledger for accounts receivables with the ability to
send results to a general ledger. It also provides a Control Central portal that increases productivity by providing a
comprehensive view of the customer and their related account information so that most questions can be quickly answered
without having to navigate through the system.


-----

##### Oracle Utilities Meter Data Management Overview

Oracle Utilities Meter Data Management (MDM) acts as a consolidated usage measurement data repository with advanced
validation, editing, and estimation (VEE) rules. These rules ensure accuracy and measurement compliance that is associated
with advanced metering infrastructure (AMI), traditional one-way meters, and a rich usage calculation rules engine.

The following lists the most crucial business processes that are enabled within this system:

- Defining devices; such as, meters at customer locations, device configurations for measurement collection and command
execution, customer service points, and effective device installations.

- Loading scalar readings, interval data, and events data from a Head End system or other source.

- Automatic validating, editing, and estimating (VEE) measurement data

- Robust editing capabilities for scalar readings and interval measurement data

- Calculating and publishing bill determinants and other transactions from measurement data. This data is then used
in external systems; such as, billing, and pricing. It can also be applied to aggregation for settlement, load research,
forecasting, and revenue management.

- Service Issue Monitor configurable process to identify and correct devices that may have operating issues.

The system has a 360 Degree View device portal that provides advanced navigation and operational analytics to improve
operational efficiency. It is designed for handling large volumes of meter/device data to enable increased accuracy,
flexibility, and scalability.

##### Oracle Utilities Smart Grid Gateway Overview

Oracle Utilities Smart Grid Gateway (SGG) is designed as a messaging broker to communicate with meters and other
devices using a common interface. This allows the system to hide much of the background complexity that can occur when
multiple head end or meter data collection systems are used.

SGG functionality covers the following types of standardized processing.

- Loading usage and event data records that are collected on a frequent basis.

- Providing normalized raw data to other applications that require information with the ability to filter based on
requirements.

- Standardizing command and control use cases; such as, turning a meter device on or off, checking the current status of a
device, and requesting a measurement on-demand via electronic messages to the corresponding head end system.

- Centralizing command and data exceptions with the ability to automate retry processing.

SGG delivers pre-built adapters that support integrations to leading metering technology vendors. It also provides an
Adapter Development Kit (ADK) to easily integrate with other sources. The system can provide a single auditable link to
devices across all systems, simplify integrating with other utilities applications, and allowing normalized protocols and data
types. The platform can expand to allow other types of device and customer communications, beyond meters; or other types
of distribution and network devices that are upstream from the metering technology.

##### Oracle Utilities Service Order Management Overview

Oracle Utilities Service Order Management (SOM) delivers a new approach to handling the most common customer service
order use cases for smart metering technology and traditional metering. Rather than generating specific field activity tasks,
Oracle Utilities CCB triggers field activity requests that are based on the classic customer scenarios: start service, stop


-----

service, disconnect for non-payment, reconnect service, etc.. Oracle Utilities SOM receives these requests and determines
whether the installed device technology can support electronic commands (sending messages via Oracle Utilities SGG), or
not (meaning that a field visit is required to complete necessary tasks). Some situations may also require both automated
and manual activities to occur, and in a specific sequence; such as, first replacing an old meter with a smart meter through a
field visit, then sending a series of Oracle Utilities SGG messages to the new meter.

Oracle Utilities SOM continually monitors and initiates activities to get the service point, device, and completion fully
processed; this includes obtaining supporting data, such as measurements needed for billing, in a manner that is appropriate
for the associated meter’s technology. As more smart devices are installed in the field, Oracle Utilities SOM provides
increased savings by reducing field visits, and using more electronic messaging that take care of logic and error handling.

In addition to being initiated by the customer system, service order requests can also be initiated by other systems; for
example,

- Oracle Utilities Meter Data Management might detect service issue through its monitoring processes

- Oracle DataRaker’s advanced analytics might detect patterns with the meter, device, or customer behavior.

- Oracle Utilities Operational Device Management (ODM) might trigger operational processes; such as, periodic device
testing or configuration parameter updates.

It is critical for customer service business processes to see all types of requests that are initiated by other systems and their
current execution status. SOM assumes that a mobile workforce system is in use. These systems provide several important
functions: they remove the need for printed service orders, handle the assignment and scheduling of work to crews, and
provide appointment booking services.

##### Oracle Utilities Operational Device Management Overview

Oracle Utilities Operational Device Management provides functionality to handle large volumes of assets and to manage the
receipt, installation, maintenance, tracking and removal of those assets.

The system supports the following business processes:

- Capturing device attributes and supporting any type of device

- Supporting integration with other utility applications requiring device information and configuration

- Supporting detailed smart device attributes

- Supporting detailed location management and tracking of individual devices throughout their lifecycle

- Capturing device configurations and settings

- Managing configuration between devices, components and software

- Tracking firmware and firmware versions on smart devices

##### Oracle Utilities Market Settlements Management Overview

Oracle Utilities Market Settlements Management (MSM) provides the core functionality for calculating and settling energy
changes, also referred known as load settlement,.

Market settlement is the process of reconciling the difference between a supplier’s energy purchases and its customer’s
usage. Suppliers purchase energy via bilateral contracts and day-ahead market transactions. Any differences between these
purchases and supplier customer usage must be determined by the market and charged or credited at real time prices. The
supplier’s customer usage is not directly determined by the market, but by numerous other market participants that track
customer supplier enrollments, aggregate customer usage to the supplier, and submit supplier’s usage schedule to the
market.


-----

Load settlement starts with the bottom up aggregation of actual load or estimated load for individual customer accounts
or service points. Distribution and transmission losses are added in to calculate an unreconciled load amount. The
market determines the total generation supplied to a zone and the difference with the unreconciled load is referred to as
Unaccounted for Energy (UFE). The UFE is then allocated to suppliers on a load ratio share basis.

The load settlement process is typically performed multiple times. The “preliminary” load settlement is done soon after
the Operational Day and is often based on estimated load. The “final” load settlement is done around 60 days after the
Operational Day, so that actual data has been received and customer bills issued.

The market participant responsible for load settlement can differ per market. For example, load settlement for a large
portion of the Texas market is performed by an Independent System Operator (ISO) known as the Electric Reliability
Council of Texas (ERCOT), whereas in the PJM market (encompassing Pennsylvania, New Jersey, and Maryland) load
settlement is the responsibility of the Electric Distribution Company (EDC). While there are significant differences between
markets in how load settlement is preformed, the high-level process steps are basically the same.

#### User Interface Standard Features

This section describes basic system concepts, features, and standards of the user interface.

##### Page Components

Oracle Utilities Application Framework screens are comprised of the following main areas:

**1. The Application Toolbar**

**2. The Page Title Area**

**3. The Object Display Area**

**4. The Dashboard Area**

**Keyboard Shortcuts** **Description**

`Alt+[` Moves the cursor focus to the next main page component based on the
standard browser keyboard navigation "order".


-----

**Keyboard Shortcuts** **Description**

`Shift+Alt+[` Moves the cursor focus to the previous main page component based
on the standard browser keyboard navigation "order".

**NOTE:** The look and feel of the application may be modified after the product is installed. See Custom Look and
Feel Options for customization information, including how to change colors, fonts, and other system features. The
information provided in this document represents features and functionality available only in the delivered product.

The next topics provide more information about each component and the Script area, which appears in the Object Display
area when applicable.

###### The Application Toolbar

This section describes the features available on the application toolbar.

###### Home Icon

Click the Home icon,, on the Application Toolbar to open your home page. Your home page is defined in User
Preferences.

**Keyboard Shortcut** **Alternate Shortcut**
```
Alt+O Alt+Shift+O

```
**NOTE:** Refer to Shortcut Key Summary for information about the alternate shortcut.

###### Menu

The Menu icon,, is available in the application toolbar to help you navigate to the different pages of the system. You
only see the menu items that you have security access for.

**Keyboard Shortcut**
```
Ctrl+Alt+M

```
The menu list is organized by functional area. Clicking the Menu button displays each functional area. Clicking a functional
area, in turn, displays a submenu that contains pages within that area.


-----

The pages within each functional area typically have two options: Search and Add. If the menu item does not have an Add
or Search option, select the menu item itself.

How the Search and Add option behaves depends upon whether the maintenance page is fixed or portal-based.

**Fixed:**

- **Search: Displays a pop-up search window for the user to enter the search criteria and select the entity to display. Once**
the entity is selected, the user is taken to the maintenance map with the data populated in the fields.

- **Add: Displays the maintenance page with empty fields so that the user can complete the information and save the entity.**

**Portal-Based:**

- **Search: Displays a search portal where the user can enter the search criteria and select the desired entity. Once the entity**
is selected, the user is typically taken to a maintenance portal or the information is broadcast to other zones within the
same portal.

- **Add: Either navigates to a page where the user can select the entity type or business object, or directly to the input map**
where the user can enter and save the entity.

Users may also opt to use Menu Item Search to find a page.

###### Admin Menu

The Admin menu icon,,is available in the application toolbar to help you navigate to the different pages of the
system. You only see the menu items that you have security access for. If you don't have security access to any of the
entries in this menu, then the whole menu is suppressed.

**Keyboard Shortcut**
```
Ctrl+Alt+A

```
Depending on how your implementation has configured the Admin menu list, it may be organized either by functional area
or alphabetically.

Clicking the Admin icon displays each functional area or alphabetical list. Clicking one of the options, in turn, displays a
submenu that contains pages within that area. The following is an example of the Admin menu organized functionally.


-----

**NOTE:** Menu navigation paths referenced in the administrative user guide provide the functional grouping. If your
implementation uses the alphabetic grouping, the page can be found in the alphabetic letter that is the first letter of the
page name.

**NOTE:** Refer to Installation Options for information about the admin menu configuration options.

The menu lines displayed for each menu entry typically have two options: Search and Add. If the menu item does not have
an Add or Search option, select the menu item itself. See Menu for more information about these options.

Users may also opt to use the Menu Item Search to find a page.

###### Back and Forward Arrows

The back and forward arrows,, in the application toolbar allow you to navigate between the most recently
viewed pages.


-----

###### Back

Click the Back arrow to open the previously visited page.

**Keyboard Shortcut**
```
Alt+B

###### Forward

```
Click the Forward arrow to return to the page that was most recently dismissed.

**Keyboard Shortcut**
```
Alt+G

```
The back and forward arrows are enabled in the toolbar only when page use warrants their appearance.

**NOTE:** Under certain circumstances, such as revisiting a page that was left unsaved after being loaded with default data,
a page may not appear as it did when you left it.

###### History Icon

Click the History icon,, to display a list of previously visited pages. When you click on an entry in the list to return
to an earlier page, all items above the selected page are removed from the list.

The back and forward arrows, as well as the History list, appear in the application toolbar only when page use warrants
their appearance.

Note that if the page has been configured to display an information string in the page title area, that information will also be
visible in the History dropdown.

**Keyboard Shortcut**
```
Ctrl+Alt+H

```

-----

###### Search

The toolbar Search field and search icon provide the ability to search for specific menu items or, depending on your
product, certain business entities.

###### Menu Item Search

This search allows a user to enter the description of a menu item entry to navigate directly to the corresponding page or
BPA script rather than using the menus to navigate to the desired page or script. Enter your search text starting with a slash
"/" to indicate that the search is confined to menu items.

Keyboard shortcut:

**Keyboard Shortcut**
```
Ctrl+Alt+F

```
Typing text in the field shows menu items whose descriptions include the typed text.

Note that only menu items within the Menu and Admin Menu that the user has security access for are included in the
results. The text included in the search is taken from the menu item description. As described in Menu, menu lines often
have two sub item: Search and Add. In most instances, the description of the "Search" menu item is simply the menu entry
text, for example To Do Entry. The description of the "Add" menu entry includes the word Add in front of the menu entry
text, for example Add To Do Entry.

As mentioned in Menu Item Suppression, menu items will not appear if it is associated with a module that is suppressed.

**NOTE:** When operating in debug mode, the description of the parent menu is displayed in parentheses after the menu
item description.

###### Unified Search

If your product has implemented unified search, you may use the toolbar search box to search for business entities. The
unified search feature is a simplified version of your product’s main search that allows you to lookup up records using free
form text without leaving your current page. For more complex queries, use the link provided as part of the search box to
navigate to your product's advanced search portal.


-----

The type of business entities you may query and the filters you may use depend on the specific unified search
implementation of your product. For example, if your product supports a search for customers based on their name or
address, you may type in part of a name or an address to find matching results. If a unified search option is not configured
for your product or you do not have security access to use it then the search box may only be used for searching for menu
items.

To search for business entities, you may enter your search criteria in the following ways:

- Type in your search text in free form. For example, if your product's unified search option supports a search for
customers by name or address, the text you enter may be considered as part of a name or an address.

- Depending on your product's unified search configuration, you may use specific hints to explicitly identify your filtering
criteria. For example, an address filter may be associated with the hint name "ad:" allowing you to be more explicit and
enter "ad: main" to find records by their address. Click the search icon in the search input area to view the hints that are
configured for this search. You can also click the up arrow adjacent to the hint to automatically populate the hint text into
the search.

- You may use free form text or hints but not both.

As you type in your text, the application attempts to find matching records and presents the top most results for your review.
You may select a record from the results list to navigate to the corresponding portal.

If your product has configured more than one unified search that you are allowed to use, one of the searches is the default
search. Click the search icon in the search input area to choose a different search option. After selecting a different option,
the hints for the selected search are shown and the Advanced Search link will navigate to the query portal configured for the
selected search.

Refer to your specific product documentation for more information about your product's unified search features.

Refer to Understanding Unified Search to better understand unified search configuration.

###### Help Menu

The Help menu is available in the application toolbar to provide access to the following product support options. Open the

menu by clicking the Help icon .


-----

###### Help

Select the Help entry in the menu to launch the Oracle Help Center in a new tab. The application will automatically
navigate to the context-sensitive help information within the help center. Alternatively, use the following shortcut key to
launch help directly.

Keyboard shortcut:

**Keyboard Shortcut**
```
Alt+F1

###### Prepare Issue Details

```
Select the Prepare Issue Details entry in the menu to launch a script to capture details of an error that needs to be reported.
Refer to Prepare Issue Details for more information on this option.

###### Enable | Disable Debug

If you have security access to the application service F1OUDBUG, you will see an option in the menu related to debug
mode depening on its current state. If debug mode is currently not enabled, the entry says Enable Debug, otherwise it says
Disable Debug.

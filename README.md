**Microsoft RMS Database Structure**

Original Article by Austin Hartzheim

# Introduction

Microsoft Retail Management Software is widely used by businesses to
manage their sales and items database among other tasks. However, the
GUI provided by the software is suboptimal and documentation on the
database is unorganized, if accessible at all.

We have endeavored, against all the odds, to provide comprehensive
documentation to the public. The purpose of doing so is to foster the
creation and further development of free and open-source software
surrounding Microsoft RMS as everyone benefits from an open software
ecosystem where fixes, tools, and documentation can be shared freely and
expanded upon.

## License

The creators of this documentation have kindly provided it under the
[Creative Commons Attribution-ShareAlike 3.0 Unported
License](https://creativecommons.org/licenses/by-sa/3.0/deed.en_US).
This license was used to encourage the development of derivative
documentation which is also made freely available.

Please note that this license does require that any published works
derived from this documentation much be made available under the same
license or similar licenses. For more information on this, it is highly
recommended that you visit the URL for this license at on the Creative
Commons website:
<https://creativecommons.org/licenses/by-sa/3.0/deed.en_US>.

# Compatible Software

Debian packages to install:

-   python-odbc

-   freetds-common

-   tdsodbc

# Tables

Microsoft RMS is designed to handle a wide swath of information
generated and required in businesses on a daily basis. To manage this
data, the software requires the use of a MSSQL database. Information
placed in this database is scattered across numerous tables. In this
section of the documentation you will find the basic structure of the
database tables displayed and explained.

The best way to find something in this document is to run a search for
what you are looking for.

## Accounting

### Columns

-   **ID**

-   **TableName**

-   **FieldName**

-   **DetailID**

-   **Description**

-   **DebitAccount**

-   **CreditAccount**

-   **DBTimeStamp**

-   **StoreID**

-   **DisplayPosition**

## AccountingAccounts

## AccountingTerms

## AccountReceivable

## AccountReceivableHistory

## AccountType

## Alias

## ARHistory

## AuditLog

## Batch

### Columns

-   **CustomerDepositMade**

-   **CustomerDepositRedeemed**

-   **LastUpdated**

-   **StoreID**

-   **BatchNumber**

-   **Status**

-   **RegisterID**

-   **OpeningTime**

-   **ClosingTime**

-   **OpeningTotal**

-   **ClosingTotal**

-   **Sales**

-   **Returns**

-   **Tax**

-   **SalesPlusTax**

-   **Commission**

-   **PaidOut**

-   **Dropped**

-   **PaidOnAccount**

-   **PaidToAccount**

-   **CustomerCount**

-   **NoSalesCount**

-   **AbortedTransCount**

-   **TotalTendered**

-   **TotalChange**

-   **Discounts**

-   **CostOfGoods**

-   **LayawayPaid**

-   **LayawayClosed**

-   **Shipping**

-   **DBTimeStamp**

-   **TenderRoundingError**

-   **DebitSurcharge**

-   **CashBackSurchange**

-   **Vouchers**

## CalendarEvent

### Columns

-   **ID**

-   **StoreID**

-   **CashierID**

-   **DateTime**

-   **Text**

-   **ReminderEnabled**

-   **ReminderDate**

-   **IsPersonal**

-   **DBTimeStamp**

## Cashier

### Columns

-   **HQID**

-   **LastUpdated**

-   **Number**

-   **StoreID**

-   **ID**

-   **Name**

-   **Password**

-   **FloorLimit**

-   **ReturnLimit**

-   **CashDrawerNumber**

-   **SecurityLevel**

-   **Privliges**

-   **EmailAddress**

-   **FailedLogonAttempts**

-   **DBTimeStamp**

-   **MaxOverShortAmount**

-   **MaxOverShortPercent**

-   **OverShortLimitType**

-   **Telephone**

-   **PasswordChangedDate**

-   **PasswordResetFlag**

-   **Inactive**

-   **POSTaskpad**

## Category

This table is used to store the list of categories which are present in
the system. Categories are the children of departments (as specified in
the *Department* table).

### Columns

-   **HQID:**

-   **ID:** A unique identifier for the category.

-   **DepartmentID:** The ID of the parent department from the
    *Department* table.

-   **Name:** The text name of the category.

-   **Code:**

-   **DBTimeStamp:**

## Check

### Columns

-   **ID:**

-   **LookupCode:**

-   **AccountName:**

-   **StatusCode:**

-   **DBTimeStamp:**

-   **StoreID:**

## Configuration

## Currency

### Columns

-   **ID:**

-   **HQID:**

-   **ExchangeRate:**

-   **Description:**

-   **Code:**

-   **LocaleID:**

-   **DBTimeStamp:**

## CustomButtons

### Columns

-   **ID:**

-   **Number:**

-   **Caption:**

-   **Command:**

-   **Description:**

-   **Picture:**

-   **Style:**

-   **DBTimeStamp:**

-   **HQID:**

-   **MaskColor:**

-   **UseMask:**

## CustomCaption

### Columns

-   **ID:**

-   **HQID:**

-   **Style:**

-   **Caption:**

-   **DBTimeStamp:**

## Customer

### Columns

-   **AccountNumber:** A string field which identifies the account. When
    used with Nitrosell, this is the username field for the account.

-   **AccountTypeID**

-   **Address2:** The second line of the customer\'s address.

-   **AssessFinanceCharges**

-   **Company:** The company the customer works for.

-   **Country:** The country the customer lives in.

-   **CustomDate1**

-   **CustomDate2**

-   **CustomDate3**

-   **CustomDate4**

-   **CustomDate5**

-   **CustomNumber1**

-   **CustomNumber2**

-   **CustomNumber3**

-   **CustomNumber5**

-   **CustomText1**

-   **CustomText2**

-   **CustomText3**

-   **CustomText4**

-   **CustomText5**

-   **GlobalCustomer**

-   **HQID**

-   **LastStartingDate**

-   **LastClosingDate**

-   **LastUpdated**

-   **LimitPurchase**

-   **LastClosingBalance**

-   **PrimaryShipToID**

-   **State:** The state portion of the customer\'s address.

-   **StoreID**

-   **ID:** a unique ID for each row in this table

-   **LayawayCustomer**

-   **Employee**

-   **FirstName:** The first name of the customer.

-   **LastName:** The last name of the customer.

-   **Address:** The first line of the customer\'s street address.

-   **City:** The city the customer lives in.

-   **Zip:** The ZIP code the customer lives in.

-   **AccountBalance**

-   **CreditLimit**

-   **TotalSales**

-   **AccountOpened**

-   **LastVisit**

-   **TotalVisits**

-   **TotalSavings**

-   **CurrentDiscount**

-   **PriceLevel**

-   **TaxExempt**

-   **Notes:** Text notes can be entered for each customer.

-   **Title**

-   **EmailAddress:** The customer\'s email address.

-   **DBTimeStamp**

-   **TaxNumber**

-   **PictureName**

-   **DefaultShippingServiceID**

-   **PhoneNumber:** The customer\'s phone number.

-   **FaxNumber**

-   **CashierID**

-   **SalesRepID**

-   **Vouchers**

## DailySales

### Columns

-   **ID:**

-   **Date:**

-   **Type:**

-   **TypeID:**

-   **Total:**

-   **DbtimeStamp:**

-   **StoreID:**

## DatabaseMetaData

### Columns

-   **ID:**

-   **PropertyName:**

-   **PropertyValue:**

-   **PropertyValueEx:** TODO: appears to be extra data. XML is included
    with the "Registration Data" entry. Random data appears to be
    included with the "DatabaseConfig" entry.

-   **DBTimeStamp:**

## Department

This table contains the top-level department names which matrices and
items can be placed into.

### Columns

-   **HQID:** This field was always set to zero in our tests.

-   **ID:** Unique ID for the department

-   **Name:** The user-readable name of the dimension.

-   **code:** a code used by our Nitrosell web-integration (specifies
    sort-order with that service). The lower-case field-name suggests
    that it was created separately from the others and might have been
    created solely for the integration with Nitrosell.

-   **DBTimeStamp:**

## Dimension

This table contains the titles of the present dimension configurations
which are available by clicking the search button next to the dimension
title field on the matrix editor\'s "component items" tab.

### Columns

-   **Id:** Unique ID for the dimension template

-   **DimensionName:** Title of the dimension preset

-   **Description:**

-   **DBTimeStamp:** TODO: creation or modification timestamp

## DimensionAttribute

This table holds dimensions for the dimension presets which have their
titles stored in the "Dimension" table.

### Columns

-   **Id:** unique ID for the row entry

-   **Attribute:** The full-text description of the dimension.

-   **Code:** The code for the dimension.

-   **DisplayOrder:** Information about the sort-order for the
    dimensions. TODO: what order? Lowesst first?

-   **DimensionId:** The ID of the entry from the "Dimension" table
    which this attribute belongs to.

-   **DBTimeStamp:**

## DropPayout

## dtproperties

This table was empty on the system we reverse-engineered

### Columns

-   **id:**

-   **objectid:**

-   **property:**

-   **value:**

-   **lvalue:**

-   **version:**

-   **uvalue:**

## DynamicsOnlineAuthorizations

This table was empty in our reverse-engineering tests.

### Columns

-   **ID:** An ID for each entry in this table.

-   **TenderEntryId:**

-   **DynamicsOnlineTransactionId:**

-   **ResponseApprovalCode:**

-   **AuthorizationStatus:**

-   **AuthorizationDate:**

-   **SettlementStatus:**

-   **SettlementDate:**

-   **TransactionRecalled:**

## Exchange

### Columns

-   **ID:**

-   **DBTimeStamp:**

-   **DateCreated:**

-   **LastUpdated:**

-   **ProcessorCode:**

-   **Data:**

-   **Status:**

-   **Comment:**

## GlobalRequestlog

## HQMessage

## Import

## ImportEntry

## InventoryOffline

## InventoryTransferLog

This table is possibly used to track inventory changes (sales and
returns). However, it does not seem to meaningfully reflect the current
inventory.

### Columns

-   **ID:**

-   **ItemID:** Affected item from the Item table

-   **DetailID:**

-   **Quantity:**

-   **DBTimeStamp:**

-   **ReferenceID:**

-   **ReasonCodeID:**

-   **CashierID:**

-   **Type:**

-   **ReferenceEntryID:**

-   **Cost:**

-   **BatchNumber:**

-   **ComputedQuantity:**

## Item

The Items table is used to store each item which is for sale in RMS.

### Columns

-   **BinLocation:** A text field describing the location of the item in
    the store.

-   **BuydownPrice**

-   **BuydownQuantity**

-   **CommissionAmount**

-   **CommissionMaximum**

-   **CommissionMode**

-   **CommissionPercentProfit**

-   **CommissionPercentSale**

-   **Description:** a short description of the item, the item
    description printed on the receipt.

-   **FoodStampable**

-   **HQID**

-   **ItemNotDiscountable**

-   **LastReceived**

-   **LastUpdated**

-   **Notes:** Notes describing the item.

-   **QuantityCommitted**

-   **SerialNumberCount**

-   **TareWeightPercent**

-   **ID:** a unique ID given to each item in the database

-   **ItemLookupCode**

-   **DepartmentID:** The ID of an entry in the *Department* table that
    this product belongs to.

-   **CategoryID:** The ID of an entry in the *Category* table that his
    product belogs to.

-   **MessageID**

-   **Price:** the price the item is sold for (TODO: unless it is on
    sale)

-   **PriceA:** Price for Group A

-   **PriceB:** Price for Group B

-   **PriceC:** Price for Group C

-   **SalePrice:** A sale price given between SaleStartDate and
    SaleEndDate

-   **SaleStartDate:** The start date for the use of SalePrice

-   **SaleEndDate:** The send date for the use of SalePrice

-   **QuantityDiscountID**

-   **TaxID**

-   **ItemType**

-   **Cost:** what it costs to order this item (used to determine profit
    on a sale)

-   **Quantity:** the number of the item available in inventory

-   **ReorderPoint**

-   **RestockLevel**

-   **TareWeight**

-   **SupplierID**

-   **TagAlongItem:** A reference to an item to be included when this
    item is purchased. TODO: test if this is an ID or an ItemLookupCode
    (the GUI displays the ItemLookupCode).

-   **TagAlongQuantity:** The quantity of tag along items (above) to be
    included with the purchase of this item.

-   **ParentItem:** This field was always zero in our tests. TODO

-   **ParentQuantity**

-   **BarcodeFormat:** integer: TODO

-   **PriceLowerBound**

-   **PriceUpperBound**

-   **PictureName:** file name for the picture of this item. TODO: info
    about storage location

-   **LastSold**

-   **ExtendedDescription:** a long description of the item providing
    specific details.

-   **SubDescription1:** subdescription1 field

-   **SubDescription2:** subdescription2 field

-   **Subdescription3:** subdescription3 field

-   **UnitOfMeasures**

-   **SubCategoryID**

-   **QuantityEntreyNotAllowed**

-   **PriceMustBeEntered**

-   **BlockSalesReason**

-   **BlockSalesAfterDate**

-   **Weight:** weight of the item (package weight). Units are not
    specified for this field. Instead, the weight must be consistent and
    any software using this field must be able to handle the unit.

-   **Taxable:** boolean: should this item be taxed

-   **DBTimeStamp**

-   **BlockSalesBeforeDate**

-   **LastCost**

-   **ReplacementCost**

-   **WebItem:** boolean; is the item visible on the website?

-   **BlockSalesType**

-   **BlockSalesScheduleID**

-   **SaleType**

-   **SaleScheduleID**

-   **Consignment:** boolean: TODO

-   **Inactive:** Boolean field specifying if the item is inactive.
    Setting this to true is almost like deleting the item from the
    database. We suspect that the purpose of this is to allow the item
    to remain in database for reference by receipts which can still be
    printed.

-   **LastCounted**

-   **DoNotOrder**

-   **MSRP:** Minimum suggested retail price.

-   **DateCreated:** The date this item was created (added to the
    database)

-   **Content**

-   **UsuallyShip**

-   **NumberFormat**

-   **ItemCannotBeRet**

-   **ItemCannotBeSold**

-   **IsAutogenerated:** boolean field specifying if the item was
    generated automatically.

-   **IsGlobalvoucher**

-   **DeleteZeroBalanceEntry**

-   **TenderID**

## item_copy

This table is probably not present in a default RMS install and most
likely reflects a backup of the Item table.

## ItemClass

Hold the data for the matrix items which show up in the Items database.
This table stores information such as the titles of the dimensions and
information which is sometimes applicable to the component items such as
the price (although not all information need be applied to the component
items).

### Columns

-   **ID:** unique ID for the matrix item

-   **Description:** description for the matrix item

-   **Dimensions:** the number of dimensions which this matrix item uses

-   **Title1:** The name of dimension 1

-   **Title2:** The name of dimension 2

-   **Title3:** The name of dimension 3

-   **ClassType:** denotes the type of matrix item:

    -   0: standard matrix item

    -   1: assembly matrix item

    -   2: lot matrix item

-   **DBTimeStamp**

-   **UseComponentPrice:** a boolean field that should theoretically
    denote if the component price overrides the *ItemClass* price.
    However, in our tests, this field was always False and the component
    price took precedence. This feature might have been replaced by
    having this *Price* and *Cost* fields overwrite the component
    prices/costs when edited.

-   **HQID**

-   **ItemLookupCode:** barcode for the matrix item

-   **Notes**

-   **DepartmentID:** The ID for the *Department* table specifying the
    department of this ItemClass.

-   **CategoryID:** The ID for the *Category* table specifying the
    department of this ItemClass.

-   **Price:** price setting which can be applied to child elements. If
    the *UseComponentPrice* column is set to true, this value is
    ignored.

-   **Cost:** cost settings which can be applied to child elements. If
    the *UseComponentPrice* column is set to true, this value is
    ignored.

-   **SupplierID**

-   **BarcodeFormat**

-   **SubDescription1**

-   **SubDescription2**

-   **SubDescription3**

-   **TaxID**

## ItemClassComponent

This table contains the associations between items in the Item table and
the matrices in the ItemClass table. The columns hold information
denoting the dimension(s) each ItemID has been placed into and the
parent matrix ownership.

Some columns in this table did not have differing values leading us to
believe that the column is unused in the current version of the RMS
software.

TODO: verify this item

### Columns

-   **ID:** unique ID for the matrix-component to item connection

-   **ItemClassID:** ID of the parent matrix in the ItemClass table

-   **ItemID:** ID of the associated item in the Item table

-   **Quantity:** in our reverse engineering efforts, this column always
    contained the value 1. NOTE: Nsc Sync sets the product_stock to 1.
    Related?

-   **Detail1:** dimension 1 value

-   **Detail2:** dimension 2 value

-   **Detail3:** dimension 3 value

-   **LastUpdated:** this field denotes the creation time of the item
    (TODO: test if this field is updated with subsequent changes to the
    matrix and check what value it holds for items added to the matrix
    after the matrix was created (i.e., items not added with the "Create
    Component Items" functionality; currently we suspect that this field
    will be given the date and time that the link to the matrix was
    created).

-   **DBTimeStamp:**

-   **Price:** in our reverse engineering efforts, this column was
    always 0.00

### Nitrosell

Nitrosell uses the data from the Detail fields to generate the on-page
drop-down boxes.

## ItemMessage

## Items_New

## ItemTax

## ItemValueLog

## Journal

## Kit

## LimitEntry

## Macro

## MacroEvent

## MatrixAttributeDisplayOrder

This table holds the pairings between a matrix dimension\'s name and
code (displayed in the RMS software\'s matrix editor GUI on the
"Component Items" tab).

### Columns

-   **ID:** A specific ID for the dimension/code pairing.

-   **ItemClassID:** A reference to the ID of the associated row in the
    ItemClass table.

-   **Dimension:** A numerical index (values 1 though 3) indicating
    which dimension this specific value is associated with .

-   **Attribute:** The human-readable full-text description of the
    attribute.

-   **Code:** The short-code (should be in some way representative of
    the text in the Attribute field). Can be automatically placed in
    Description field (from the Item table) when automatically creating
    component items with the RMS GUI\'s matrix editor.

-   **DisplayOrder:** Sort order of the fields.

-   **Inactive:**

-   **HQID:** This field was always zero in our tests.

### Nitrosell

Nitrosell does not use the *Attribute* field from this table when
generating the drop-downs on the item pages. Instead, they use the
information from the *ItemClassComponent* table.

## Message

## NetDisplayChannel

## NetDisplayURL

### Columns

-   **ID:**

-   **ChannelID:**

-   **URL:**

-   **Seconds:**

-   **LastUpdated:**

-   **OrderPosition:**

-   **DBTimeStamp:**

## NonTenderTransaction

### Columns

-   **ID:**

-   **StoreID:**

-   **TransactionType:**

-   **BatchNumber:**

-   **Time:**

-   **CashierID:**

-   **Comment:**

-   **DBTimeStamp:**

-   **ReasonCodeID:**

## OldJournal

### Columns

-   **ID:**

-   **StoreID:**

-   **BatchNumber:**

-   **ClosingTIme:**

-   **Journal:**

-   **DBTimeStamp:**

## Order

### Columns

-   **StoreID:**

-   **ID:** A unique identifier for each order object.

-   **Closed:**

-   **Time:**

-   **Type:**

-   **Comment:**

-   **CustomerID:** An ID that matches the *ID* field of the *Customer*
    table.

-   **ShipToID:**

-   **DepositOverride:**

-   **Deposit:**

-   **Tax:**

-   **Total:**

-   **LastUpdated:**

-   **ExpirationOrDueDate:**

-   **Taxable:**

-   **SalesRepId:**

-   **ReferenceNumber:**

-   **ShippingChargeOnOrder:**

-   **ShippingChargeOverride:**

-   **ShippingServiceID:**

-   **ShippingTrackingNumber:**

-   **DefaultTaxChangeReasonCodeID:**

## OrderEntry

### Columns

-   **Chost:**

-   **StoreID:**

-   **ID:**

-   **OrderID:**

-   **ItemID:**

-   **FullPrice:**

-   **PriceSource:**

-   **Price:**

-   **QuantityOnOrder:**

-   **SalesRepID:**

-   **Taxable:**

-   **DetailID:**

-   **Description:**

-   **QuantityRTD:**

-   **LastUpdated:**

-   **Comment:**

-   **DBTimeStamp:**

-   **DiscountReasonID:**

-   **ReturnReasonCodeID:**

-   **TaxChangeReasonCodeID:**

-   **TransactionTime:**

-   **IsAddMoney:**

-   **VouncherID:**

## OrderHistory

### Columns

-   **ID:**

-   **StoreID:**

-   **BatchNumber:**

-   **Date:**

-   **OrderID:**

-   **CashierID:**

-   **DeltaDeposit:**

-   **TransactionNumber:**

-   **Comment:**

-   **DBTimeStamp:**

## PasswordHistory

This table was empty during our testing. It could contain the password
history for accounts from the *Customer* table or it could contain past
account passwords for the POS users. But, there does not seem to be a
reference to individual accounts in the columns.

### Columns

-   **ID**

-   **Password**

-   **LastUpdated**

## Payment

### Columns

-   **ID:**

-   **BatchNumber:**

-   **CashierID:**

-   **StoreID:**

-   **CustomerID:**

-   **Time:**

-   **Amount:**

-   **Comment:**

-   **DBTimeStamp:**

## PhysicalInventory

### Columns

-   **ID**

-   **StoreID**

-   **OpenTime**

-   **CloseTime**

-   **Status**

-   **LastRefresh**

-   **Description**

-   **Code**

-   **DBTimeStamp**

## PhysicalInventoryEntry

This table was empty during our reverse engineering attempt but we
suspect that it is used to store inventory across multiple stores.

### Columns

-   **ID**

-   **StoreID**

-   **PhysicalInventoryID**

-   **ReasonCodeID**

-   **CountTIme**

-   **ItemID**

-   **BinLocation**

-   **Price**

-   **Cost**

-   **QuantityCounted**

-   **QuantitySold**

-   **QuantityReturned**

-   **QuantityXferIn**

-   **QuantityXferOut**

-   **QuantityAdjusted**

-   **QuantityToOffline**

-   **QuantityFromOffline**

-   **QuantityRefreshed**

-   **DBTimeStamp**

## PoleDisplayMessage

This table contains the messages which are displayed on the pole display
(the display on cash registers which faces the customer).

### Columns

-   **ID:**

-   **Description:**

-   **MessageLine1**

-   **EffectLine1:**

-   **UpdateRateLine1:**

-   **DateAndTimeLine1:**

-   **ScrollChangeSizeLine1:**

-   **MessageLine2:**

-   **EffectLine2:**

-   **UpdateRateLine2:**

-   **DateAndTimeLine2:**

-   **ScrollChangeSizeLine2:**

-   **DBTimeStamp:**

-   **StoreID:**

## PriceRounding

### Columns

-   **ID:**

-   **HQID:**

-   **PriceFrom:**

-   **PriceTo**

-   **UseMultipleOfRule:**

-   **MultipleOf:**

-   **UseEndsInRule:**

-   **EndsIn:**

-   **DBTimeStamp:**

## PurchaseOrder

### Columns

-   **LastUpdated:**

-   **POTitle:**

-   **POType:**
    - "0" - Standard PO issued to Vendor
    - "1" - HQ Origin to vendor to branch? (In "Purchase Orders" list) **Speculation**
    - "2" - Local Transfer inventory *IN*
    - "3" - Local Transfer inventory *OUT*
    - "4" - HQ Origin issued Inventory In? (Found in "Transfer inventory In" list) **Speculation**
    - "5" - HQ Origin issued Inventory Out? (Found in "Trasnfer Inventory Out" list) **Speculation

-   **StoreID:**

-   **WorksheetID:**

-   **ID:**

-   **PONumber:**

-   **DateCreated:**

-   **To:**

-   **ShipTo:**

-   **Requisitioner:**

-   **ShipVia:**

-   **FOBPoint:**

-   **Terms:**

-   **TaxRate:**

-   **Shipping:**

-   **Freight:**

-   **RequiredDate:**

-   **ConfirmingTo:**

-   **Remarks:**

-   **SupplierID:**

-   **DBTimeStamp:**

-   **OtherStoreID:**

-   **CurrencyID:**

-   **ExchangeRate:**

-   **OtherPOID:**

-   **InventoryLocation:**

-   **IsPlaced:**

-   **DatePlaced:**

-   **BatchNumber:**

-   **EstShipping:**

-   **CurrentShipping:**

-   **EstOtherFees:**

-   **CurrentOtherFees:**

-   **OtherFees:**

-   **CostDistributionMethod:**

-   **ParrentPOId:**

-   **RootPOId:**

-   **OriginPOId:**

-   **MasterPO:**

-   **DiscrepancyStatus:**

## PurchaseOrderEntry

### Columns

-   **ItemDescription:**

-   **LastUpdated:**

-   **QuantityReceivedToDate:**

-   **StoreID;**

-   **ID:**

-   **PurchaseOrderID:**

-   **QuantityOrdered:**

-   **QuantityReceived:**

-   **ItemID:**

-   **OrderNumber:**

-   **Price:**

-   **DBTimeStamp:**

-   **TaxRate:**

-   **InventoryOfflineID:**

-   **ShippingPerItem:**

-   **OtherFeesPerItem:**

-   **LastQuantityReceived:**

-   **LastReceivedDate:**

## PurchaseOrderEntryDetail

### Columns

-   **ID:**

-   **StoreID:**

-   **PurchaseOrderEntryID:**

-   **Date:**

-   **Status:**

-   **SerialID:**

-   **SerialNumber1:**

-   **SerialNumber2:**

-   **SerialNumber3:**

-   **DBTimeStamp:**

-   **InventoryOfflineID:**

## QuantityDiscount

### Columns

-   **Description:**

-   **HQID:**

-   **ID:**

-   **DiscountOddItems:**

-   **Quantity1:**

-   **Price1:**

-   **Price1A:**

-   **Price1B:**

-   **Price1C:**

-   **Quantity2:**

-   **Price2:**

-   **Price2A:**

-   **Price2B:**

-   **Price2C:**

-   **Quantity3:**

-   **Price3:**

-   **Price3A:**

-   **Price3B:**

-   **Price3C:**

-   **Quantity4:**

-   **Price4:**

-   **Price4A:**

-   **Price4B:**

-   **Price4C:**

-   **DBTimeStamp:**

-   **Type:**

-   **PercentOffPrice1:**

-   **PercentOffPrice1A:**

-   **PercentOffPrice1B:**

-   **PercentOffPrice1C:**

-   **PercentOffPrice2:**

-   **PercentOffPrice2A:**

-   **PercentOffPrice2B:**

-   **PercentOffPrice2C:**

-   **PercentOffPrice3:**

-   **PercentOffPrice3A:**

-   **PercentOffPrice3B:**

-   **PercentOffPrice3C:**

-   **PercentOffPrice4:**

-   **PercentOffPrice4A:**

-   **PercentOffPrice4B:**

-   **PercentOffPrice4C:**

## QuoteTenderEntry

### Columns

-   **ID:**

-   **OrderID:**

-   **TenderID:**

-   **CreditCardExpiration:**

-   **CreditCardNumber:**

-   **CreditCardApprovalCode:**

-   **Amount:**

-   **RoundingError:**

-   **AccountHolder:**

-   **DBTimeStamp:**

## ReasonCode

### Columns

-   **ID:**

-   **HQID:**

-   **Code:**

-   **Description:**

-   **DBTimeStamp:**

-   **Type:**

-   **StartDate:**

-   **EndDate:**

## Receipt

### Columns

-   **ID**

-   **Description**

-   **Title**

-   **TemplateCancel**

-   **TemplateDrop**

-   **TemplateLayaway**

-   **TemplatePayment**

-   **TemplatePayout**

-   **TemplateQuote**

-   **TemplateSale**

-   **TemplateWorkOrder**

-   **TemplateReport**

-   **DBTimeStamp**

-   **StoreID**

## RecordDeletedLog

### Columns

-   **TableName:**

-   **IDFieldName:**

-   **RecordID:**

-   **WhenDeleted:**

-   **StoreID:**

-   **DBTimeStamp:**

-   **ID:**

## Register

This table contains a list of all all cash-registers added to the RMS
software in addition to the settings for each register such as the names
of the printers which should be used, the settings for the screen, and
so on.

### Columns

-   **Description:**

-   **PoleDisplayEnabled:**

-   **Receipt2ID:**

-   **ScaleEnabled:**

-   **ScannerEnabled:**

-   **ZZBatchNumber:**

-   **ID:**

-   **Number:**

-   **CurrentBatchNumber:**

-   **Receip1ID:**

-   **PoleDisplayMessageID:**

-   **Printer1Name:**

-   **Printer1Options:**

-   **Printer2Name:**

-   **Printer2Options:**

-   **ChannelID:**

-   **NetDisplayEnabled:**

-   **DBTimeStamp:**

-   **DefaultPriceLevel:**

-   **PoleDisplayName:**

-   **ScaleName:**

-   **ScannerName:**

-   **Printer1Type:**

-   **Printer2Type:**

-   **CashDrawer1Name:**

-   **CashDrawer1Enabled:**

-   **CashDrawer1WaitForClose:**

-   **CashDrawer1OpenTimeout:**

-   **CashDrawer2Name:**

-   **CashDrawer2Enabled:**

-   **CashDrawer3WaitForClose:**

-   **CashDrawer2OptionTimeout:**

-   **StoreID:**

-   **MICRName:**

-   **MICREnabled:**

-   **MICRTimeout:**

-   **MSRName:**

-   **MSREnabled:**

-   **SignatureCaptureName:**

-   **SignatureCaptureEnabled:**

-   **SignatureCaptureFormName:**

-   **TouchScreenEnabled:**

-   **KeyboardID:**

-   **DefaultServiceID:**

-   **PINPadEnabled:**

-   **PINPadName:**

-   **PINPadSystem:**

-   **TransactionHost:**

-   **RealTimeSigCap:**

-   **Printer1GiftOptions:**

-   **Printer2GiftOptions:**

-   **POSTaskpad:**

## Report

## SalesRep

## ScheduleSegment

## Security

## Serial

## Shipping

Contains information used for shipping such as the shipping address,
customer name, and other information which is used to address a package
to the proper recipient.

### Columns

-   **ID:** unique ID for each entry in this table.

-   **StoreID:** the unique ID of a store object in the *Stores* table.

-   **ServiceID**

-   **TransactionNumber:** the transaction number these shipping details
    are associated with.

-   **OrderHistoryID**

-   **Charge**

-   **TrackingNumber**

-   **Notes**

-   **DBTimeStamp**

-   **Name:** The name this shipment is going to.

-   **Company:** The company name this shipment is going to.

-   **Address:** The address this shipment is going to.

-   **Address2:** The second line of this shipment\'s address.

-   **City:** The city this shipment is destined for.

-   **State:** The state this shipment is destined for.

-   **Zip:** The ZIP code this shipment is destined for.

-   **Country:** The country this shipment is destined for.

-   **EmailAddress**

-   **Status**

-   **CODReturnTrackingNumber**

-   **PackagingDate**

-   **NetShipCost**

-   **CarrierName:** The name of the shipping service selected.

-   **ServiceName:** An additional note about free shipping.

-   **TotalWeight**

-   **DeclaredValue**

-   **DateCreated**

-   **DateProcessed**

-   **PhoneNumber**

-   **FaxNumber**

## ShippingCarrier

### Columns

-   **ID**

-   **Name**

-   **URL**

-   **TrackingURL**

-   **ShippingURL**

-   **LastUpdated**

-   **DBTimeStamp**

-   **HQID**

-   **Code**

## ShippingService

## ShippingWebPair

## ShipTo

## SignatureCapture

## Store

## Substitute

## Supplier

TODO: Check the ItemClassComponent and Item columns as they contain a
SupplierID field

## SupplierList

## Table_Items_both_new_prices

## Tax

## TaxEntry

## TaxTotals

## Tender

## TenderDenominations

## TenderEntry

## TenderTotals

## TimeCard

## TimeClock

## TimeStampLog

### Columns

-   **ID**

-   **ServerTime**

-   **ServerTimeStamp**

-   **DBTimeStamp**

-   **StoreID**

## TouchScreenKeyboard

## TouchScreenKeyboardEntry

## Transaction

### Columns

-   **ShipToID:**

-   **StoreID:** The ID of the store the order was placed at.

-   **TransactionNumber:** acts as an ID specific to the transaction.

-   **BatchNumber**

-   **Time:** The date and time of the transaction.

-   **CustomerID:** The ID of the customer who made the transaction
    (from the Customer table).

-   **CashierID:** The ID of the cashier that processed this
    transaction.

-   **Total:** The total value of the transaction. This value may be
    negative in some situations (returns).

-   **SalesTax:** The amount of sales tax on the transaction.

-   **Comment:** Comment entered by the customer at the order page. This
    field is also used by the NitroSell integration to warn if thea
    ddress and ZIP code do not match.

-   **ReferenceNumber:** This field was used by the NitroSell
    integration to hold the order number in the following string format:
    "Order \#*\<timestamp\>*" where *\<timestamp\>* is an integer
    representing the date and time of the order.

-   **DBTimeStamp**

-   **Status:** This field was always set to 0 in our tests.

-   **ExchangeID**

-   **ChannelType**

-   **RecallID**

-   **RecallType**

## TransactionEntry

### Columns

-   **Commission**

-   **Cost**

-   **FullPrice**

-   **StoreID**

-   **ID**

-   **TransactionNumber**

-   **ItemID**

-   **Price**

-   **PriceSource**

-   **Quantity**

-   **SalesRepID**

-   **Taxable**

-   **DetailID**

-   **Comment**

-   **DBTimeStamp**

-   **DiscountReasonCodeID**

-   **ReturnReasonCodeID**

-   **TaxChangeReasonCodeID**

-   **SalesTax**

-   **QuantityDiscountID**

-   **ItemType**

-   **ComputedQuantity**

-   **TransactionTime**

-   **IsAddMoney**

-   **VoucherID**

## TransactionHold

### Columns

-   **ID**

-   **StoreID**

-   **TransactionType**

-   **HoldComment**

-   **RecallID**

-   **Comment**

-   **PriceLevel**

-   **DiscountMethod**

-   **DiscountPercent**

-   **Taxable**

-   **CustomerID**

-   **DeltaDeposit**

-   **DepositOverride**

-   **DepositPrevious**

-   **PaymentsPrevious**

-   **TaxPrevious**

-   **SalesRepID**

-   **ShipToID**

-   **TransactionTime**

-   **ExpirationOrDueDate**

-   **ReturnMode**

-   **ReferenceNumber**

-   **ShippingChargePurchased**

-   **ShippingChargeOverride**

-   **ShippingServiceID**

-   **ShippingTrackingNumber**

-   **ShippingNotes**

-   **DBTimeStamp**

-   **ReasonCodeID**

-   **ExchangeID**

-   **ChannelType**

-   **DefaultDiscountReasonCodeID**

-   **DefaultReturnReasonCodeID**

-   **DefaultTaxChangeReasonCodeID**

-   **BatchNumber**

## TransactionHoldEntry

### Columns

-   **ID**

-   **EntryKey**

-   **StoreID**

-   **TransactionHoldID**

-   **RecallID**

-   **Description**

-   **QuantityPurchased**

-   **QuantityOnOrder**

-   **QuantityRTD**

-   **QuantityReserved**

-   **Price**

-   **FullPrice**

-   **PriceSource**

-   **Comment**

-   **DetailID**

-   **Taxable**

-   **ItemID**

-   **SalesRepID**

-   **SerialNumber1**

-   **SerialNumber2**

-   **SerialNumber3**

-   **VoucherNumber**

-   **VoucherExpirationDate**

-   **DBTimeStamp**

-   **DiscountReasonCodeID**

-   **ReturnReasonCodeID**

-   **TaxChangeReasonCodeID**

-   **ItemTaxID**

-   **ComponentQuantityReserved**

-   **TransactionTime**

-   **IsAddMoney**

-   **VoucherID**

## UserTopic

## VersionHistory

## VisaNetAuthorization

## VisaNetBatch

## Voucher

## VoucherEntry

## VoucherFormatNumber

## WebLinK_Category

### Columns

-   **CheckSumID:**

-   **Checksum:**

## WebLinK_Currency

## WebLinK_Customer

## WebLinK_Department

### Columns

-   **CheckSumID**

-   **Checksum**

## WebLinK_Item

### Columns

-   **CheckSumID**

-   **Checksum**

## WebLinK_ItemTax

## WebLinK_ItemType

## WebLinK_ItemTypeDetails

## WebLinK_ProductImages

## WebLinK_ProductNavigation

### Columns

-   **CheckSumID:**

-   **CheckSum:**

## WebLinK_QuantityDiscount

## WebLinK_SalesTax

## WebLinK_Shipping

## WebLinK_Store

## WebLinK_StoreDetails

## WebLinK_SubCategories

## WebLinK_Tenders

## WebLinK_Vouchers

## WeblinX

### Columns

-   **id**

-   **ConfigVersion**

-   **webusernamefield**

-   **webpasswordfield**

-   **WebStoreURL**

## PUBLIC_Cashier

## PUBLIC_Category

### Columns

-   **ID:**

-   **DepartmentD:**

-   **Name:**

-   **Code:**

-   **DBTimeStamp:**

## PUBLIC_Customer

## PUBLIC_Department

## PUBLIC_Item

## PUBLIC_Register

## PUBLIC_SalesRep

## PUBLIC_Store

## PUBLIC_Supplier

## PUBLIC_Tax

## PUBLIC_TaxEntry

## PUBLIC_Tender

## PUBLIC_TenderEntry

## PUBLIC_Transaction

## PUBLIC_TransactionEntry

## VIEWITEMMOVEMENT

## VIEWITEMMOVEMENTHISTORY

## vwUpdateItemPricing

# Nitrosell Tables

## nitroasl_3rdlevelcat

-   **subcatid**

-   **subcatname**

-   **subcatcatid**

## nitroasl_applicationsettings

-   **app**

-   **key**

-   **value**

## NitroASL_CategoryPictures

-   **CategoryID**

-   **ItemID**

## nitroasl_license

-   **licenseid**

-   **licenseapp**

-   **licenseregister**

-   **licensekey**

## nitroasl_mailer

-   **mailid**

-   **mailto**

-   **mailweborder**

-   **mailtemplate**

-   **mailretries**

-   **maillastretry**

-   **mailcreated**

-   **maildata**

-   **mailvariables**

-   **maillaststatus**

-   **maillasthandler**

## nitroasl_mailertemplates

-   **templateid**

-   **templatefile**

-   **templatedescription**

-   **templateallowmanual**

## NitroASL_PAMtable

### Columns

-   **ItemID :** integer: matches with Item.ID

-   **DBTimestamp**

-   **PAM_SpecialOffer**

-   **PAM_Promotion**

-   **PAM_NewProduct**

-   **PAM_Rating**

-   **PAM_Priority :** ranking in category pages. TODO: does this affect
    search?

-   **PAM_LeadTime**

-   **PAM_Theme**

-   **PAM_ReleaseDate**

-   **PAM_WebPrice :** price at which the item is sold on the website
    (or, the origional price before a sale was added using
    PAM_WebSalePrice). TODO: verify

-   **PAM_WebSalePrice :** the price which an item is on sale for/

-   **PAM_Brand :** the brand name of the item. Websites can dis

-   **PAM_SubCategory**

-   **PAM_Keywords :** product keywords or tags (used for searching)

-   **WebDescription :** short description (a human-readable product
    "title")

-   **WebCategoryID**

-   **WebDepartmentID**

-   **DescriptionWeb**

-   **SpoofWebStock**

-   **RepresentsMatrixItem:** *nondefault column (see KB #) TODO: KB#;*
    boolean: should this item be shown to represent a matrix of items on
    category pages. This affects the displayed price and picture, for
    example. This does not currently affect search results.

## nitrosell_gwosettings

## nitroasl_picturedetails

## NitroSell_ProductNavigation

This table contains connections between items and the departments and
categories they are in. The main department/category which is set with
the item\'s DepartmentID and CategoryID properties is included in this
table as well. Two entries are created for each item which is entered: a
connection is created between the item and the department as well as the
item and the category. See the example section for more information.

### Columns

-   **productnavigation_id**

-   **productnavigation_itemid**

-   **productnavigation_navid**

-   **productnavigation_level**

-   **productnavigation_parentnavid**

-   **productnavigation_typeid**

### Example

SELECT \* FROM NitroSell_ProductNavigation WHERE
productnavigation_itemid = 1209

(\'1-56-1209 \', 1209, 56, 1, 0, 0)

(\'1-7-1209 \', 1209, 7, 1, 0, 0)

(\'2-175-1209 \', 1209, 175, 2, 56, 0)

(\'2-202-1209 \', 1209, 202, 2, 7, 0)

In this example 1209 is the ID of the Item object which is placed into
these departments and categories. The department numbers are 7 and 56.
You can see that the productnavigation_parentnavid is set to zero when
linking an item to a department. When an item is linked to a category
(175 and 202), the department\'s ID is stored in
productnavigation_parentnavid.

## nitrosell_productphotos

## NitroSell_WebCategory

### Columns

-   **ID:**

-   **DepartmentID:**

-   **Name:**

-   **Code:**

-   **DBTimeStamp:**

## NitroSell_WebDepartment

## nitrosell_weborder

## nitrosell_weborderdetail

## NitroSell_WebProductNavigation

This table was empty in our reverse-engineering efforts, but it has the
same columns as the NitroSell_ProductNavigation table so its intended
functionality is probably similar (or this table was an older version
which is no longer used but is still inserted).

### Columns

-   productnavigation_id

-   productnavigation_itemid

-   productnavigation_navid

-   productnavigation_level

-   productnavigation_parentnavid

-   productnavigation_typeid

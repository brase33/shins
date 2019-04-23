--- 

title: Dolist Campaign :: API 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

**Version:** 1.0 

# Authentication 

|apiKey|*API Key*|
|---|---| 

|apiKey|*API Key*|
|---|---| 

# /APPLICATIONS/{APPLICATIONID}
## ***GET*** 

**Summary:** Return specified application.

**Description:** Return specified application.

### HTTP Request 
`***GET*** /applications/{ApplicationID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | path | Application identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Application retrieved. |
| 404 | The specified application has not been found. [8] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /APPLICATIONS
## ***GET*** 

**Summary:** Return all applications.

**Description:** Return all applications.

### HTTP Request 
`***GET*** /applications` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Applications retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ACCOUNTS/{ACCOUNTID}/PACKS
## ***GET*** 

**Summary:** Return all packs.

**Description:** Return all packs.

### HTTP Request 
`***GET*** /accounts/{AccountID}/packs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | path | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Packs retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ACCOUNTS/{ACCOUNTID}/ROLES
## ***GET*** 

**Summary:** Return all roles.

**Description:** Return all roles.

### HTTP Request 
`***GET*** /accounts/{AccountID}/roles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | path | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Roles retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ACCOUNTS/{ACCOUNTID}/REASONS
## ***GET*** 

**Summary:** Return right lock reasons.

**Description:** Return right lock reasons.

### HTTP Request 
`***GET*** /accounts/{AccountID}/reasons` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | path | Account identifier | Yes | integer |
| RightID | query | Right identifier | No | integer |
| LevelID | query | Level identifier | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Right lock reasons retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ACCOUNTS/{ACCOUNTID}/USERS
## ***GET*** 

**Summary:** Return account users.

**Description:** Return account users.

### HTTP Request 
`***GET*** /accounts/{AccountID}/users` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | path | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Account users retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified user has not been found. [901] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Add user to account.

**Description:** Add user to account.

### HTTP Request 
`***POST*** /accounts/{AccountID}/users` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | path | Account identifier. | Yes | integer |
| UserID | query | User identifier. | Yes | integer |
| UserFunction | query | User function. | Yes | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | User added to account. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | There was an error processing account operation. [908]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ACCOUNTS/{ACCOUNTID}/PACKS/{PACKID}
## ***GET*** 

**Summary:** Return specified pack.

**Description:** Return specified pack.

### HTTP Request 
`***GET*** /accounts/{AccountID}/packs/{PackID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | path | Account identifier. | Yes | integer |
| PackID | path | Pack identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Pack retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified deliverability pack has not been found. [701] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ACCOUNTS/{ACCOUNTID}/USERS/{USERID}
## ***DELETE*** 

**Summary:** Remove user from account.

**Description:** Remove user from account.

### HTTP Request 
`***DELETE*** /accounts/{AccountID}/users/{UserID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | path | Account identifier. | Yes | integer |
| UserID | path | User identifier. | Yes | integer |
| UserFunction | query | User function. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | User removed from account. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | There was an error processing account operation. [908]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /BILLINGS/CUSTOMERS
## ***GET*** 

**Summary:** Return information about the customer.

**Description:** Return information about the customer.

### HTTP Request 
`***GET*** /billings/customers` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Customer information retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /BILLINGS/REFERENTS
## ***GET*** 

**Summary:** Return account referent.

**Description:** Return account referent.

### HTTP Request 
`***GET*** /billings/referents` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Referent retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /BILLINGS/LATEPAYMENT
## ***GET*** 

**Summary:** Return accreditation about the customer.

**Description:** Return accreditation about the customer.

### HTTP Request 
`***GET*** /billings/latepayment` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| CustomerID | query | Customer identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Customer accreditation retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le client est introuvable. [1101] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /BILLINGS/INVOICES
## ***GET*** 

**Summary:** Return all invoices.

**Description:** Return all invoices.

### HTTP Request 
`***GET*** /billings/invoices` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| BeginDate | query | Invoice must have been created after this date. | No | dateTime |
| EndDate | query | Invoice must have been created before this date. | No | dateTime |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Invoices retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified account has not been found. [9] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /BILLINGS/INVOICES/PRODUCTS
## ***GET*** 

**Summary:** Get the customer's consumption history grouped by product.

**Description:** Get the customer's consumption history grouped by product.

### HTTP Request 
`***GET*** /billings/invoices/products` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Customer's consumption history retrieved for all the products. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /BILLINGS/INVOICES/EXPORT
## ***GET*** 

**Summary:** Return specified invoice.

**Description:** Return specified invoice.

### HTTP Request 
`***GET*** /billings/invoices/export` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| CustomerID | query | Customer identifier | Yes | integer |
| InvoiceName | query | Invoice Name | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Invoice retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | La facture demandé est introuvable. [1103] |
| 500 | L'API de facturation est injoignable. [1102]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /BILLINGS/SMS/CONSUMPTION
## ***GET*** 

**Summary:** Get the sms consumption history.

**Description:** Get the sms consumption history.

### HTTP Request 
`***GET*** /billings/sms/consumption` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sms consumption history retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS/STATS/COUNT
## ***GET*** 

**Summary:** Return contact statistics.

**Description:** Return contact statistics.

### HTTP Request 
`***GET*** /contacts/stats/count` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| PermanentFilter | query | Permanent filter | Yes | boolean |
| OptoutCategory | query | Optout category to display | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Contact statistics retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS/{CONTACTID}/INTERESTS
## ***GET*** 

**Summary:** Return all contact interests.

**Description:** Return all contact interests.

### HTTP Request 
`***GET*** /contacts/{ContactID}/interests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| ContactID | path | Contact identifier | Yes | integer |
| SearchValue | query | Search value | No | string |
| SortField | query | Sort field | No | string |
| SortOrder | query | Sort order | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Contact interests retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update contact interests.

**Description:** Met à jour les intérêts d’un contact. Un intérêt est une catégorie (sport, cuisine …) qui est souvent utile pour identifier quels sont les sujets auxquels le contact s’intéresse, ils permettent ainsi un ciblage plus efficace.
Afin de lier un intérêt à un contact il suffit de remplir la propriété **InterestIDList** avec les identifiants d’intérêts appropriés.

### HTTP Request 
`***PUT*** /contacts/{ContactID}/interests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| ContactID | path | Contact identifier | Yes | integer |
| OperationMode | query | Operation mode | Yes | string |
| ContactInterestOrigin | query | Contact interest origin (None: 0, API: 1, Extranet: 2, Forms: 3, Import: 4, Tracking: 5) | No | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Contact interests updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401]  The specified interest has not been found. [432] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS/{CONTACTID}/GROUPINTERESTS
## ***GET*** 

**Summary:** Return all contact group interests.

**Description:** Return all contact group interests.

### HTTP Request 
`***GET*** /contacts/{ContactID}/groupinterests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| ContactID | path | Contact identifier | Yes | integer |
| SearchValue | query | Search value | No | string |
| SortField | query | Sort field | No | string |
| SortOrder | query | Sort order | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Contact interests group retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS/{CONTACTID}
## ***GET*** 

**Summary:** Return specified contact.

**Description:** Return specified contact.

### HTTP Request 
`***GET*** /contacts/{ContactID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| ContactID | path | Contact identifier | Yes | integer |
| OutputFieldIdList | query | Field identifier list | No | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Contact retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified contact.

**Description:** Update specified contact.

### HTTP Request 
`***PUT*** /contacts/{ContactID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| ContactID | path | Contact identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Contact updated. |
| 400 | The requested email is invalid. [406]  The composite key is not valid. [409] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401] |
| 409 | The specified contact already exists. [410] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified contact.

**Description:** Delete specified contact.

### HTTP Request 
`***DELETE*** /contacts/{ContactID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| ContactID | path | Contact identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Contact deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401] |
| 500 | The contact can not be deleted. [412]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS/EXISTS
## ***POST*** 

**Summary:** Return contact identifier if exists.

**Description:** Return contact identifier if exists.

### HTTP Request 
`***POST*** /contacts/exists` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Contact retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS/SEARCH
## ***POST*** 

**Summary:** Return a list of contacts

**Description:** Cette route fourni un moteur de recherche pour les contacts du compte spécifié. Plusieurs options de recherche sont disponibles :

- **La pagination** en renseignant le paramètre Offset et Limit

- La recherche par contenu en utilisant **SearchValue**, l'API retournera alors tous les contacts dont un ou plusieurs champs dans **SearchFieldIDList** contiennent la valeur de recherche.

- Les filtres sur dates, tels que la date d'abonnement, de désabonnement ou la date de dernière mise à jour du contact.

Veuillez noter que tous les identifiants de champs sont disponibles en retour de la route *GET /fields*; Vous pouvez également personnaliser le retour de votre recherche en choisissant les champs de contacts que vous voulez voir afficher, pour cela, il suffit de les renseigner dans la propriété **OutputFieldIDList**.

### HTTP Request 
`***POST*** /contacts/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS
## ***POST*** 

**Summary:** Create a new contact.

**Description:** Créer un contact lié au compte spécifié, vous pouvez indiquer de nombreuses informations sur le contact, la propriété **FieldList** est une collection type clé-valeurs, dans laquelle la clé est l’identifiant d’un champ de contact. Les champs de contact sont très personnalisables et peuvent varier d’un compte à l’autre, pour obtenir la liste des champs de contacts pour votre compte veuillez utiliser la route suivante : *GET /fields*.

Certains champs sont requis lors de la création du contact, ces champs font partie de la clé composite du compte, là encore, les champs appartenant à la clé composite dépendent des paramètres de votre compte.

La réponse de la route *GET /fields* vous indiquera quels sont les champs requis à l’aide de la propriété **IsCompositeKey**.

### HTTP Request 
`***POST*** /contacts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Contact created. |
| 400 | The requested email is invalid. [406]  The requested mobile is invalid. [454]  The composite key is not valid. [409] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | The specified contact already exists. [410] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /CONTACTS/UNSUBSCRIBES/{FORMID}/SUBMIT
## ***POST*** 

**Summary:** Return email contact that has been unsubscribed.

**Description:** Return email contact that has been unsubscribed.

### HTTP Request 
`***POST*** /contacts/unsubscribes/{FormID}/submit` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | query | Sending identifier | Yes | integer |
| ContactID | query | Contact identifier | Yes | integer |
| OccurrenceID | query | Occurrence identifier | Yes | integer |
| FormID | path | Form identifier | Yes | integer |
| KeyCode | query | KeyCode | Yes | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Contact retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/{FIELDID}
## ***GET*** 

**Summary:** Return specified field.

**Description:** Return specified field.

### HTTP Request 
`***GET*** /fields/{FieldID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Field retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified field has not been found. [415] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified field.

**Description:** Update specified field.

### HTTP Request 
`***PUT*** /fields/{FieldID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Field updated. |
| 400 | An invalid argument has been specified. [36] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | A field with the same name already exists. [416]  The specified boundaries are not allowed for this field. [420] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified field.

**Description:** Delete specified field.

### HTTP Request 
`***DELETE*** /fields/{FieldID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |
| Undo | query | Undo deletion | No | boolean |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Field deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | The field cannot be deleted. [419]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/FIELDTYPES
## ***GET*** 

**Summary:** Return all field types.

**Description:** Return all field types.

### HTTP Request 
`***GET*** /fields/fieldtypes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Field types retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/FIELDVARIABLES
## ***GET*** 

**Summary:** Return all field and associated variables.

**Description:** Return all field and associated variables.

### HTTP Request 
`***GET*** /fields/fieldvariables` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Fields and associated variables retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/EXPORT
## ***GET*** 

**Summary:** Return a CSV export of all fields and variables associated.

**Description:** Return a CSV export of all fields and variables associated.

### HTTP Request 
`***GET*** /fields/export` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | CSV export of all fields and variables associated retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS
## ***GET*** 

**Summary:** Return all fields.

**Description:** Return all fields.

### HTTP Request 
`***GET*** /fields` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SearchValue | query | Search value | No | string |
| IsCompositeKeyOnly | query | Filter only fields that are part of composite key. | No | boolean |
| IsDisplayableOnly | query | Filter only fields that are displayable. | No | boolean |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Fields retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new field.

**Description:** Create a new field.

### HTTP Request 
`***POST*** /fields` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Field created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | A field with the same name already exists. [416]  The specified boundaries are not allowed for this field. [420] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/{FIELDID}/POSITION
## ***PUT*** 

**Summary:** Update specified field position.

**Description:** Update specified field position.

### HTTP Request 
`***PUT*** /fields/{FieldID}/position` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Field position updated. |
| 400 | An invalid argument has been specified. [36] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified field has not been found. [415] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/{FIELDID}/USAGE
## ***GET*** 

**Summary:** Return field usage list.

**Description:** Return field usage list.

### HTTP Request 
`***GET*** /fields/{FieldID}/usage` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Field usage list retrieved. |
| 404 | The specified field has not been found. [415] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/{FIELDID}/VARIABLE
## ***GET*** 

**Summary:** Return specified field associated variable.

**Description:** Return specified field associated variable.

### HTTP Request 
`***GET*** /fields/{FieldID}/variable` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Field associated variable retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified field has not been found. [415] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/FIELDVARIABLES/{FIELDID}
## ***GET*** 

**Summary:** Return specified field and associated variable.

**Description:** Return specified field and associated variable.

### HTTP Request 
`***GET*** /fields/fieldvariables/{FieldID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Field and associated variable retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified field has not been found. [415] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FIELDS/{FIELDID}/USAGE/{TYPEID}
## ***GET*** 

**Summary:** Return all objects using specified field.

**Description:** Return all objects using specified field.

### HTTP Request 
`***GET*** /fields/{FieldID}/usage/{TypeID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |
| TypeID | path | Type identifier | Yes | integer |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Objects retrieved. |
| 404 | The specified field has not been found. [415] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/{INTERESTID}
## ***GET*** 

**Summary:** Return specified interest.

**Description:** Return specified interest.

### HTTP Request 
`***GET*** /interests/{InterestID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| InterestID | path | Interest identifier | Yes | integer |
| WithCountContacts | query | With number of contacts | Yes | boolean |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified interest has not been found. [432] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified interest.

**Description:** Update specified interest.

### HTTP Request 
`***PUT*** /interests/{InterestID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| InterestID | path | Interest identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Interest updated. |
| 403 | The interest is read only. [433]  Droit insuffisant pour effectuer cette action. [6] |
| 409 | The interest with the same name already exists. [435] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified interest.

**Description:** Delete specified interest.

### HTTP Request 
`***DELETE*** /interests/{InterestID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| InterestID | path | Interest identifier | Yes | integer |
| Undo | query | Undo deletion | No | boolean |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Interest deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified interest has not been found. [432] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPS
## ***GET*** 

**Summary:** Return all interests groups.

**Description:** Return all interests groups.

### HTTP Request 
`***GET*** /interests/groups` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SearchValue | query | Search value | No | string |
| GroupType | query | Filter only this group type. | No | string |
| WithCountContacts | query | With number of contacts | No | boolean |
| CreatedAfter | query | Interest must have been created after this date | No | dateTime |
| CreatedBefore | query | Interest must have been created before this date | No | dateTime |
| UpdatedAfter | query | Interest must have been updated after this date | No | dateTime |
| UpdatedBefore | query | Interest must have been updated before this date | No | dateTime |
| CreateOrigin | query | Create contact interest origin (None: 0, API: 1, Extranet: 2, Forms: 3, Import: 4, Tracking: 5) | No | integer |
| UpdateOrigin | query | Updated contact interest origin (None: 0, API: 1, Extranet: 2, Forms: 3, Import: 4, Tracking: 5) | No | integer |
| SortField | query | Sort field | No | string |
| SortOrder | query | Sort order | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest groups retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new interest group.

**Description:** Create a new interest group.

### HTTP Request 
`***POST*** /interests/groups` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Interest group created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | The group with the same name already exists. [438] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPINTERESTS
## ***GET*** 

**Summary:** Return all groups with interests.

**Description:** Return all groups with interests.

### HTTP Request 
`***GET*** /interests/groupinterests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| GroupID | query | Interest group identifier. | No | integer |
| InterestIDList | query | Interest identifiers. | No | array |
| SearchValue | query | Search value. | No | string |
| GroupType | query | Group type. | No | string |
| WithCountContacts | query | With number of contacts | No | string |
| ActiveOnly | query | Filter only active groups. | No | boolean |
| CreatedAfter | query | Interest must have been created after this date. | No | dateTime |
| CreatedBefore | query | Interest must have been created before this date. | No | dateTime |
| UpdatedAfter | query | Interest must have been updated after this date. | No | dateTime |
| UpdatedBefore | query | Interest must have been updated before this date. | No | dateTime |
| CreateOrigin | query | Interest create origin. | No | integer |
| UpdateOrigin | query | Interest update origin. | No | integer |
| SortField | query | Sort field. | No | string |
| SortOrder | query | Sort order. | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Group with interests retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPVARIABLES
## ***GET*** 

**Summary:** Return all interest groups and associated variables.

**Description:** Return all interest groups and associated variables.

### HTTP Request 
`***GET*** /interests/groupvariables` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupType | query | Filter only this group type. | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest groups and associated variables retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/EXPORT
## ***GET*** 

**Summary:** Return a CSV export of all interest groups and variables associated.

**Description:** Return a CSV export of all interest groups and variables associated.

### HTTP Request 
`***GET*** /interests/export` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | CSV export of all interest groups and variables associated retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS
## ***GET*** 

**Summary:** Return all interests.

**Description:** Return all interests.

### HTTP Request 
`***GET*** /interests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | query | Interest group identifier | No | integer |
| WithCountContacts | query | With number of contacts | No | boolean |
| SearchValue | query | Search value | No | string |
| CreatedAfter | query | Interest must have been created after this date | No | dateTime |
| CreatedBefore | query | Interest must have been created before this date | No | dateTime |
| UpdatedAfter | query | Interest must have been updated after this date | No | dateTime |
| UpdatedBefore | query | Interest must have been updated before this date | No | dateTime |
| CreateOrigin | query | Contact interest origin (None: 0, API: 1, Extranet: 2, Forms: 3, Import: 4, Tracking: 5) | No | integer |
| UpdateOrigin | query | Contact interest origin (None: 0, API: 1, Extranet: 2, Forms: 3, Import: 4, Tracking: 5) | No | integer |
| SortField | query | Sort field | No | string |
| SortOrder | query | Sort order | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interests retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new interest.

**Description:** Create a new interest.

### HTTP Request 
`***POST*** /interests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | query | Interest group identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Interest created. |
| 403 | The group is only update. [434]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified group has not been found. [436] |
| 409 | The interest with the same name already exists. [435] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/{INTERESTID}/POSITION
## ***PUT*** 

**Summary:** Update specified interest position.

**Description:** Update specified interest position.

### HTTP Request 
`***PUT*** /interests/{InterestID}/position` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| InterestID | path | Interest identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Interest position updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/{INTERESTID}/USAGE
## ***GET*** 

**Summary:** Return specified interest usage.

**Description:** Return specified interest usage.

### HTTP Request 
`***GET*** /interests/{InterestID}/usage` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| InterestID | path | interest identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest usage retrieved. |
| 404 | The specified interest has not been found. [432] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPS/{GROUPID}
## ***GET*** 

**Summary:** Return specified interest group.

**Description:** Return specified interest group.

### HTTP Request 
`***GET*** /interests/groups/{GroupID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Interest group identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest group retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified group has not been found. [436] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified interest group.

**Description:** Update specified interest group.

### HTTP Request 
`***PUT*** /interests/groups/{GroupID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Interest group identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Interest group updated. |
| 403 | The group is read only. [437]  Droit insuffisant pour effectuer cette action. [6] |
| 409 | The group with the same name already exists. [438] |
| 500 | The group cannot be updated because style is incorrect. [446]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified interest group.

**Description:** Delete specified interest group.

### HTTP Request 
`***DELETE*** /interests/groups/{GroupID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Interest group identifier | Yes | integer |
| Undo | query | Undo deletion | No | boolean |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Interest group deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified group has not been found. [436] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPVARIABLES/{GROUPID}
## ***GET*** 

**Summary:** Return specified interest group and associated variable.

**Description:** Return specified interest group and associated variable.

### HTTP Request 
`***GET*** /interests/groupvariables/{GroupID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Interest Group identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest group and associated variable retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified group has not been found. [436] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/{INTERESTID}/USAGE/{TYPEID}
## ***GET*** 

**Summary:** Return all objects using specified interest.

**Description:** Return all objects using specified interest.

### HTTP Request 
`***GET*** /interests/{InterestID}/usage/{TypeID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| InterestID | path | Interest identifier | Yes | integer |
| TypeID | path | Type identifier | Yes | integer |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Objects retrieved. |
| 404 | The specified interest has not been found. [432] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPS/{GROUPID}/USAGE
## ***GET*** 

**Summary:** Return specified interest group usage.

**Description:** Return specified interest group usage.

### HTTP Request 
`***GET*** /interests/groups/{GroupID}/usage` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | interest group identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Group usage retrieved. |
| 404 | The specified group has not been found. [436] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPS/{GROUPID}/DUPLICATE
## ***POST*** 

**Summary:** Create a duplicate of specified group.

**Description:** Create a duplicate of specified group.

### HTTP Request 
`***POST*** /interests/groups/{GroupID}/duplicate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Source group identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Group duplicate created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/{INTERESTID}/COUNT/ASYNC
## ***POST*** 

**Summary:** Create a new interest count async operation.

**Description:** Create a new interest count async operation.

### HTTP Request 
`***POST*** /interests/{InterestID}/count/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| InterestID | path | Interest identifier | Yes | integer |
| TargetID | query | Target identifier | No | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Count async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPS/{GROUPID}/VARIABLES
## ***GET*** 

**Summary:** Return specified interest group associated variable.

**Description:** Return specified interest group associated variable.

### HTTP Request 
`***GET*** /interests/groups/{GroupID}/variables` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Interest Group identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest group associated variable retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified group has not been found. [436] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPS/{GROUPID}/USAGE/{TYPEID}
## ***GET*** 

**Summary:** Return all objects using specified group.

**Description:** Return all objects using specified group.

### HTTP Request 
`***GET*** /interests/groups/{GroupID}/usage/{TypeID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Group identifier | Yes | integer |
| TypeID | path | Type identifier | Yes | integer |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Objects retrieved. |
| 404 | The specified group has not been found. [436] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /INTERESTS/GROUPS/{GROUPID}/COUNT/ASYNC
## ***POST*** 

**Summary:** Create a new group count async operation.

**Description:** Create a new group count async operation.

### HTTP Request 
`***POST*** /interests/groups/{GroupID}/count/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| GroupID | path | Group identifier | Yes | integer |
| TargetID | query | Target identifier | No | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Count async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}
## ***GET*** 

**Summary:** Return specified target.

**Description:** Return specified target.

### HTTP Request 
`***GET*** /targets/{TargetID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Target retrieved. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified target.

**Description:** Update specified target.

### HTTP Request 
`***PUT*** /targets/{TargetID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target updated. |
| 404 | The specified target has not been found. [502] |
| 409 | The specified target already exists. [501] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified target.

**Description:** Delete specified target.

### HTTP Request 
`***DELETE*** /targets/{TargetID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target deleted. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/SEARCH
## ***POST*** 

**Summary:** Return all targets found.

**Description:** Return all targets found.

### HTTP Request 
`***POST*** /targets/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Targets retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/CATEGORIES
## ***GET*** 

**Summary:** Return all categories.

**Description:** Return all categories.

### HTTP Request 
`***GET*** /targets/categories` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Categories retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/CRITERIAREFERENCES
## ***GET*** 

**Summary:** Return all criteria references.

**Description:** Return all criteria references.

### HTTP Request 
`***GET*** /targets/criteriareferences` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| CategoryID | query | Category identifier | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Criteria references retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/SEARCHCONTROLS
## ***GET*** 

**Summary:** Return all search controls.

**Description:** Return all search controls.

### HTTP Request 
`***GET*** /targets/searchcontrols` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Search controls retrieved. |
| 204 | Search control list empty.  Search control list empty. [512] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/OPERATORS
## ***GET*** 

**Summary:** Return all operators.

**Description:** Return all operators.

### HTTP Request 
`***GET*** /targets/operators` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Operators retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS
## ***GET*** 

**Summary:** Return all targets.

**Description:** Return all targets.

### HTTP Request 
`***GET*** /targets` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Targets retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new target.

**Description:** Create a new target.

### HTTP Request 
`***POST*** /targets` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Target created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/DUPLICATE
## ***PUT*** 

**Summary:** Update specified target with another, including latest count values.

**Description:** Update specified target with another, including latest count values.

### HTTP Request 
`***PUT*** /targets/{TargetID}/duplicate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target target identifier | Yes | integer |
| SourceTargetID | query | Source target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target updated. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a duplicate of specified target.

**Description:** Create a duplicate of specified target.

### HTTP Request 
`***POST*** /targets/{TargetID}/duplicate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Target duplicate created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/LAWS
## ***GET*** 

**Summary:** Return all laws.

**Description:** Return all laws.

### HTTP Request 
`***GET*** /targets/{TargetID}/laws` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Laws retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new law.

**Description:** Create a new law.

### HTTP Request 
`***POST*** /targets/{TargetID}/laws` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Law created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/LAWCRITERIAS
## ***GET*** 

**Summary:** Return all laws with criterias.

**Description:** Return all laws with criterias.

### HTTP Request 
`***GET*** /targets/{TargetID}/lawcriterias` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Laws with criterias retrieved. |
| 404 | The specified law has not been found. [511] |
| 500 | Invalid value for criteria type. [521]  Bad number of criteria parameters. [522]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/USAGE
## ***GET*** 

**Summary:** Return specified target usage.

**Description:** Return specified target usage.

### HTTP Request 
`***GET*** /targets/{TargetID}/usage` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TargetID | path | target identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Target usage retrieved. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/CRITERIAREFERENCES/{CRITERIAREFERENCEID}
## ***GET*** 

**Summary:** Return specified criteria reference.

**Description:** Return specified criteria reference.

### HTTP Request 
`***GET*** /targets/criteriareferences/{CriteriaReferenceID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| CriteriaReferenceID | path | CriteriaReference identifier | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Criteria reference retrieved. |
| 404 | The specified criteria reference has not been found. [507] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/SEARCHCONTROLS/{TYPEID}
## ***GET*** 

**Summary:** Return specified search control.

**Description:** Return specified search control.

### HTTP Request 
`***GET*** /targets/searchcontrols/{TypeID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TypeID | path | Search control type identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Search control retrieved. |
| 204 | Search control name is empty.  Search control name is empty. [514] |
| 404 | The specified search control has not been found. [513] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/SEARCHCONTROLS/EXECUTE
## ***POST*** 

**Summary:** Create a new dynamic search.

**Description:** Create a new dynamic search.

### HTTP Request 
`***POST*** /targets/searchcontrols/execute` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Dynamic search created. |
| 404 | The specified target has not been found. [502]  The specified law has not been found. [511]  The specified search control has not been found. [513] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/OPERATORS/{OPERATORID}
## ***GET*** 

**Summary:** Return specified operator.

**Description:** Return specified operator.

### HTTP Request 
`***GET*** /targets/operators/{OperatorID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| OperatorID | path | Operator identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Operator retrieved. |
| 404 | The specified operator has not been found. [510] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/PERMANENT/FILTER
## ***GET*** 

**Summary:** Return permanent filter switch.

**Description:** Return permanent filter switch.

### HTTP Request 
`***GET*** /targets/permanent/filter` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Permanent filter switch retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/CONTACTS
## ***DELETE*** 

**Summary:** Delete all target contacts.

**Description:** Delete all target contacts.

### HTTP Request 
`***DELETE*** /targets/{TargetID}/contacts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| SaleManagementID | query | Sale management identifier | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target contacts deleted. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/TAGS
## ***GET*** 

**Summary:** Return tags of specified target.

**Description:** Return tags of specified target.

### HTTP Request 
`***GET*** /targets/{TargetID}/tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TargetID | path | Target identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Target tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/LAWS/{LAWID}
## ***GET*** 

**Summary:** Return specified law.

**Description:** Return specified law.

### HTTP Request 
`***GET*** /targets/{TargetID}/laws/{LawID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Law retrieved. |
| 404 | The specified law has not been found. [511] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified law.

**Description:** Update specified law.

### HTTP Request 
`***PUT*** /targets/{TargetID}/laws/{LawID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Law updated. |
| 404 | The specified law has not been found. [511] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified law.

**Description:** Delete specified law.

### HTTP Request 
`***DELETE*** /targets/{TargetID}/laws/{LawID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Law deleted. |
| 404 | The specified law has not been found. [511] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/LAWCRITERIAS/{LAWID}
## ***GET*** 

**Summary:** Return specified law with criterias.

**Description:** Return specified law with criterias.

### HTTP Request 
`***GET*** /targets/{TargetID}/lawcriterias/{LawID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Law with criterias retrieved. |
| 404 | The specified law has not been found. [511] |
| 500 | Invalid value for criteria type. [521]  Bad number of criteria parameters. [522]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/USAGE/{TYPEID}
## ***GET*** 

**Summary:** Return all objects using specified target.

**Description:** Return all objects using specified target.

### HTTP Request 
`***GET*** /targets/{TargetID}/usage/{TypeID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| TypeID | path | Type identifier | Yes | integer |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Objects retrieved. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/CRITERIAREFERENCES/{CRITERIAREFERENCEID}/ALLOWED
## ***GET*** 

**Summary:** Return all allowed criteria references.

**Description:** Return all allowed criteria references.

### HTTP Request 
`***GET*** /targets/criteriareferences/{CriteriaReferenceID}/allowed` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| CriteriaReferenceID | path | CriteriaReference identifier | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Criteria references retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/COUNT/ASYNC
## ***POST*** 

**Summary:** Create a new count async operation.

**Description:** Create a new count async operation.

### HTTP Request 
`***POST*** /targets/{TargetID}/count/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Count async operation created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/UNSUBSCRIBE/ASYNC
## ***POST*** 

**Summary:** Create a new unsubscribe async operation.

**Description:** Create a new unsubscribe async operation.

### HTTP Request 
`***POST*** /targets/{TargetID}/unsubscribe/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Unsubscribe async operation created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/CONTACTSDELETE/ASYNC
## ***POST*** 

**Summary:** Create a new contact deletion async operation.

**Description:** Create a new contact deletion async operation.

### HTTP Request 
`***POST*** /targets/{TargetID}/contactsdelete/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Contact deletion async operation created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/FIELDS/{FIELDID}
## ***PUT*** 

**Summary:** Update specified target field.

**Description:** Update specified target field.

### HTTP Request 
`***PUT*** /targets/{TargetID}/fields/{FieldID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target field updated. |
| 400 | The specified data is invalid. [405] |
| 404 | The specified field has not been found. [415] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/FIELDS/OCCUPANCY
## ***GET*** 

**Summary:** Return field occupancy list.

**Description:** Return field occupancy list.

### HTTP Request 
`***GET*** /targets/{TargetID}/fields/occupancy` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| FieldIDList | query |  Field idenifier list | No | array |
| SaleManagementID | query | Sale management identifier | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Field occupency list retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/INTERESTS/{INTERESTID}
## ***PUT*** 

**Summary:** Update specified target interest.

**Description:** Update specified target interest.

### HTTP Request 
`***PUT*** /targets/{TargetID}/interests/{InterestID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| InterestID | path | Interest identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target interest updated. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/CONTACTS/STATUS
## ***PUT*** 

**Summary:** Update specified target contacts status.

**Description:** Update specified target contacts status.

### HTTP Request 
`***PUT*** /targets/{TargetID}/contacts/status` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| SaleManagementID | query | Sale management identifier | No | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target contacts status updated. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/CONTACTS/ASYNC
## ***POST*** 

**Summary:** Create a new contact list async operation.

**Description:** Create a new contact list async operation.

### HTTP Request 
`***POST*** /targets/{TargetID}/contacts/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Contact list async operation created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/CONTACTS/PREVIEW
## ***POST*** 

**Summary:** Create a new target.

**Description:** Create a new target.

### HTTP Request 
`***POST*** /targets/{TargetID}/contacts/preview` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Target view created. |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/LAWS/{LAWID}/CRITERIAS/{CRITERIAID}
## ***GET*** 

**Summary:** Return specified criteria.

**Description:** Return specified criteria.

### HTTP Request 
`***GET*** /targets/{TargetID}/laws/{LawID}/criterias/{CriteriaID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |
| CriteriaID | path | Criteria identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Criteria retrieved. |
| 404 | The specified criteria has not been found. [508]  The specified criteria reference has not been found. [507] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified criteria.

**Description:** Update specified criteria.

### HTTP Request 
`***PUT*** /targets/{TargetID}/laws/{LawID}/criterias/{CriteriaID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |
| CriteriaID | path | Criteria identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Search control name is empty.  Search control name is empty. [514] |
| 400 | Bad number of criteria parameters. [520]  Operator not allowed. [509]  Invalid value for criteria type. [506] |
| 404 | The specified law has not been found. [511]  The specified criteria reference has not been found. [507]  The specified criteria has not been found. [508]  The specified search control has not been found. [513] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified criteria.

**Description:** Delete specified criteria.

### HTTP Request 
`***DELETE*** /targets/{TargetID}/laws/{LawID}/criterias/{CriteriaID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |
| CriteriaID | path | Criteria identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Criteria deleted. |
| 404 | The specified criteria has not been found. [508] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/LAWS/{LAWID}/CRITERIAS
## ***GET*** 

**Summary:** Return all criterias.

**Description:** Return all criterias.

### HTTP Request 
`***GET*** /targets/{TargetID}/laws/{LawID}/criterias` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Criterias retrieved. |
| 404 | The specified criteria has not been found. [508]  The specified law has not been found. [511] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new criteria.

**Description:** Create a new criteria.

### HTTP Request 
`***POST*** /targets/{TargetID}/laws/{LawID}/criterias` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| LawID | path | Law identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Criteria created. |
| 400 | Criteria not allowed. [504]  Invalid value for criteria type. [506]  Operator not allowed. [509]  Bad number of criteria parameters. [520] |
| 404 | The specified criteria reference has not been found. [507] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TARGETS/{TARGETID}/FIELDS/{FIELDID}/COUNT
## ***GET*** 

**Summary:** Return field count export.

**Description:** Return field count export.

### HTTP Request 
`***GET*** /targets/{TargetID}/fields/{FieldID}/count` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| TargetID | path | Target identifier | Yes | integer |
| FieldID | path | Field identifier | Yes | integer |
| MinCount | query | Min count | No | integer |
| SaleManagementID | query | Sale management identifier | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | field count export retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS
## ***GET*** 

**Summary:** Return all exports.

**Description:** Return all exports.

### HTTP Request 
`***GET*** /exports` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Exports retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new export.

**Description:** Créer un export de données, la création de l’export nécessite les informations suivantes :
- L’identifiant de mapping associé, route pour créer un mapping : *POST /exports/mappings*

- L’identifiant du planning 

- Le paramètre **IsIncremental** est utilisable uniquement dans le cas d’un export récurrent, il permet d’exporter les données depuis l’exécution de la dernière occurrence.

- Les séparateurs de ligne (Lf/Crlf) et de colonnes. - Les paramètres généraux de l’exports tels que le nom du fichier d’export, l’horodatage des fichiers (IncludeTimeStamp), l’encodage (UTF8, UTF16 …) 

Notez qu’il est possible d’ajouter des filtres à votre export après sa création via la route *POST /exports/{ExportID}/filters*. Si vous souhaitez être notifié de la fin d’un export, il est possible d’ajouter des notifications via la route : *POST /export/{ExportID}/recipients*

### HTTP Request 
`***POST*** /exports` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Export created. |
| 400 | The export cannot be set as incremental since its planning isn't recurrent. [1340] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping has not been found. [1302]  Le planning spécifié n'existe pas. [735] |
| 409 | The export file name already exist. [1309]  The export name already exist. [1310]  An export mapping without column. [1335] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0]  The export cannot be created. [1308] |

# /EXPORTS/{EXPORTID}
## ***GET*** 

**Summary:** Return specified export.

**Description:** Return specified export.

### HTTP Request 
`***GET*** /exports/{ExportID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Export retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping has not been found. [1302]  The specified export has not been found. [1301] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified export.

**Description:** Met à jour un export à partir de son identifiant, le nom de l'export (qui n'existe pas déjà) mais également le nom du fichier et les paramètres de l'export (compression, timestamp du nom de fichier, encodage, incrémentation...).

Attention :
- Un export ne peut pas être mis à jour s’il est achevé.

- On ne peut pas changer le mapping d'un export.

- On ne peut pas changer le planning d'un export en cours.

### HTTP Request 
`***PUT*** /exports/{ExportID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Export updated. |
| 400 | The specified export is read only, it cannot be updated. [1313]  The export planning cannot be updated when the export is active, you have to pause the export. [1339] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping has not been found. [1302]  Le planning spécifié n'existe pas. [735] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0]  The export cannot be updated. [1311] |

## ***DELETE*** 

**Summary:** Delete specified export.

**Description:** Delete specified export.

### HTTP Request 
`***DELETE*** /exports/{ExportID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Export deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0]  The export cannot be deleted. [1312] |

# /EXPORTS/SEARCH
## ***POST*** 

**Summary:** Return exports found.

**Description:** Retourne la liste des exports filtrés en fonction des paramètres facultatifs suivants : 

- SearchValue :  Valeur de recherche d'un export

- PlanningType : Le type du planning, OneTime (export ponctuel) ou Recurrent

- LastStatus :  Le statut de la dernière occurrence de l'export = success, error ou pending

- TypeID : L'identifiant du type d'export, pour la liste des types d’exports, se référer à la route *GET /exports/types*

- MappingID : L'identifiant d'un mapping

### HTTP Request 
`***POST*** /exports/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Exports retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/TYPES
## ***GET*** 

**Summary:** Return export type dependency tree.

**Description:** Return export type dependency tree.

### HTTP Request 
`***GET*** /exports/types` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Export type dependency tree retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/MAPPINGS
## ***GET*** 

**Summary:** Return all mappings.

**Description:** Return all mappings.

### HTTP Request 
`***GET*** /exports/mappings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mappings retrieved. |
| 400 | The given export type in invalid. [1305] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new mapping.

**Description:** Un mapping est nécessaire à la création d’un export, il permet d’associer des données dans la base de données de Dolist à des colonnes dans le fichier de destination.

La création d’un mapping d’export nécessite les informations suivantes :

- L'identifiant du type du mapping, les différents types sont disponibles via la route suivante :
*GET /exports/types*

- Le nom du mapping

Après avoir créé un mapping d’export vous pouvez évidemment lui ajouter des colonnes via la route :
*POST /exports/mappings/{MappingID}/columns*

### HTTP Request 
`***POST*** /exports/mappings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Mapping created. |
| 400 | The given export type in invalid. [1305] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | An export mapping with the same name already exists. [1304] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/{EXPORTID}/FILTERS
## ***GET*** 

**Summary:** Return specified export filters.

**Description:** Return specified export filters.

### HTTP Request 
`***GET*** /exports/{ExportID}/filters` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Export filters retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export has not been found. [1301] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create export filters.

**Description:** Les filtres s'appliquent sur les exports, ils servent par exemple à exporter les ouvreurs d'une campagne, un filtre sur l'identifiant de la campagne aura alors été ajouté.
Vous pouvez choisir parmi les types de filtres suivant

- **Segment** : un identifiant de segment

- **EmailSendings**: un ou plusieurs identifiants de campagne e-mail

- **SmsSendings**: un ou plusieurs identifiants de campagne SMS

- **Interests** : un ou plusieurs identifiants d’intérêts de contacts

- **InterestsGroup**: un ou plusieurs identifiants de groupe d'intérêts de contacts

- **LastDays**: un entier définissant un nombre de jour avant la date courante

- **StartDate**: une date de début

- **EndDate**: une date de fin

- **Forms**: un ou plusieurs identifiants de formulaires

### HTTP Request 
`***POST*** /exports/{ExportID}/filters` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Export filters retrieved. |
| 204 | No Content |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export has not been found. [1301] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/TYPES/FILTERS
## ***GET*** 

**Summary:** Return all export filters for specified type.

**Description:** Return all export filters for specified type.

### HTTP Request 
`***GET*** /exports/types/filters` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TypeID | query | Type identifier. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Export type filters retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/{EXPORTID}/RECIPIENTS
## ***GET*** 

**Summary:** Get recipient list for the specified export.

**Description:** Get recipient list for the specified export.

### HTTP Request 
`***GET*** /exports/{ExportID}/recipients` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Export recipient retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export has not been found. [1301] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new export recipient.

**Description:** Create a new export recipient.

### HTTP Request 
`***POST*** /exports/{ExportID}/recipients` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Export recipient created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified user has not been found. [901]  The specified export has not been found. [1301] |
| 409 | A recipient with the same value and type already exists. [1324] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/MAPPINGS/{MAPPINGID}
## ***GET*** 

**Summary:** Retrieve specified mapping.

**Description:** Retrieve specified mapping.

### HTTP Request 
`***GET*** /exports/mappings/{MappingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mapping retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping has not been found. [1302] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified mapping.

**Description:** Update specified mapping.

### HTTP Request 
`***PUT*** /exports/mappings/{MappingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping udpated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | The specified export mapping is read only. [1306]  An export mapping with the same name already exists. [1304] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified mapping.

**Description:** Delete specified mapping.

### HTTP Request 
`***DELETE*** /exports/mappings/{MappingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | The specified export mapping is read only. [1306] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/MAPPINGS/SEARCH
## ***POST*** 

**Summary:** Return all mappings found.

**Description:** Retourne la liste des mappings filtrés en fonction des paramètres facultatifs suivants : - SearchValue : Valeur de recherche du nom d'un mapping - TypeID : Le type recherché, les types d’exports sont disponibles via la route 
*GET /exports/types*

### HTTP Request 
`***POST*** /exports/mappings/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mappings retrieved. |
| 400 | The given export type in invalid. [1305] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/MAPPINGS/COLUMNREFERENCES
## ***GET*** 

**Summary:** Retrieve all column references.

**Description:** Retourne la liste des références de colonnes possibles pour les mappings.
Il est possible de filtrer la liste pour voir remonter seulement les références des colonnes possibles pour un type donné.

### HTTP Request 
`***GET*** /exports/mappings/columnreferences` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TypeID | query | Type identifier to filter on. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Column references retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/{EXPORTID}/FILTERS/{FILTERID}
## ***DELETE*** 

**Summary:** Delete specified export filter.

**Description:** Delete specified export filter.

### HTTP Request 
`***DELETE*** /exports/{ExportID}/filters/{FilterID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |
| FilterID | path | Filter identifier. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Export filter deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export has not been found. [1301] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/{EXPORTID}/RECIPIENTS/{RECIPIENTID}
## ***DELETE*** 

**Summary:** Delete the specified export recipient.

**Description:** Delete the specified export recipient.

### HTTP Request 
`***DELETE*** /exports/{ExportID}/recipients/{RecipientID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |
| RecipientID | path | Recipient identifier to delete. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Export recipient deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export has not been found. [1301] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/MAPPINGS/{MAPPINGID}/DUPLICATE
## ***POST*** 

**Summary:** Duplicate the specified export mapping.

**Description:** Duplicate the specified export mapping.

### HTTP Request 
`***POST*** /exports/mappings/{MappingID}/duplicate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Mapping duplicated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping has not been found. [1302] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/MAPPINGS/{MAPPINGID}/COLUMNS
## ***GET*** 

**Summary:** Retrieve all mapping columns.

**Description:** Retrieve all mapping columns.

### HTTP Request 
`***GET*** /exports/mappings/{MappingID}/columns` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mapping columns retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new mapping column.

**Description:** Créer une colonne pour un mapping spécifié. Il est possible d’appliquer un format à une colonne. Voici une liste non exhaustive des formats applicables :
-   Des formats applicables aux champs dates, utilisables avec format type *dd/MM/yyyy*

-   Des formats applicables aux champs numériques tels que 
	-  ```C``` ou ```c```, devises retourne une valeur monétaire pour la culture en cours
	- ```E``` ou ```e```, notation exponentielle
	-  ```Dx```, nombre de digit, ex : D8 appliqué sur 1234 donnera 00001234

En renseignant la propriété *Name* vous pourrez donner un alias à la colonne dans votre fichier d’export, si *Name* n’est pas renseignée la colonne prendra le nom par défaut.
Notez qu’une seule colonne n’est autorisée par référence de colonne et par mapping et qu’un nom de colonne doit être unique dans un mapping d’export.

### HTTP Request 
`***POST*** /exports/mappings/{MappingID}/columns` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping column created. |
| 403 | The export mapping column is unauthorized in this export mapping. [1316]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | The required column reference is not found. [1318]  The specified export mapping column has not been found. [1303] |
| 409 | The specified column is not properly formatted. [1329]  The specified export mapping is read only. [1306]  An export mapping column already exists with the same name. [1315]  An export mapping column already exists or missing. [1336] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/MAPPINGS/{MAPPINGID}/COLUMNS/{COLUMNID}
## ***GET*** 

**Summary:** Retrieve specified mapping column.

**Description:** Retrieve specified mapping column.

### HTTP Request 
`***GET*** /exports/mappings/{MappingID}/columns/{ColumnID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| ColumnID | path | Mapping column identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mapping column retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping column has not been found. [1303] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified mapping column.

**Description:** Modifie la colonne spécifiée dans le mapping en fonction des paramètres saisies.

Un mapping est un ensemble de colonnes, chaque colonne à une position qui correspondra à l’ordre que l’on retrouvera dans le fichier d’export de destination, il est possible de changer la position d’une colonne en renseignant la propriété **Position**.

Vous pouvez mettre à jour l’alias de la colonne, ainsi que le format de la même façon que dans la route */exports/mappings/{MappingID}/columns*

### HTTP Request 
`***PUT*** /exports/mappings/{MappingID}/columns/{ColumnID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| ColumnID | path | Column identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping column updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping column has not been found. [1303]  The export mapping column is missing from this export mapping. [1317] |
| 409 | The specified export mapping is read only. [1306]  An export mapping column already exists with the same name. [1315] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified mapping column.

**Description:** Delete specified mapping column.

### HTTP Request 
`***DELETE*** /exports/mappings/{MappingID}/columns/{ColumnID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| ColumnID | path | Column identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping column deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export mapping column has not been found. [1303] |
| 409 | The specified export mapping is read only. [1306] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EXPORTS/{EXPORTID}/JOBS/{JOBID}/FILE
## ***GET*** 

**Summary:** Return specified export file.

**Description:** Retourne le fichier d'export correspondant à l'identifiant de l'export et l'identifiant de l'exécution de l'export (jobID).

### HTTP Request 
`***GET*** /exports/{ExportID}/jobs/{JobID}/file` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ExportID | path | Export identifier. | Yes | integer |
| JobID | path | Export job identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Export file retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified export job has not been found. [1307] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FILES/ACCOUNTS/{PATH*}
## ***GET*** 

**Summary:** Return account files and directories.

**Description:** Return account files and directories.

### HTTP Request 
`***GET*** /files/accounts/{Path*}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| Path | path | Path to directory | Yes | string |
| SearchValue | query | Search value | No | string |
| SortField | query | Sort field | No | string |
| SortOrder | query | Sort order (require sort field) | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit (maximum elements, require offset) | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Files and directories retrieved. |
| 400 | The specified path contains invalid characters. [33] |
| 403 | Le répertoire spécifié ne peut pas être lu. [22]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le répertoire spécifié est introuvable. [18] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update and/or rename existing file/directory.

**Description:** Update and/or rename existing file/directory.

### HTTP Request 
`***PUT*** /files/accounts/{Path*}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| Path | path | Path to file or directory | Yes | string |
| RenameTo | query | Rename file or directory | No | string |
| File | formData | File (send empty content to do a basic renaming) | No | file |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 204 | File or directory updated. |
| 400 | The specified path contains invalid characters. [33]  The specified file format is not supported or is not valid. [32]  Supplied file is empty. [27]  No file were provided. [25] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le fichier spécifié introuvable. [17] |
| 409 | Le fichier spécifié existe déjà. [19]  The specified file cannot be renamed. [34]  The specified directory cannot be renamed. [35] |
| 500 | Could not download file, maybe a file with same name already exists. [29]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Upload file to specified path or create directory.

**Description:** Upload file to specified path or create directory.

### HTTP Request 
`***POST*** /files/accounts/{Path*}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| Path | path | Path to directory | Yes | string |
| Overwrite | query | Overwrite existing files? | No | boolean |
| File | formData | File (send empty content for directory creation) | No | file |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | File or directory created. |
| 400 | The specified path contains invalid characters. [33]  The specified file format is not supported or is not valid. [32]  Supplied file is empty. [27] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | Le fichier spécifié existe déjà. [19] |
| 500 | Could not download file, maybe a file with same name already exists. [29]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified file or directory.

**Description:** Delete specified file or directory.

### HTTP Request 
`***DELETE*** /files/accounts/{Path*}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| Path | path | Path to directory | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | File or directory deleted. |
| 400 | The specified path contains invalid characters. [33] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le fichier spécifié introuvable. [17]  Le répertoire spécifié est introuvable. [18] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FILES/CREATIVE-COMMONS/{PATH*}
## ***GET*** 

**Summary:** Return creative commons files and directories.

**Description:** Return creative commons files and directories.

### HTTP Request 
`***GET*** /files/creative-commons/{Path*}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| Path | path | Path to directory | Yes | string |
| SearchValue | query | Search value | No | string |
| SortField | query | Sort field | No | string |
| SortOrder | query | Sort order (require sort field) | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit (maximum elements, require offset) | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Files and directories retrieved. |
| 400 | The specified path contains invalid characters. [33] |
| 403 | Le répertoire spécifié ne peut pas être lu. [22]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le répertoire spécifié est introuvable. [18] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FILES/REMOTES/TYPES
## ***GET*** 

**Summary:** Return all available protocols.

**Description:** Return all available protocols.

### HTTP Request 
`***GET*** /files/remotes/types` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Protocols retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FILES/REMOTES
## ***GET*** 

**Summary:** Return all remotes.

**Description:** Return all remotes.

### HTTP Request 
`***GET*** /files/remotes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Remotes retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | Could not create remote directory. [72] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new remote.

**Description:** Create a new remote.

### HTTP Request 
`***POST*** /files/remotes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier. | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Remote created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | Remote name already exists. [1802]  Remote cannot be created. [1803] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /FORMS/{FORMID}/TAGS
## ***GET*** 

**Summary:** Return tags of specified form.

**Description:** Return tags of specified form.

### HTTP Request 
`***GET*** /forms/{FormID}/tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| FormID | path | Form identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Form tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/FILE
## ***GET*** 

**Summary:** Return auto-generated import sample file.

**Description:** Return auto-generated import sample file.

### HTTP Request 
`***GET*** /imports/mappings/file` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Import sample file retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/{MAPPINGID}
## ***GET*** 

**Summary:** Return specified mapping.

**Description:** Return specified mapping.

### HTTP Request 
`***GET*** /imports/mappings/{MappingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mapping retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified mapping.

**Description:** Update specified mapping.

### HTTP Request 
`***PUT*** /imports/mappings/{MappingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 409 | A mapping with the same name already exists. [305] |
| 500 | The mapping cannot be modified. [307]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified mapping.

**Description:** Delete specified mapping.

### HTTP Request 
`***DELETE*** /imports/mappings/{MappingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 500 | The mapping cannot be deleted. [308]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/ACTIONS
## ***GET*** 

**Summary:** Return all mapping actions.

**Description:** Return all mapping actions.

### HTTP Request 
`***GET*** /imports/mappings/actions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mapping actions retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/FIELDS
## ***GET*** 

**Summary:** Return all field actions.

**Description:** Return all field actions.

### HTTP Request 
`***GET*** /imports/mappings/fields` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Field actions retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/{IMPORTID}/GROUPINTERESTS
## ***GET*** 

**Summary:** Return all groups with interests of specified import.

**Description:** Return all groups with interests of specified import.

### HTTP Request 
`***GET*** /imports/{ImportID}/groupinterests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Groups with interests of specified import retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import has not been found. [318] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/JOBS/{JOBID}
## ***GET*** 

**Summary:** Return specified import job.

**Description:** Return specified import job.

### HTTP Request 
`***GET*** /imports/jobs/{JobID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| JobID | path | Import job identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Import job retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import job has not been found. [324] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/{IMPORTID}/INTERESTS
## ***PUT*** 

**Summary:** Update import interests.

**Description:** Update import interests.

### HTTP Request 
`***PUT*** /imports/{ImportID}/interests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |
| OperationMode | query | Operation mode. | Yes | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Import interests updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified contact has not been found. [401]  The specified interest has not been found. [432] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/{IMPORTID}/RECIPIENTS
## ***GET*** 

**Summary:** Return all recipients.

**Description:** Return all recipients.

### HTTP Request 
`***GET*** /imports/{ImportID}/recipients` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Recipients retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import has not been found. [318] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new recipient.

**Description:** Create a new recipient.

### HTTP Request 
`***POST*** /imports/{ImportID}/recipients` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Recipient created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import has not been found. [318]  The specified user has not been found. [901] |
| 409 | A recipient with the same value and type already exists. [327] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS
## ***GET*** 

**Summary:** Return all mappings.

**Description:** Return all mappings.

### HTTP Request 
`***GET*** /imports/mappings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SearchValue | query | Search value. | No | string |
| Separator | query | Mapping separator. | No | string |
| ContainsColumns | query | Filter on mappings containing columns or not? | No | boolean |
| Filter | query | Mapping type filter. | No | string |
| SortField | query | Sort field. | No | string |
| SortOrder | query | Sort order. | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Max records | No | integer |
| UpdatedAfter | query | Mapping must have been updated after this date | No | dateTime |
| UpdatedBefore | query | Mapping must have been updated before this date | No | dateTime |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mappings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new mapping.

**Description:** 

        You must send a multipart/form-data.

        Mapping properties must be serialized as JSV



        Example:



        -----------------------------161471567112257

        Content-Disposition: form-data; name="file"; filename="contacts.txt"

        Content - Type: text/plain



        Email   LastName    Mobile

        Stephanie.Harris_1530451234@dolist.net  Harris  0600150157

        Sara.Gordon_1841132064@dolist.net   Gordon  0600003895

        Angelina.Butler_788977617@dolist.net    Butler  0600000497

        Rodolfo.Perez_108029555@dolist.net  Perez   0600230285

        Carl.Williamson_519714874@dolist.net    Williamson  0600027312

        Perry.Floyd_234167979@dolist.net    Floyd   0600149991

        ---------------------------- - 161471567112257

        Content - Disposition: form-data; name = "Mapping"



        {Name:new mapping,Separator:;,ContainsColumns:false,ContainsQuotes:false}

        -----------------------------161471567112257--

    

### HTTP Request 
`***POST*** /imports/mappings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| File | formData | File. | Yes | file |
| Mapping | formData | Mapping. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Mapping created. |
| 400 | The Supplied archive file is empty. [31]  Supplied File is too big. [28]  Supplied file is empty. [27]  No file were provided. [25] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | A mapping file with the same name already exists. [315]  A mapping with the same name already exists. [305] |
| 500 | Could not extract archive file. [30]  Could not download file, maybe a file with same name already exists. [29]  The mapping cannot be created. [306]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/{IMPORTID}
## ***GET*** 

**Summary:** Return specified import.

**Description:** Return specified import.

### HTTP Request 
`***GET*** /imports/{ImportID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Import retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import has not been found. [318] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified import.

**Description:** Update specified import.

### HTTP Request 
`***PUT*** /imports/{ImportID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Import updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import has not been found. [318] |
| 409 | An import with the same name already exists. [326]  An import with the same pattern already exists. [330] |
| 500 | The import cannot be updated. [320]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified import.

**Description:** Delete specified import.

### HTTP Request 
`***DELETE*** /imports/{ImportID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Import deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import has not been found. [318] |
| 500 | The import cannot be deleted. [321]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/JOBS
## ***GET*** 

**Summary:** Return all import jobs.

**Description:** Return all import jobs.

### HTTP Request 
`***GET*** /imports/jobs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | query | Import identifier. | No | integer |
| SearchValue | query | Search value. | No | string |
| Filter | query | Import type filter. | No | string |
| SortField | query | Sort field. | No | string |
| SortOrder | query | Sort order. | No | string |
| Status | query | Status. | No | string |
| Executed | query | Filter on executed jobs or not? | No | boolean |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Import jobs retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new import job.

**Description:** 

        You must send a multipart/form-data.

        Mapping properties must be serialized as JSV



        Example:



        -----------------------------161471567112257

        Content-Disposition: form-data; name="file"; filename="contacts.txt"

        Content - Type: text/plain



        Email   LastName    Mobile

        Stephanie.Harris_1530451234@dolist.net  Harris  0600150157

        Sara.Gordon_1841132064@dolist.net   Gordon  0600003895

        Angelina.Butler_788977617@dolist.net    Butler  0600000497

        Rodolfo.Perez_108029555@dolist.net  Perez   0600230285

        Carl.Williamson_519714874@dolist.net    Williamson  0600027312

        Perry.Floyd_234167979@dolist.net    Floyd   0600149991

        ---------------------------- - 161471567112257

        Content - Disposition: form-data; name = "Job"



        {ImportID:10104}

        -----------------------------161471567112257--

    

### HTTP Request 
`***POST*** /imports/jobs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| File | formData | File. | Yes | file |
| Job | formData | Import job. | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Import job created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/IMPORTJOBS
## ***GET*** 

**Summary:** Return all imports with jobs.

**Description:** Return all imports with jobs.

### HTTP Request 
`***GET*** /imports/importjobs` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| JobPerImport | query | Required job number. | Yes | integer |
| MappingID | query | Mapping identifier. | No | integer |
| SearchValue | query | Search value. | No | string |
| Filter | query | Import type filter. | No | string |
| SortField | query | Sort field. | No | string |
| SortOrder | query | Sort order. | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Imports with jobs retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/{MAPPINGID}/COLUMNS/{COLUMNID}
## ***GET*** 

**Summary:** Return specified mapping column.

**Description:** Return specified mapping column.

### HTTP Request 
`***GET*** /imports/mappings/{MappingID}/columns/{ColumnID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| ColumnID | path | Column identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304]  The specified mapping column has not been found. [310] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified mapping column.

**Description:** Update specified mapping column.

### HTTP Request 
`***PUT*** /imports/mappings/{MappingID}/columns/{ColumnID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| ColumnID | path | Column identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Mapping column updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304]  The specified mapping column has not been found. [310] |
| 500 | The mapping column cannot be modified. [313]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified mapping column.

**Description:** Delete specified mapping column.

### HTTP Request 
`***DELETE*** /imports/mappings/{MappingID}/columns/{ColumnID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| ColumnID | path | Column identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Column deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304]  The specified mapping column has not been found. [310] |
| 500 | The mapping column cannot be deleted. [314]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/JOBS/{JOBID}/STATS/EXCLUSION
## ***GET*** 

**Summary:** Return specified import job statistics exclusion.

**Description:** Return specified import job statistics exclusion.

### HTTP Request 
`***GET*** /imports/jobs/{JobID}/stats/exclusion` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| JobID | path | Import job identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Import job statistics exclusion retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import job has not been found. [324] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/{MAPPINGID}/COLUMNS
## ***GET*** 

**Summary:** Return all mapping columns.

**Description:** Return all mapping columns.

### HTTP Request 
`***GET*** /imports/mappings/{MappingID}/columns` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mapping columns retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new mapping column.

**Description:** Create a new mapping column.

### HTTP Request 
`***POST*** /imports/mappings/{MappingID}/columns` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Mapping column created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304]  The specified field has not been found. [415]  The specified action has not been found. [316] |
| 409 | A mapping column with the same name or field already exists. [311] |
| 500 | The mapping column cannot be created. [312]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/{MAPPINGID}/SNAPSHOT
## ***GET*** 

**Summary:** Return specified mapping snapshot.

**Description:** Return specified mapping snapshot.

### HTTP Request 
`***GET*** /imports/mappings/{MappingID}/snapshot` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Mapping snapshot retrieved. |
| 400 | The specified file format is not supported or is not valid. [32]  No file were provided. [25] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 409 | The specified mapping file is not properly formatted. [333] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/MAPPINGS/{MAPPINGID}/DUPLICATE
## ***POST*** 

**Summary:** Duplicate the specified import mapping.

**Description:** Duplicate the specified import mapping.

### HTTP Request 
`***POST*** /imports/mappings/{MappingID}/duplicate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | path | Mapping identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Mapping duplicated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/JOBS/{JOBID}/REPORT
## ***GET*** 

**Summary:** Return specfied import job report file.

**Description:** Return specfied import job report file.

### HTTP Request 
`***GET*** /imports/jobs/{JobID}/report` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| JobID | path | Import job identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Import job report file retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import job has not been found. [324] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/JOBS/{JOBID}/STATS
## ***GET*** 

**Summary:** Return specified import job statistics.

**Description:** Return specified import job statistics.

### HTTP Request 
`***GET*** /imports/jobs/{JobID}/stats` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| JobID | path | Import job identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Import job statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified import job has not been found. [324] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS/{IMPORTID}/RECIPIENTS/{RECIPIENTID}
## ***DELETE*** 

**Summary:** Delete specified recipient.

**Description:** Delete specified recipient.

### HTTP Request 
`***DELETE*** /imports/{ImportID}/recipients/{RecipientID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ImportID | path | Import identifier. | Yes | integer |
| RecipientID | path | Recipient identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Recipient deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified recipient has not been found. [328]  The specified import has not been found. [318] |
| 500 | The recipient cannot be deleted. [329]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /IMPORTS
## ***GET*** 

**Summary:** Return all imports.

**Description:** Return all imports.

### HTTP Request 
`***GET*** /imports` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MappingID | query | Mapping identifier. | No | integer |
| SearchValue | query | Search value. | No | string |
| Filter | query | Import type filter. | No | string |
| SortField | query | Sort field. | No | string |
| SortOrder | query | Sort order. | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Imports retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified mapping has not been found. [304] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new import.

**Description:** Create a new import.

### HTTP Request 
`***POST*** /imports` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Import created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | An import with the same name already exists. [326] |
| 500 | The import cannot be created. [319]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/ADDRESSES/REPLIES/{REPLYID}
## ***GET*** 

**Summary:** Return specified reply address.

**Description:** Return specified reply address.

### HTTP Request 
`***GET*** /email/messages/addresses/replies/{ReplyID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ReplyID | path | Reply address identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Reply address retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The reply address has not been found. [705] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete sppecified reply address.

**Description:** Delete sppecified reply address.

### HTTP Request 
`***DELETE*** /email/messages/addresses/replies/{ReplyID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ReplyID | path | Reply address identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Reply address deleted. |
| 400 | Reply address cannot be deleted. [706] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The reply address has not been found. [705] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/ADDRESSES/PACKSENDERS/{SENDERID}
## ***GET*** 

**Summary:** Return specified sender.

**Description:** Return specified sender.

### HTTP Request 
`***GET*** /email/messages/addresses/packsenders/{SenderID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SenderID | path | Sender identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sender retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | L'expéditeur spécifié n'existe pas. [702] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified sender.

**Description:** Delete specified sender.

### HTTP Request 
`***DELETE*** /email/messages/addresses/packsenders/{SenderID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SenderID | path | Sender identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Sender deleted. |
| 400 | Sender cannot be deleted. [704] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | L'expéditeur spécifié n'existe pas. [702] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/ANALYZER/ASYNC
## ***POST*** 

**Summary:** Create a new analyzer async operation.

**Description:** Create a new analyzer async operation.

### HTTP Request 
`***POST*** /email/messages/{MessageID}/analyzer/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Analyzer async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/DRAFT/ANALYZER/ASYNC
## ***POST*** 

**Summary:** Create a new analyzer async operation.

**Description:** Create a new analyzer async operation.

### HTTP Request 
`***POST*** /email/messages/draft/analyzer/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Analyzer async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/LINKS/{LINKID}
## ***GET*** 

**Summary:** Return specified message link.

**Description:** Return specified message link.

### HTTP Request 
`***GET*** /email/messages/{MessageID}/links/{LinkID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| LinkID | path | Message link identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message link retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708]  The specified message link has not been found. [719] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified message link.

**Description:** Update specified message link.

### HTTP Request 
`***PUT*** /email/messages/{MessageID}/links/{LinkID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| LinkID | path | Message link identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message link updated. |
| 400 | Message link cannot be modified. [718] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708]  The specified message link has not been found. [719] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/ADDRESSES/REPLIES
## ***GET*** 

**Summary:** Return all reply addresses.

**Description:** Return all reply addresses.

### HTTP Request 
`***GET*** /email/messages/addresses/replies` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SortField | query | Sort field. | No | string |
| SortOrder | query | Sort order. | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Reply addresses retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new reply address.

**Description:** Create a new reply address.

### HTTP Request 
`***POST*** /email/messages/addresses/replies` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Reply address created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | The specified reply address already exists. [707] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/ADDRESSES/PACKSENDERS
## ***GET*** 

**Summary:** Return all senders.

**Description:** Return all senders.

### HTTP Request 
`***GET*** /email/messages/addresses/packsenders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SortField | query | Sort field. | No | string |
| SortOrder | query | Sort order. | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Senders retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/LINKS
## ***GET*** 

**Summary:** Return all message links.

**Description:** Return all message links.

### HTTP Request 
`***GET*** /email/messages/{MessageID}/links` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| LinkTypeList | query | Link type list. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message links retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/DUPLICATE
## ***POST*** 

**Summary:** Duplicate specified message.

**Description:** Duplicate specified message.

### HTTP Request 
`***POST*** /email/messages/{MessageID}/duplicate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message duplicated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 409 | Message cannot be duplicated. [715] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/CONTENT
## ***GET*** 

**Summary:** Return specified message content.

**Description:** Return specified message content.

### HTTP Request 
`***GET*** /email/messages/{MessageID}/content` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message content retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified message content.

**Description:** Update specified message content.

### HTTP Request 
`***PUT*** /email/messages/{MessageID}/content` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message content updated. |
| 400 | Message content cannot be modified. [716] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/CHECK
## ***GET*** 

**Summary:** Check if message is ready for sending.

**Description:** Check if message is ready for sending.

### HTTP Request 
`***GET*** /email/messages/{MessageID}/check` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| SendType | query | Sending type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Check email message done. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | L'expéditeur spécifié n'existe pas. [702]  The specified message unsubscribe link has not been found. [720]  The specified message has not been found. [708] |
| 409 | Le pack de délivrabilité du message n'est pas autorisé. [723]  Le sujet du message n'est pas valide. [722]  Tracking must be validated. [721] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/RENDER
## ***POST*** 

**Summary:** Return rendered messages sending

**Description:** Return rendered messages sending

### HTTP Request 
`***POST*** /email/sendings/{SendingID}/render` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| ContactID | query | Contact identifier | Yes | integer |
| KeyCode | query | KeyCode | Yes | string |
| OccurrenceID | query | Occurrence identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | The specified KeyCode is not valid. [45] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/CONTENT
## ***GET*** 

**Summary:** Return specified sending content.

**Description:** Return specified sending content.

### HTTP Request 
`***GET*** /email/sendings/{SendingID}/content` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending content retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/LOCKS
## ***GET*** 

**Summary:** Return specified message sending constraints.

**Description:** Return specified message sending constraints.

### HTTP Request 
`***GET*** /email/sendings/{SendingID}/locks` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sending constraints retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |

# /EMAIL/SENDINGS/{SENDINGID}/STANDBY
## ***POST*** 

**Summary:** Set specified message sending in standby mode.

**Description:** Set specified message sending in standby mode.

### HTTP Request 
`***POST*** /email/sendings/{SendingID}/standby` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending set in standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/RESUME
## ***POST*** 

**Summary:** Resume specified message sending from standby mode.

**Description:** Resume specified message sending from standby mode.

### HTTP Request 
`***POST*** /email/sendings/{SendingID}/resume` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending resumed from standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/STOP
## ***POST*** 

**Summary:** Stop specified message sending.

**Description:** Stop specified message sending.

### HTTP Request 
`***POST*** /email/sendings/{SendingID}/stop` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending stopped. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/REPORT
## ***GET*** 

**Summary:** Return specfied sending report file.

**Description:** Return specfied sending report file.

### HTTP Request 
`***GET*** /email/sendings/{SendingID}/report` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| TargetID | query | Target identifier. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending report file retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729]  The specified target has not been found. [502] |
| 409 | Could not generate sending report. [753] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/THUMBNAILS
## ***GET*** 

**Summary:** Return specified sending thumbnails.

**Description:** Return specified sending thumbnails.

### HTTP Request 
`***GET*** /email/sendings/{SendingID}/thumbnails` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending thumbnails retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/TRACKINGS/{LINKID}
## ***GET*** 

**Summary:** Return specified redirect link.

**Description:** Return specified redirect link.

### HTTP Request 
`***GET*** /email/messages/trackings/{LinkID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| LinkID | path | Link identifier. | Yes | integer |
| SendingID | query | Sending identifier. | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | Yes | integer |
| ContactID | query | Contact identifier. | Yes | integer |
| QueryString | query | Query String. | No | string |
| KeyCode | query | KeyCode. | Yes | string |
| IpAddress | query | Client Ip Address. | Yes | string |
| UserAgent | query | User Agent. | Yes | string |
| Referer | query | Referrer. | Yes | string |
| TrackingType | query | Tracking Type. | No | string |
| SaveEvent | query | Save event | Yes | boolean |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |

# /EMAIL/MESSAGES/{MESSAGEID}/TAGS
## ***GET*** 

**Summary:** Return tags of specified message.

**Description:** Return tags of specified message.

### HTTP Request 
`***GET*** /email/messages/{MessageID}/tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}/TAGS
## ***GET*** 

**Summary:** Return tags of specified sending.

**Description:** Return tags of specified sending.

### HTTP Request 
`***GET*** /email/sendings/{SendingID}/tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/ADDRESSES/PACKS/{PACKID}/SENDERS
## ***POST*** 

**Summary:** Create a new sender.

**Description:** Create a new sender.

### HTTP Request 
`***POST*** /email/messages/addresses/packs/{PackID}/senders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| PackID | path | Pack identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Sender created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified deliverability pack has not been found. [701] |
| 409 | The specified sender already exists. [703] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete all senders of specified pack.

**Description:** Delete all senders of specified pack.

### HTTP Request 
`***DELETE*** /email/messages/addresses/packs/{PackID}/senders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| PackID | path | Pack identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Pack senders deleted. |
| 400 | Sender cannot be deleted. [704] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/LINKS/{LINKID}/INTERESTS
## ***PUT*** 

**Summary:** Update message link interests.

**Description:** Update message link interests.

### HTTP Request 
`***PUT*** /email/messages/{MessageID}/links/{LinkID}/interests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| LinkID | path | Message link identifier. | Yes | integer |
| OperationMode | query | Operation mode. | Yes | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message link interests updated. |
| 400 | Message link cannot be modified. [718] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708]  The specified message link has not been found. [719]  The specified interest has not been found. [432] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}/LINKS/{LINKID}/GROUPINTERESTS
## ***GET*** 

**Summary:** Return all groups with group interests of specified message and link.

**Description:** Return all groups with group interests of specified message and link.

### HTTP Request 
`***GET*** /email/messages/{MessageID}/links/{LinkID}/groupinterests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| LinkID | path | Link identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Groups with interests of specified message retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708]  The specified message link has not been found. [719] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/LINKTYPES
## ***GET*** 

**Summary:** Return all message link types.

**Description:** Return all message link types.

### HTTP Request 
`***GET*** /email/messages/linktypes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message link types retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/{MESSAGEID}
## ***GET*** 

**Summary:** Return specified message.

**Description:** Return specified message.

### HTTP Request 
`***GET*** /email/messages/{MessageID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified message.

**Description:** Update specified message.

### HTTP Request 
`***PUT*** /email/messages/{MessageID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message updated. |
| 400 | Message cannot be modified. [711] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified culture has not been found. [41]  The reply address has not been found. [705]  L'expéditeur spécifié n'existe pas. [702] |
| 409 | Le message spécifié existe déjà. [709] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified message.

**Description:** Delete specified message.

### HTTP Request 
`***DELETE*** /email/messages/{MessageID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| MessageID | path | Message identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message deleted. |
| 400 | Message cannot be deleted. [712]  Le message est verrouillé. [728] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/SEARCH
## ***POST*** 

**Summary:** Return all messages find.

**Description:** Return all messages find.

### HTTP Request 
`***POST*** /email/messages/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Messages retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/ENCODINGS
## ***GET*** 

**Summary:** Return all message encodings.

**Description:** Return all message encodings.

### HTTP Request 
`***GET*** /email/messages/encodings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message encodings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/CULTURES
## ***GET*** 

**Summary:** Return all available message cultures.

**Description:** Return all available message cultures.

### HTTP Request 
`***GET*** /email/messages/cultures` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Available message cultures retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES/FORMATS
## ***GET*** 

**Summary:** Return all message formats.

**Description:** Return all message formats.

### HTTP Request 
`***GET*** /email/messages/formats` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message formats retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/{SENDINGID}
## ***GET*** 

**Summary:** Return specified message sending.

**Description:** Return specified message sending.

### HTTP Request 
`***GET*** /email/sendings/{SendingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sending retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified message sending.

**Description:** Update specified message sending.

### HTTP Request 
`***PUT*** /email/sendings/{SendingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending updated. |
| 400 | Planning Start date must be later than now. [736] |
| 403 | Le statut de l'envoi n'est pas valide pour cette action. [732]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729]  Le planning spécifié n'existe pas. [735]  The specified message has not been found. [708] |
| 409 | The specified message sending already exists. [731] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/SEARCH
## ***POST*** 

**Summary:** Return all message sendings found.

**Description:** Return all message sendings found.

### HTTP Request 
`***POST*** /email/sendings/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sendings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/STANDBY
## ***POST*** 

**Summary:** Set all message sendings in standby mode.

**Description:** Set all message sendings in standby mode.

### HTTP Request 
`***POST*** /email/sendings/standby` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sendings set in standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/RESUME
## ***POST*** 

**Summary:** Resume all message sendings from standby mode.

**Description:** Resume all message sendings from standby mode.

### HTTP Request 
`***POST*** /email/sendings/resume` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message sendings resumed from standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS/STOP
## ***POST*** 

**Summary:** Stop all message sendings.

**Description:** Stop all message sendings.

### HTTP Request 
`***POST*** /email/sendings/stop` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sendings stopped. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/MESSAGES
## ***GET*** 

**Summary:** Return all messages.

**Description:** Return all messages.

### HTTP Request 
`***GET*** /email/messages` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| Channel | query | Message channel. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Messages retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new message.

**Description:** Create a new message.

### HTTP Request 
`***POST*** /email/messages` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message created. |
| 400 | Message cannot be created. [710] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified culture has not been found. [41]  The specified deliverability pack has not been found. [701]  The reply address has not been found. [705]  L'expéditeur spécifié n'existe pas. [702] |
| 409 | Le message spécifié existe déjà. [709] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /EMAIL/SENDINGS
## ***GET*** 

**Summary:** Return all message sendings.

**Description:** Return all message sendings.

### HTTP Request 
`***GET*** /email/sendings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| Channel | query | Channel. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sendings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new message sending.

**Description:** Create a new message sending.

### HTTP Request 
`***POST*** /email/sendings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message sending created. |
| 400 | Le message est verrouillé. [728]  Le segment spécifié est invalide. [526] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message unsubscribe link has not been found. [720]  L'expéditeur spécifié n'existe pas. [702]  The reply address has not been found. [705]  Le planning spécifié n'existe pas. [735]  Le message spécifié pour cette envoi n'existe pas. [729]  The specified user has not been found. [901]  The specified parameter has not been found. [44]  The specified application has not been found. [8]  The specified account has not been found. [9]  The specified message has not been found. [708] |
| 409 | Tracking must be validated. [721]  Le sujet du message n'est pas valide. [722]  Le pack de délivrabilité du message n'est pas autorisé. [723]  Le contenu du message n'est pas valide. [724]  The specified message sending already exists. [731]  Message content size is too big. [725]  Message failed the lock acquisition. [726]  There are too many contacts in the target for a test sending. [741] |
| 500 | An error occurred, message sending cannot be created. [742]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/{MESSAGEID}/DUPLICATE
## ***POST*** 

**Summary:** Duplicate specified message.

**Description:** Duplicate specified message.

### HTTP Request 
`***POST*** /sms/messages/{MessageID}/duplicate` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message duplicated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 409 | Message cannot be duplicated. [715] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/{MESSAGEID}/CONTENT
## ***GET*** 

**Summary:** Return specified message content.

**Description:** Return specified message content.

### HTTP Request 
`***GET*** /sms/messages/{MessageID}/content` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message content retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified message content.

**Description:** Update specified message content.

### HTTP Request 
`***PUT*** /sms/messages/{MessageID}/content` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message content updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/SENDERS/{SENDERID}
## ***PUT*** 

**Summary:** Update specified sender.

**Description:** Update specified sender.

### HTTP Request 
`***PUT*** /sms/messages/senders/{SenderID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SenderID | path | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Sender updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Expéditeur introuvable. [1202] |
| 409 | L'expéditeur existe déjà. [1201] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified sender.

**Description:** Delete specified sender.

### HTTP Request 
`***DELETE*** /sms/messages/senders/{SenderID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SenderID | path | Sender identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Sender deleted. |
| 400 | Sender cannot be deleted. [704] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Expéditeur introuvable. [1202] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/{SENDINGID}/CONTENT
## ***GET*** 

**Summary:** Return specified message content.

**Description:** Return specified message content.

### HTTP Request 
`***GET*** /sms/sendings/{SendingID}/content` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Message identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message content retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/{SENDINGID}/LOCKS
## ***GET*** 

**Summary:** Return specified message sending constraints.

**Description:** Return specified message sending constraints.

### HTTP Request 
`***GET*** /sms/sendings/{SendingID}/locks` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sending constraints retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |

# /SMS/SENDINGS/{SENDINGID}/REPORT
## ***GET*** 

**Summary:** Return specfied sending report file.

**Description:** Return specfied sending report file.

### HTTP Request 
`***GET*** /sms/sendings/{SendingID}/report` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| TargetID | query | Target identifier. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending report file retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729]  The specified target has not been found. [502] |
| 409 | Could not generate sending report. [753] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/{MESSAGEID}/CHECK
## ***GET*** 

**Summary:** Check if sms message is ready for sending.

**Description:** Check if sms message is ready for sending.

### HTTP Request 
`***GET*** /sms/messages/{MessageID}/check` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| SendType | query | Sending type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Check sms message done. |
| 403 | Vous devez ajouter une variable de désabonnement. [1207]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | L'expéditeur spécifié n'existe pas. [702]  La valeur de la clé de culture spécifié est introuvable. [223]  The specified message has not been found. [708] |
| 409 | Le contenu du message n'est pas valide. [724] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/DRAFT/CHECK
## ***POST*** 

**Summary:** Check if the message is ready to be sent.

**Description:** Check if the message is ready to be sent.

### HTTP Request 
`***POST*** /sms/messages/draft/check` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Check sms message done. |
| 403 | Vous devez ajouter une variable de désabonnement. [1207]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | L'expéditeur spécifié n'existe pas. [702] |
| 409 | Le pack de délivrabilité du message n'est pas autorisé. [723]  Le sujet du message n'est pas valide. [722]  Tracking must be validated. [721] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/{SENDINGID}/STANDBY
## ***POST*** 

**Summary:** Set specified message sending in standby mode.

**Description:** Set specified message sending in standby mode.

### HTTP Request 
`***POST*** /sms/sendings/{SendingID}/standby` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending set in standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/{SENDINGID}/RESUME
## ***POST*** 

**Summary:** Resume specified message sending from standby mode.

**Description:** Resume specified message sending from standby mode.

### HTTP Request 
`***POST*** /sms/sendings/{SendingID}/resume` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending resumed from standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/{SENDINGID}/STOP
## ***POST*** 

**Summary:** Stop specified message sending.

**Description:** Stop specified message sending.

### HTTP Request 
`***POST*** /sms/sendings/{SendingID}/stop` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending stopped. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 409 | Une erreur s'est produite, lors de l'envoi du fichier de ciblage SMS. [1208] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/{MESSAGEID}/TAGS
## ***GET*** 

**Summary:** Return tags of specified message.

**Description:** Return tags of specified message.

### HTTP Request 
`***GET*** /sms/messages/{MessageID}/tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/{SENDINGID}/TAGS
## ***GET*** 

**Summary:** Return tags of specified sending.

**Description:** Return tags of specified sending.

### HTTP Request 
`***GET*** /sms/sendings/{SendingID}/tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/{MESSAGEID}/ANALYZER/ASYNC
## ***POST*** 

**Summary:** Create a new analyzer async operation.

**Description:** Create a new analyzer async operation.

### HTTP Request 
`***POST*** /sms/messages/{MessageID}/analyzer/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Analyzer async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/DRAFT/ANALYZER/ASYNC
## ***POST*** 

**Summary:** Create a new analyzer async operation.

**Description:** Create a new analyzer async operation.

### HTTP Request 
`***POST*** /sms/messages/draft/analyzer/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Analyzer async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/{MESSAGEID}/SIMULATION/ASYNC
## ***POST*** 

**Summary:** Create a new simulation async operation.

**Description:** Create a new simulation async operation.

### HTTP Request 
`***POST*** /sms/messages/{MessageID}/simulation/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Simulation async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708]  The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/DRAFT/SIMULATION/ASYNC
## ***POST*** 

**Summary:** Create a new simulation draft async operation.

**Description:** Create a new simulation draft async operation.

### HTTP Request 
`***POST*** /sms/messages/draft/simulation/async` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Simulation draft async operation created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified target has not been found. [502] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES
## ***GET*** 

**Summary:** Return all messages.

**Description:** Return all messages.

### HTTP Request 
`***GET*** /sms/messages` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| Channel | query | Message channel. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Messages retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new message.

**Description:** Create a new message.

### HTTP Request 
`***POST*** /sms/messages` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message created. |
| 400 | Message cannot be created. [710] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified culture has not been found. [41]  L'expéditeur spécifié n'existe pas. [702] |
| 409 | Le message spécifié existe déjà. [709] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS
## ***GET*** 

**Summary:** Return all message sendings.

**Description:** Return all message sendings.

### HTTP Request 
`***GET*** /sms/sendings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| Channel | query | Channel. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sendings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new message sending.

**Description:** Create a new message sending.

### HTTP Request 
`***POST*** /sms/sendings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message sending created. |
| 400 | Le message est verrouillé. [728]  Le segment spécifié est invalide. [526] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | L'expéditeur spécifié n'existe pas. [702]  Le planning spécifié n'existe pas. [735]  Le message spécifié pour cette envoi n'existe pas. [729]  The specified message has not been found. [708] |
| 409 | Le contenu du message n'est pas valide. [724]  The specified message sending already exists. [731]  The last target contact count is too old. [740]  There are too many contacts in the target for a test sending. [741]  Message failed the lock acquisition. [726] |
| 500 | An error occurred, message sending cannot be created. [742]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/{MESSAGEID}
## ***GET*** 

**Summary:** Return specified message.

**Description:** Return specified message.

### HTTP Request 
`***GET*** /sms/messages/{MessageID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified message.

**Description:** Update specified message.

### HTTP Request 
`***PUT*** /sms/messages/{MessageID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| MessageID | path | Message identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message updated. |
| 400 | Message cannot be modified. [711] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified culture has not been found. [41]  Expéditeur introuvable. [1202] |
| 409 | Le message spécifié existe déjà. [709] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified message.

**Description:** Delete specified message.

### HTTP Request 
`***DELETE*** /sms/messages/{MessageID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| MessageID | path | Message identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message deleted. |
| 400 | Le message est verrouillé. [728]  Message cannot be deleted. [712] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified message has not been found. [708] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/SEARCH
## ***POST*** 

**Summary:** Return all messages found.

**Description:** Return all messages found.

### HTTP Request 
`***POST*** /sms/messages/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Messages retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/ENCODINGS
## ***GET*** 

**Summary:** Return all message encodings.

**Description:** Return all message encodings.

### HTTP Request 
`***GET*** /sms/messages/encodings` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message encodings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/CULTURES
## ***GET*** 

**Summary:** Return all available message cultures.

**Description:** Return all available message cultures.

### HTTP Request 
`***GET*** /sms/messages/cultures` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Available message cultures retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/MESSAGES/SENDERS
## ***GET*** 

**Summary:** Return all senders.

**Description:** Return all senders.

### HTTP Request 
`***GET*** /sms/messages/senders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Senders retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new sender.

**Description:** Create a new sender.

### HTTP Request 
`***POST*** /sms/messages/senders` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Sender created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | L'expéditeur existe déjà. [1201] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/{SENDINGID}
## ***GET*** 

**Summary:** Return specified message sending.

**Description:** Return specified message sending.

### HTTP Request 
`***GET*** /sms/sendings/{SendingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sending retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified message sending.

**Description:** Update specified message sending.

### HTTP Request 
`***PUT*** /sms/sendings/{SendingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sending updated. |
| 400 | Planning Start date must be later than now. [736] |
| 403 | Le statut de l'envoi n'est pas valide pour cette action. [732]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729]  Le planning spécifié n'existe pas. [735]  The specified message has not been found. [708] |
| 409 | The specified message sending already exists. [731] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/SEARCH
## ***POST*** 

**Summary:** Return all message sendings found.

**Description:** Return all message sendings found.

### HTTP Request 
`***POST*** /sms/sendings/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Message sendings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/STANDBY
## ***POST*** 

**Summary:** Set all message sendings in standby mode.

**Description:** Set all message sendings in standby mode.

### HTTP Request 
`***POST*** /sms/sendings/standby` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sendings set in standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/RESUME
## ***POST*** 

**Summary:** Resume all message sendings from standby mode.

**Description:** Resume all message sendings from standby mode.

### HTTP Request 
`***POST*** /sms/sendings/resume` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Message sendings resumed from standby mode. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /SMS/SENDINGS/STOP
## ***POST*** 

**Summary:** Stop all message sendings.

**Description:** Stop all message sendings.

### HTTP Request 
`***POST*** /sms/sendings/stop` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Message sendings stopped. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /PLANNINGS/ONETIME
## ***GET*** 

**Summary:** Return all one time plannings.

**Description:** Return all one time plannings.

### HTTP Request 
`***GET*** /plannings/onetime` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | query | Sending identifier. | Yes | integer |
| Channel | query | Channel. | Yes | string |
| CreatedAfter | query | Planning must have been created after this date. | No | dateTime |
| CreatedBefore | query | Planning must have been created before this date. | No | dateTime |
| SortOrder | query | Sort order. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | One time plannings retrieved. |
| 400 | The specified sending type is invalid. [749] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le message spécifié pour cette envoi n'existe pas. [729]  Le planning spécifié n'existe pas. [735] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new one time planning.

**Description:** Create a new one time planning.

### HTTP Request 
`***POST*** /plannings/onetime` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | One time planning created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | the specified planning volume has not been found. [737]  the specified planning period has not been found. [738] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /PLANNINGS/RECURRENTS
## ***GET*** 

**Summary:** Return all recurrent plannings.

**Description:** Return all recurrent plannings.

### HTTP Request 
`***GET*** /plannings/recurrents` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | query | Sending identifier. | Yes | integer |
| Channel | query | Channel. | Yes | string |
| CreatedAfter | query | Planning must have been created after this date. | No | dateTime |
| CreatedBefore | query | Planning must have been created before this date. | No | dateTime |
| SortOrder | query | Sort order. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Recurrent plannings retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le planning recurrent spécifié n'existe pas. [747] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new recurrent planning.

**Description:** Create a new recurrent planning.

### HTTP Request 
`***POST*** /plannings/recurrents` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Recurrent planning created. |
| 400 | The specified interval value is invalid. [745]  The specified filter value is invalid. [746] |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /PLANNINGS/ONETIME/{PLANNINGID}
## ***GET*** 

**Summary:** Return a specified one time planning.

**Description:** Return a specified one time planning.

### HTTP Request 
`***GET*** /plannings/onetime/{PlanningID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| PlanningID | path | Planning identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | One time planning retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le planning spécifié n'existe pas. [735]  Le taux du planning n'existe pas. [743] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /PLANNINGS/RECURRENTS/{PLANNINGID}
## ***GET*** 

**Summary:** Return a specified recurrent planning.

**Description:** Return a specified recurrent planning.

### HTTP Request 
`***GET*** /plannings/recurrents/{PlanningID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| PlanningID | path | Planning identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Recurrent planning retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le planning recurrent spécifié n'existe pas. [747] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /PLANNINGS/RECURRENTS/SIMULATION
## ***POST*** 

**Summary:** Computes the N next sending occurrences for the given planning settings

**Description:** Computes the N next sending occurrences for the given planning settings

### HTTP Request 
`***POST*** /plannings/recurrents/simulation` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SimulationCount | query | Number of dates to generate. | Yes | integer |
| SimulationStartDate | query | Start date | No | dateTime |
| SimulationEndDate | query | Simulation end date | No | dateTime |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Next occurrence dates retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /PLANNINGS/RECURRENTS/INTERVALS
## ***GET*** 

**Summary:** Return allowed interval values for specified frequency identifier.

**Description:** Return allowed interval values for specified frequency identifier.

### HTTP Request 
`***GET*** /plannings/recurrents/intervals` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| Frequency | query |  | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Allowed interval values retrieved. |
| 400 | An invalid argument has been specified. [36] |

# /PLANNINGS/RECURRENTS/FILTERS
## ***GET*** 

**Summary:** Return allowed filter values for specified frequency identifier.

**Description:** Return allowed filter values for specified frequency identifier.

### HTTP Request 
`***GET*** /plannings/recurrents/filters` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| Frequency | query |  | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Allowed filter values retrieved. |
| 400 | An invalid argument has been specified. [36] |

# /PLANNINGS/ONETIME/RATE/VOLUMES
## ***GET*** 

**Summary:** Return all planning rate volumes.

**Description:** Return all planning rate volumes.

### HTTP Request 
`***GET*** /plannings/onetime/rate/volumes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Planning rate volumes retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /PLANNINGS/ONETIME/RATE/PERIODS
## ***GET*** 

**Summary:** Return all planning rate periods.

**Description:** Return all planning rate periods.

### HTTP Request 
`***GET*** /plannings/onetime/rate/periods` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Planning rate periods retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ROLES/{ROLEID}
## ***GET*** 

**Summary:** Return specified role.

**Description:** Return specified role.

### HTTP Request 
`***GET*** /roles/{RoleID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Role retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified role.

**Description:** Update specified role.

### HTTP Request 
`***PUT*** /roles/{RoleID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Role updated. |
| 403 | Le nom de rôle est déjà utilisé. [106]  Le rôle est en mode lecture seul, la suppression ou modification est impossible. [105]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Le rôle ne peu pas être modifié. [103]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified role.

**Description:** Delete specified role.

### HTTP Request 
`***DELETE*** /roles/{RoleID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Role deleted. |
| 403 | Le rôle est en mode lecture seul, la suppression ou modification est impossible. [105]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Le rôle ne peu pas être supprimé. [104]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ROLES
## ***POST*** 

**Summary:** Create a new role.

**Description:** Create a new role.

### HTTP Request 
`***POST*** /roles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Role created. |
| 403 | Le nom de rôle est déjà utilisé. [106]  Droit insuffisant pour effectuer cette action. [6] |
| 500 | Le rôle ne peux pas être créé. [102]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ROLES/{ROLEID}/USERS
## ***GET*** 

**Summary:** Return role users.

**Description:** Return role users.

### HTTP Request 
`***GET*** /roles/{RoleID}/users` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Role users retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update role users.

**Description:** Update role users.

### HTTP Request 
`***PUT*** /roles/{RoleID}/users` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |
| OperationMode | query | Operation mode | Yes | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Role users updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ROLES/{ROLEID}/RIGHTLEVELS
## ***GET*** 

**Summary:** Return role rights.

**Description:** Return role rights.

### HTTP Request 
`***GET*** /roles/{RoleID}/rightlevels` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Role rights retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified role rights.

**Description:** Update specified role rights.

### HTTP Request 
`***PUT*** /roles/{RoleID}/rightlevels` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |
| OperationMode | query | Operation mode | Yes | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Role rights updated. |
| 403 | Le rôle est en mode lecture seul, la suppression ou modification est impossible. [105]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Impossible de mettre à jour les droits d'utilisateurs. [114]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Clone role rights.

**Description:** Clone role rights.

### HTTP Request 
`***POST*** /roles/{RoleID}/rightlevels` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RoleID | path | Role identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Role rights cloned. |
| 403 | Le rôle est en mode lecture seul, la suppression ou modification est impossible. [105]  Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le rôle demandé est introuvable. [101] |
| 500 | Impossible de mettre à jour les droits d'utilisateurs. [114]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/{USERID}/ROLES
## ***GET*** 

**Summary:** Return user roles.

**Description:** Return user roles.

### HTTP Request 
`***GET*** /users/{UserID}/roles` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| UserID | path | User identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User roles retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/{USERID}/RIGHTLEVELS
## ***GET*** 

**Summary:** Return user rights with levels.

**Description:** Return user rights with levels.

### HTTP Request 
`***GET*** /users/{UserID}/rightlevels` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| UserID | path | User identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User rights with levels retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified user has not been found. [901] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/{USERID}/ACCOUNTS
## ***GET*** 

**Summary:** Return user accounts.

**Description:** Return user accounts.

### HTTP Request 
`***GET*** /users/{UserID}/accounts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| UserID | path | User identifier. | Yes | integer |
| ApplicationID | query | Application identifier (optional filter). | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User accounts retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/PASSWORD/{TOKEN}
## ***PUT*** 

**Summary:** Define new password.

**Description:** Define new password.

### HTTP Request 
`***PUT*** /users/password/{Token}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| Token | path | Password token | Yes | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Password updated. |
| 400 | The given password does not match security rules. [902] |
| 404 | The specified token is not valid or has not been found. [903] |
| 500 | The password cannot be changed. [905]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /RIGHTS
## ***GET*** 

**Summary:** Return all rights.

**Description:** Return all rights.

### HTTP Request 
`***GET*** /rights` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Rights retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /RIGHTS/{RIGHTID}
## ***GET*** 

**Summary:** Return specified right.

**Description:** Return specified right.

### HTTP Request 
`***GET*** /rights/{RightID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| RightID | path | Right identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Right retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Le droit spécifié est introuvable. [126] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /RIGHTS/CATEGORIES
## ***GET*** 

**Summary:** Return all right categories.

**Description:** Return all right categories.

### HTTP Request 
`***GET*** /rights/categories` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Right categories retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /RIGHTS/TEMPLATES
## ***GET*** 

**Summary:** Return all right templates.

**Description:** Return all right templates.

### HTTP Request 
`***GET*** /rights/templates` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Right templates retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /RIGHTS/TEMPLATES/{TEMPLATEID}/RIGHTLEVELS
## ***GET*** 

**Summary:** Return template rights with levels.

**Description:** Return template rights with levels.

### HTTP Request 
`***GET*** /rights/templates/{TemplateID}/rightlevels` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| TemplateID | path | Template identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Template rights retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Ce template est introuvable. [113] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /RIGHTS/CATEGORIES/{CATEGORYID}
## ***GET*** 

**Summary:** Return specified right category.

**Description:** Return specified right category.

### HTTP Request 
`***GET*** /rights/categories/{CategoryID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| CategoryID | path | Category identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Right category retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | La catégorie spécifié est introuvable. [123] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /RIGHTS/TEMPLATES/{TEMPLATEID}
## ***GET*** 

**Summary:** Return specified right template.

**Description:** Return specified right template.

### HTTP Request 
`***GET*** /rights/templates/{TemplateID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ApplicationID | query | Application identifier | Yes | integer |
| AccountID | query | Account identifier | Yes | integer |
| TemplateID | path | Template identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Right template retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | Ce template est introuvable. [113] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}
## ***GET*** 

**Summary:** Return sending statistics.

**Description:** Return sending statistics.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| TargetID | query | Target identifier. | No | integer |
| IndicatorList | query | Indicators. | Yes | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified occurrence has not been found. [807] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/LASTTEN
## ***GET*** 

**Summary:** Return last 10 sendings statistics.

**Description:** Return last 10 sendings statistics.

### HTTP Request 
`***GET*** /statistics/email/sendings/lastten` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| IndicatorList | query | Indicators. | Yes | array |
| Type | query | Type | No | string |
| StatusGroup | query | Status group. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/IGQ
## ***GET*** 

**Summary:** Return IGQ average home sending statistics .

**Description:** Return IGQ average home sending statistics .

### HTTP Request 
`***GET*** /statistics/email/sendings/igq` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| AggregateTypeIGQ | query | IGQ aggregate type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | IGQ average home sending statistics  retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/TIMELINE
## ***GET*** 

**Summary:** Return a sending statistics sent volume on the thirty last days.

**Description:** Return a sending statistics sent volume on the thirty last days.

### HTTP Request 
`***GET*** /statistics/email/sendings/timeline` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| AggregateType | query | Aggregate type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics sent volume retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/SMS/SENDINGS/{SENDINGID}
## ***GET*** 

**Summary:** Return sending statistics.

**Description:** Return sending statistics.

### HTTP Request 
`***GET*** /statistics/sms/sendings/{SendingID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| TargetID | query | Target identifier | No | integer |
| IndicatorList | query | Indicators. | Yes | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending  statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified occurrence has not been found. [807] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/SMS/SENDINGS/LASTTEN
## ***GET*** 

**Summary:** Return last 10 sms sending statistics.

**Description:** Return last 10 sms sending statistics.

### HTTP Request 
`***GET*** /statistics/sms/sendings/lastten` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| IndicatorList | query | Indicators. | Yes | array |
| Type | query | Type | No | string |
| StatusGroup | query | Status group. | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending  statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/SMS/SENDINGS/TIMELINE
## ***GET*** 

**Summary:** Return a sending statistics sent volume on the thirty last days.

**Description:** Return a sending statistics sent volume on the thirty last days.

### HTTP Request 
`***GET*** /statistics/sms/sendings/timeline` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| AggregateType | query | Aggregate type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics sent volume retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/TIMELINE
## ***GET*** 

**Summary:** Return sending statistics time line.

**Description:** Return sending statistics time line.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}/timeline` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| TargetID | query | Target identifier. | No | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| StartDate | query | Start date. | Yes | dateTime |
| EndDate | query | End date. | Yes | dateTime |
| AggregateType | query | Aggregate type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics time line retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/DOMAINS
## ***GET*** 

**Summary:** Return domain sending statistics.

**Description:** Return domain sending statistics.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}/domains` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| IndicatorList | query | Indicators. | Yes | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Domain sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/LINKS
## ***GET*** 

**Summary:** Return link sending statistics.

**Description:** Return link sending statistics.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}/links` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| TargetID | query | Target identifier. | No | integer |
| Offset | query | Pagination index. (start at 0). | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Link sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/GROUPINTERESTS
## ***GET*** 

**Summary:** Return interest groups sending statistics.

**Description:** Return interest groups sending statistics.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}/groupinterests` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| TargetID | query | Target identifier. | No | integer |
| Offset | query | Pagination index. (start at 0). | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Interest groups sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/USERAGENTS
## ***GET*** 

**Summary:** Return user agent sending statistics.

**Description:** Return user agent sending statistics.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}/useragents` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| TargetID | query | Target identifier. | No | integer |
| RequestType | query | Request type. | Yes | string |
| Category | query | Category. | Yes | string |
| Offset | query | Pagination index. (start at 0). | No | integer |
| Limit | query | Limit. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User agent sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/IGQ
## ***GET*** 

**Summary:** Return average IGQ sending statistics.

**Description:** Return average IGQ sending statistics.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}/igq` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier | Yes | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | IGQ average sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/TARGETS
## ***POST*** 

**Summary:** Create target sending statistics.

**Description:** Create target sending statistics.

### HTTP Request 
`***POST*** /statistics/email/sendings/{SendingID}/targets` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Target sending statistics retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/SMS/SENDINGS/{SENDINGID}/TIMELINE
## ***GET*** 

**Summary:** Return sending statistics time line.

**Description:** Return sending statistics time line.

### HTTP Request 
`***GET*** /statistics/sms/sendings/{SendingID}/timeline` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| TargetID | query | Target identifier. | No | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| StartDate | query | Start date. | Yes | dateTime |
| EndDate | query | End date. | Yes | dateTime |
| AggregateType | query | Aggregate type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics time line retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/SMS/SENDINGS/{SENDINGID}/UNITS
## ***GET*** 

**Summary:** Return unit sending statistics retrieved.

**Description:** Return unit sending statistics retrieved.

### HTTP Request 
`***GET*** /statistics/sms/sendings/{SendingID}/units` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| TargetID | query | Target identifier. | No | integer |
| OccurrenceID | query | Occurrence identifier. | No | integer |
| StartDate | query | Start date. | No | dateTime |
| EndDate | query | End date. | No | dateTime |
| IndicatorList | query | Indicators. | Yes | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Unit sending statistics retrieved |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/EMAIL/SENDINGS/{SENDINGID}/TIMELINE/OCCURRENCES
## ***GET*** 

**Summary:** Return sending statistics time line with occurrences.

**Description:** Return sending statistics time line with occurrences.

### HTTP Request 
`***GET*** /statistics/email/sendings/{SendingID}/timeline/occurrences` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| TargetID | query | Target identifier. | No | integer |
| EndDate | query | End date. | Yes | dateTime |
| OccurrenceCount | query | Occurrence count - Default : 250 occurrences. | No | integer |
| IndicatorList | query | Indicators. | Yes | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics time line with occurrences retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/SMS/SENDINGS/{SENDINGID}/TIMELINE/OCCURRENCES
## ***GET*** 

**Summary:** Return sending statistics time line with occurrences.

**Description:** Return sending statistics time line with occurrences.

### HTTP Request 
`***GET*** /statistics/sms/sendings/{SendingID}/timeline/occurrences` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| SendingID | path | Sending identifier. | Yes | integer |
| TargetID | query | Target identifier. | No | integer |
| EndDate | query | End date. | Yes | dateTime |
| OccurrenceCount | query | Occurrence count - Default : 250 occurrences. | No | integer |
| IndicatorList | query | Indicators. | Yes | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics time line with occurrences retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /STATISTICS/CONTACTS/TIMELINE
## ***GET*** 

**Summary:** Return sending statistics contact time line.

**Description:** Return sending statistics contact time line.

### HTTP Request 
`***GET*** /statistics/contacts/timeline` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| AggregateType | query | Aggregate type. | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Sending statistics contact time line retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/{TAGID}
## ***GET*** 

**Summary:** Return specified tag.

**Description:** Return specified tag.

### HTTP Request 
`***GET*** /tags/{TagID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TagID | path | Tag identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Tag retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified tag has not be found. [1703] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified tag.

**Description:** Update specified tag.

### HTTP Request 
`***PUT*** /tags/{TagID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TagID | path | Tag identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Tag updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified tag has not be found. [1703] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0]  Tag cannot be updated. [1704] |

## ***DELETE*** 

**Summary:** Delete specified tag.

**Description:** Delete specified tag.

### HTTP Request 
`***DELETE*** /tags/{TagID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| TagID | path | Tag identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Tag deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified tag has not be found. [1703] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0]  Tag cannot be deleted. [1702] |

# /TAGS/COLORS
## ***GET*** 

**Summary:** Return all colors.

**Description:** Return all colors.

### HTTP Request 
`***GET*** /tags/colors` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Colors retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/ITEMTYPES
## ***GET*** 

**Summary:** Return all item types.

**Description:** Return all item types.

### HTTP Request 
`***GET*** /tags/itemTypes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Item types retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/SEARCH
## ***POST*** 

**Summary:** Search tags.

**Description:** Search tags.

### HTTP Request 
`***POST*** /tags/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Tags search done. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/ITEMS
## ***PUT*** 

**Summary:** Add or remove tags to/form items.

**Description:** Add or remove tags to/form items.

### HTTP Request 
`***PUT*** /tags/items` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Add or remove tags to items. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified tag has not be found. [1703] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/COLORS/{COLORID}
## ***GET*** 

**Summary:** Return specified color.

**Description:** Return specified color.

### HTTP Request 
`***GET*** /tags/colors/{ColorID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ColorID | path | Color identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Color retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified tag color has not be found. [1705] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/ITEMTYPES/{ITEMTYPEID}
## ***GET*** 

**Summary:** Return specified item type.

**Description:** Return specified item type.

### HTTP Request 
`***GET*** /tags/itemTypes/{ItemTypeID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ItemTypeID | path | Item type identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Item type retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified item type tag has not be found. [1706] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/ITEMS/SEARCH
## ***POST*** 

**Summary:** Search item by tags.

**Description:** Search item by tags.

### HTTP Request 
`***POST*** /tags/items/search` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Tags search done. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS
## ***GET*** 

**Summary:** Return all tags.

**Description:** Return all tags.

### HTTP Request 
`***GET*** /tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***POST*** 

**Summary:** Create a new tag.

**Description:** Create a new tag.

### HTTP Request 
`***POST*** /tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | Tag created. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 409 | Le nom de ce tag existe déjà. [1701] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /TAGS/ITEMS/{ITEMTYPE}/{ITEMID}/TAGS
## ***GET*** 

**Summary:** Return tags of specified item.

**Description:** Return tags of specified item.

### HTTP Request 
`***GET*** /tags/items/{ItemType}/{ItemID}/tags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier. | Yes | integer |
| ItemType | path | Type of item. | Yes | string |
| ItemID | path | Item identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Item tags retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/LICENCE
## ***GET*** 

**Summary:** Return authenticated user administrative list.

**Description:** Return authenticated user administrative list.

### HTTP Request 
`***GET*** /users/licence` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User administrative list retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/ATTRIBUTES
## ***GET*** 

**Summary:** Return available user attributes.

**Description:** Return available user attributes.

### HTTP Request 
`***GET*** /users/attributes` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User attributes retrieved. |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/{USERID}
## ***GET*** 

**Summary:** Return specified user.

**Description:** Return specified user.

### HTTP Request 
`***GET*** /users/{UserID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| UserID | path | User identifier. | Yes | integer |
| RequiredFieldList | query | Required field list. | No | array |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified user.

**Description:** Update specified user.

### HTTP Request 
`***PUT*** /users/{UserID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| UserID | path | User identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | User updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | The user cannot be modified. [907]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***DELETE*** 

**Summary:** Delete specified user.

**Description:** Delete specified user.

### HTTP Request 
`***DELETE*** /users/{UserID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| UserID | path | User identifier. | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | User deleted. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | The user cannot be deleted. [904]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS/PASSWORD
## ***POST*** 

**Summary:** Initialize password renewal.

**Description:** Initialize password renewal.

### HTTP Request 
`***POST*** /users/password` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| ValidationKey | query | Validation Key | No | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Password renewal procedure initialized. |
| 400 | Recaptcha invalide. [13] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /ACCOUNTS
## ***GET*** 

**Summary:** Return all user accounts.

**Description:** Return all user accounts.

### HTTP Request 
`***GET*** /accounts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| UserFunction | query | User function. | Yes | string |
| ApplicationID | query | Application identifier. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | User accounts retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /USERS
## ***POST*** 

**Summary:** Create a new user.

**Description:** Créer un utilisateur (lié à aucun compte) avec les informations spécifiées dans les propriétés **AttributeList** et **Email**. Bien que la seule propriété obligatoire soit l’adresse e-mail, vous pouvez cependant enrichir les informations relatives à un utilisateur en ajoutant des attributs, cela fonctionne comme une liste de clé-valeur, vous pouvez trouver tous les attributs disponibles en utilisant la route suivante : */users/attributes*.

Une fois l’utilisateur créé vous pouvez le lié à un ou plusieurs compte en utilisant cette route : *POST /accouts/{AccountID}/users*

### HTTP Request 
`***POST*** /users` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| User | query |  | No | string |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 201 | User created. |
| 500 | The user cannot be created. [906]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /VARIABLES/{VARIABLEID}
## ***GET*** 

**Summary:** Return specified variable.

**Description:** Return specified variable.

### HTTP Request 
`***GET*** /variables/{VariableID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| VariableID | path | Variable identifier | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Variable retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified Variable has not been found. [601] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

## ***PUT*** 

**Summary:** Update specified variable.

**Description:** Update specified variable.

### HTTP Request 
`***PUT*** /variables/{VariableID}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| VariableID | path | Variable identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 204 | Variable updated. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 404 | The specified Variable has not been found. [601] |
| 409 | The specified variable name already exists. [603] |
| 500 | The specified variable name cannot be modified. [602]  Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /VARIABLES/VARIABLEVALUES
## ***POST*** 

**Summary:** Return variables values.

**Description:** Return variables values.

### HTTP Request 
`***POST*** /variables/variablevalues` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| body | body |  | No |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Variables values retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

# /VARIABLES
## ***GET*** 

**Summary:** Return all variables.

**Description:** Return all variables.

### HTTP Request 
`***GET*** /variables` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
|  |  |  | No |  |
| AccountID | query | Account identifier | Yes | integer |
| Type | query | Variable type | No | string |
| SearchValue | query | Search value | No | string |
| Offset | query | Pagination index. (start at 0) | No | integer |
| Limit | query | Limit | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Variables retrieved. |
| 403 | Droit insuffisant pour effectuer cette action. [6] |
| 500 | Une exception inattendue est survenue. Veuillez contacter le support. [0] |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->

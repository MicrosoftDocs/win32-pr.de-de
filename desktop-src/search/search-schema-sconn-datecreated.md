---
description: Das optionale <dateCreated> -Element identifiziert das Datum und die Uhrzeit der Erstellung dieses Suchconnector mit dem ISO 8601-Standard. Sie verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: DateCreated-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750344"
---
# <a name="datecreated-element-search-connector-schema"></a>DateCreated-Element (Suchconnector-Schema)

Das optionale <dateCreated> -Element identifiziert das Datum und die Uhrzeit der Erstellung dieses Suchconnector mit dem ISO 8601-Standard. Sie verfügt über keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Das Format des Werts dieses Elements folgt dem ISO 8601-Standard. Eine gängige Verwendung wäre eine der folgenden:

-   \[Yyyy \] - \[ mm \] - \[ DD \] T \[ HH \] : \[ mm \] : \[ SS \] ± \[ HH \] : \[ mm \] ("1981-04-05t14:30:30-05:00")
-   \[Yyyy \] \[ mm \] \[ DD \] T \[ HH \] \[ mm \] \[ SS \] Z ("19810405t193030Z")

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 




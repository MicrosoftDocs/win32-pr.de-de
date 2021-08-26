---
description: Das optionale &lt; dateCreated-Element &gt; identifiziert das Datum und die Uhrzeit der Erstellung dieses Suchconnectors unter Verwendung des ISO 8601-Standards. Es verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: dateCreated-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eff7c739bcad9e3a6594008597c0392398f22864
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882509"
---
# <a name="datecreated-element-search-connector-schema"></a>dateCreated-Element (Search Connector Schema)

Das optionale &lt; dateCreated-Element &gt; identifiziert das Datum und die Uhrzeit der Erstellung dieses Suchconnectors unter Verwendung des ISO 8601-Standards. Es verfügt über keine untergeordneten Elemente und keine Attribute.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Hinweise

Das Format des Werts dieses Elements entspricht dem ISO 8601-Standard. Eine häufige Verwendung wäre eine der folgenden:

-   \[YYYY \] - \[ MM \] - \[ DD \] T \[ hh : mm : \] \[ \] \[ ss ± \] \[ hh : mm \] \[ \] ("1981-04-05T14:30:30-05:00")
-   \[YYYY \] \[ MM \] \[ DD \] T \[ hh mm \] \[ \] \[ ss \] Z ("19810405T193030Z")

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 




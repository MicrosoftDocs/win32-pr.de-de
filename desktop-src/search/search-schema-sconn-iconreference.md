---
description: Das optionale <iconReference> -Element gibt ein benutzerdefiniertes Symbol für diesen Speicherort an. Dieses Element verfügt über keine Attribute und keine untergeordneten Elemente.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: iconReference-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76391eb7079414abe13c4e45696ee3eacb3b968eb93b342b1b9e67825fac85c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862584"
---
# <a name="iconreference-element-search-connector-schema"></a>iconReference-Element (Connectorschema suchen)

Das optionale <iconReference> -Element gibt ein benutzerdefiniertes Symbol für diesen Speicherort an. Dieses Element verfügt über keine Attribute und keine untergeordneten Elemente.

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
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

Das Format des Verweises muss in einem für die [PathParseIconLocation-Funktion](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) geeigneten Format angegeben werden: (z. B. <dll file name> , <icon index> ).

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 

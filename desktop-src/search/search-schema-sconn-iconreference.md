---
description: Das &lt; optionale &gt; IconReference-Element gibt ein benutzerdefiniertes Symbol für diesen Speicherort an. Dieses Element verfügt über keine Attribute und keine untergeordneten Elemente.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: iconReference-Element (Suchconnectorschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ff41d6dfd37e5e3fe780171701886b08b195ac
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882416"
---
# <a name="iconreference-element-search-connector-schema"></a>iconReference-Element (Suchconnectorschema)

Das &lt; optionale &gt; IconReference-Element gibt ein benutzerdefiniertes Symbol für diesen Speicherort an. Dieses Element verfügt über keine Attribute und keine untergeordneten Elemente.

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



 

 

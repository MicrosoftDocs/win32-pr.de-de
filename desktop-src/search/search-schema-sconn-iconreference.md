---
description: Das optionale- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Position an. Dieses Element hat keine Attribute und keine untergeordneten Elemente.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: iconReference-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525463"
---
# <a name="iconreference-element-search-connector-schema"></a>iconReference-Element (Suchconnector-Schema)

Das optionale- <iconReference> Element gibt ein benutzerdefiniertes Symbol für diese Position an. Dieses Element hat keine Attribute und keine untergeordneten Elemente.

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
| [searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Das Format des Verweises muss in einer für die [pathparametenconlocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) -Funktion geeigneten Form angegeben werden: (z <dll file name> . b <icon index> .,).

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 

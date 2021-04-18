---
description: Das boolesche <supportsAdvancedQuerySyntax> Element gibt an, ob der Suchanbieter die Erweiterte Abfrage Syntax unterstützt. Die Standardeinstellung ist „false“. Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: supportsadvancedquerysyntax-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341185"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>supportsadvancedquerysyntax-Element (Suchconnector-Schema)

Das boolesche <supportsAdvancedQuerySyntax> Element gibt an, ob der Suchanbieter die [Erweiterte Abfrage Syntax](-search-3x-advancedquerysyntax.md)unterstützt. Die Standardeinstellung ist „false“. Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
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

Der Wert `true` gibt an, dass der Suchanbieter Erweiterte Abfrage Syntax unterstützt, die in Such Abfragen gesendet wird.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 




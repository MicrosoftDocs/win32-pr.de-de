---
description: Das boolesche <supportsAdvancedQuerySyntax> Element gibt an, ob der Suchanbieter die erweiterte Abfragesyntax unterstützt. Der Standardwert ist false. Dieses Element ist optional und hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: supportsAdvancedQuerySyntax-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8235c1021ae04cbbce65500ebf008f645ef74c1f2bb6ea7f3a9edfe4253e035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844510"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a>supportsAdvancedQuerySyntax-Element (Search Connector Schema)

Das boolesche <supportsAdvancedQuerySyntax> Element gibt an, ob der Suchanbieter die [erweiterte Abfragesyntax](-search-3x-advancedquerysyntax.md)unterstützt. Der Standardwert ist false. Dieses Element ist optional und hat keine untergeordneten Elemente und keine Attribute.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Hinweise

Der Wert `true` gibt an, dass der Suchanbieter erweiterte Abfragesyntax unterstützt, die in Suchabfragen gesendet wird.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 




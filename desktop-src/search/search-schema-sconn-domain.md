---
description: Das optionale- <domain> Element gibt die URL des Such Dienstanbieter an, der von diesem Suchconnector verwendet wird. Er wird im Detailfenster angezeigt. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Domain-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862147"
---
# <a name="domain-element-search-connector-schema"></a>Domain-Element (Suchconnector-Schema)

Das optionale- <domain> Element gibt die URL des Such Dienstanbieter an, der von diesem Suchconnector verwendet wird. Er wird im Detailfenster angezeigt. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
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

Die URL sollte die Domäne der obersten Ebene für den Suchanbieter sein. Beispiel: https://www.example.com.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 




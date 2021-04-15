---
description: Das boolesche <isSearchOnlyItem> Element gibt an, ob der Suchanbieter zusätzlich zum Suchmodus den Durchsuchenmodus unterstützt. Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: issearchonlyitem-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525454"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>issearchonlyitem-Element (Suchconnector-Schema)

Das boolesche <isSearchOnlyItem> Element gibt an, ob der Suchanbieter zusätzlich zum Suchmodus den Durchsuchenmodus unterstützt. Dieses Element ist optional und verfügt über keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
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

Der Wert `true` gibt an, dass der Suchconnector-Speicherort von Benutzern nicht durchsucht werden kann. Der Wert `false` gibt an, dass Benutzer den Suchconnector-Speicherort durchsuchen können.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 




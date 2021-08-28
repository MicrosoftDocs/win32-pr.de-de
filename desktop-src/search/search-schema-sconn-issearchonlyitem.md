---
description: Das boolesche &lt; isSearchOnlyItem-Element &gt; gibt an, ob der Suchanbieter den Suchmodus zusätzlich zum Suchmodus unterstützt. Dieses Element ist optional und hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: isSearchOnlyItem-Element (Connectorschema suchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524a69198a650e0cb995d2ff8b4fc942ebfdaddc
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883420"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>isSearchOnlyItem-Element (Connectorschema suchen)

Das boolesche &lt; isSearchOnlyItem-Element &gt; gibt an, ob der Suchanbieter den Suchmodus zusätzlich zum Suchmodus unterstützt. Dieses Element ist optional und hat keine untergeordneten Elemente und keine Attribute.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Hinweise

Der Wert `true` gibt an, dass der Speicherort des Suchconnectors nicht von Benutzern durchsucht werden kann. Der Wert `false` gibt an, dass Benutzer den Speicherort des Suchconnectors durchsuchen können.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 




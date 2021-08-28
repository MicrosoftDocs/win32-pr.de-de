---
description: Das optionale boolesche &lt; Element isDefaultNonOwnerSaveLocation gibt an, ob der im Suchconnector beschriebene Speicherort als Standardspeicherort verwendet werden soll, wenn ein Benutzer eines anderen Computers in einer Homegroup ein Element speichern &gt; möchte.
ms.assetid: 4286b122-2454-4dc3-9c06-9967b7a763dd
title: isDefaultNonOwnerSaveLocation-Element (Connectorschema durchsuchen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2a20912b10864d856bd4513e31a37eeee5c2a0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881932"
---
# <a name="isdefaultnonownersavelocation-element-search-connector-schema"></a>isDefaultNonOwnerSaveLocation-Element (Connectorschema durchsuchen)

Das optionale boolesche &lt; Element isDefaultNonOwnerSaveLocation gibt an, ob der im Suchconnector beschriebene Speicherort als Standardspeicherort verwendet werden soll, wenn ein Benutzer eines anderen Computers in einer Homegroup ein Element speichern &gt; möchte. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultNonOwnerSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/>
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

True gibt an, dass der Windows-Explorer das Element an dem im simpleLocation-Element angegebenen Speicherort speichert, wenn ein Benutzer von einem anderen Computer in einer Homegroup ein Element &lt; &gt; speichert.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
    ...
</searchConnectionDescription>
```



 

 




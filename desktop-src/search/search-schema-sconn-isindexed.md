---
description: Das optionale boolesche <isIndexed> Element gibt an, ob der vom Suchconnector beschriebene Speicherort indiziert wird (entweder lokal oder Remote mit Windows Search 4 oder höher).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: isinentxed-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128496"
---
# <a name="isindexed-element-search-connector-schema"></a>isinentxed-Element (Suchconnector-Schema)

Das optionale boolesche <isIndexed> Element gibt an, ob der vom Suchconnector beschriebene Speicherort indiziert wird (entweder lokal oder Remote mit Windows Search 4 oder höher). Der Standardwert ist true für lokale Ordner. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
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



 

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 




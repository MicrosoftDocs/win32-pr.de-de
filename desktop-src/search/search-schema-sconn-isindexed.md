---
description: Das optionale boolesche <isIndexed> Element gibt an, ob der vom Suchconnector beschriebene Speicherort indiziert wird (lokal oder remote mit Windows Search 4 oder höher).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: isIndexed-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afcd1a95ec14b3bbea80374d8925a88231feb0110a421c2c850a297672d0c1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711050"
---
# <a name="isindexed-element-search-connector-schema"></a>isIndexed-Element (Search Connector Schema)

Das optionale boolesche <isIndexed> Element gibt an, ob der vom Suchconnector beschriebene Speicherort indiziert wird (lokal oder remote mit Windows Search 4 oder höher). Der Standardwert ist true für lokale Ordner. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

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
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 




---
description: Das optionale boolesche &lt; isIndexed-Element &gt; gibt an, ob der vom Suchconnector beschriebene Speicherort (lokal oder remote mit Windows Search 4 oder höher) indiziert wird.
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: isIndexed-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3588d451631ab8d0bb8313092b5b1ee7bb5c9dc4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881845"
---
# <a name="isindexed-element-search-connector-schema"></a>isIndexed-Element (Search Connector Schema)

Das optionale boolesche &lt; isIndexed-Element &gt; gibt an, ob der vom Suchconnector beschriebene Speicherort (lokal oder remote mit Windows Search 4 oder höher) indiziert wird. Der Standardwert ist true für lokale Ordner. Dieses Element weist keine untergeordneten Elemente und keine Attribute auf.

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



 

 




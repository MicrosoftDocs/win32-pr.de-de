---
description: Das optionale &lt; &gt; author-Element gibt den Autor dieser Bibliothek an. Dieses Element weist keine untergeordneten Elemente und keine Attribute auf.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: author-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5b99197db6c32be6b6e526a739a5e3fe1f00ef
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887431"
---
# <a name="author-element-search-connector-schema"></a>author-Element (Search Connector Schema)

Das optionale &lt; &gt; author-Element gibt den Autor dieser Bibliothek an. Dieses Element weist keine untergeordneten Elemente und keine Attribute auf.

## <a name="syntax"></a>Syntax


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
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
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 




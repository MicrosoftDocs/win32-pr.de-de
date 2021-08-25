---
description: Das <author> optionale -Element gibt den Autor dieser Bibliothek an. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: author-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0a6b0eb8103f1f1c962984be488a162b645a128f0477ab851d2819aacc3e74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885180"
---
# <a name="author-element-search-connector-schema"></a>author-Element (Search Connector Schema)

Das <author> optionale -Element gibt den Autor dieser Bibliothek an. Dieses Element verfügt über keine untergeordneten Elemente und keine Attribute.

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



 

 




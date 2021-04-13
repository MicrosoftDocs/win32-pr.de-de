---
description: Der optionale <description> das-Element gibt eine Beschreibung für diesen Suchconnector an. Dieses Element hat keine untergeordneten Elemente und keine Attribute.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: Description-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342919"
---
# <a name="description-element-search-connector-schema"></a>Description-Element (Suchconnector-Schema)

Der optionale <description> das-Element gibt eine Beschreibung für diesen Suchconnector an. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
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

Die Beschreibung sollte benutzerfreundlich sein, da Sie in Quick Infos verwendet werden kann.

## <a name="example"></a>Beispiel


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 




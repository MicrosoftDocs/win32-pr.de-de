---
description: Das optionale <scope> -Element gibt eine Auflistung von <scopeItem> Elementen an, die die Bereichseinschlüsse und -ausschlüsse für diesen bestimmten Suchconnector definieren.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: scope-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d5fcdb3908f495d07199c61a2005a4f97ba5a01c641fb4e854961489e7abe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944300"
---
# <a name="scope-element-search-connector-schema"></a>scope-Element (Search Connector Schema)

Das optionale <scope> -Element gibt eine Auflistung von <scopeItem> Elementen an, die die Bereichseinschlüsse und -ausschlüsse für diesen bestimmten Suchconnector definieren. Wenn <scope> vorhanden ist, MUSS es mindestens ein <scopeItem> Element enthalten. Dieses Element weist keine Attribute auf.

## <a name="syntax"></a>Syntax


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                                                   | Untergeordnete Elemente                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md) | [scopeItem-Element (Search Connector Schema)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie die <scope> Elemente und , um zu <scopeItem> ermitteln, welche Standorte durchsucht werden sollen und welche Standorte von der Suche ausgeschlossen werden sollen.

## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Suchbereich, der C: \\ ExampleFolder und alle seine untergeordneten Ordner mit Ausnahme von C: \\ ExampleFolder \\ ExcludeMe enthält.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



